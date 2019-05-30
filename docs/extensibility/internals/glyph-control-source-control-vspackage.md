---
title: Karakter denetimi (kaynak denetimi VSPackage'ı) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- glyphs, source control packages
- source control packages, glyphs
ms.assetid: b9413b08-b3c3-4fc3-a6e0-3dc0db3652d7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d30682a85551aab062824688b635260c30df63f9
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66321343"
---
# <a name="glyph-control-source-control-vspackage"></a>Karakter denetimi (kaynak denetimi VSPackage'ı)
Kaynak denetimi altında öğelerinin durumunu göstermek için kendi karakterleri görüntüleme olanağı kaynak denetimi VSPackage'ları için kullanılabilecek kapsamlı tümleştirme parçasıdır.

## <a name="levels-of-glyph-control"></a>Karakter denetimi düzeyleri
 Bir durum karakter görüntülendiğinde örneğin bir öğe geçerli durumunu belirten bir simge olan **Çözüm Gezgini** veya **sınıf görünümü**. Kaynak denetimi VSPackage'ı, iki düzeyde karakter denetimi alıştırma yapabilirsiniz. Glif tarafından sağlanan önceden tanımlanmış bir dizi karakter seçimi sınırlayabilirsiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE veya özel karakterler görüntülenecek kümesi tanımlayabilirsiniz.

### <a name="default-set-of-glyphs"></a>Varsayılan karakter kümesi
 Bir öğe ile ilişkili olan durum karakterleri belirlemek için **Çözüm Gezgini**, kaynak denetimi kullanarak bir proje durumu glif istekleri <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.GetSccGlyph%2A>. Kaynak denetimi VSPackage'ı IDE tarafından sağlanan önceden tanımlanmış karakter sınırlı karakter seçimi tutmak isteyebilirsiniz. Bu durumda, VSPackage tanımlanan karakter sabit listeleri temsil eden bir değer dizisi geçirir *vsshell.idl*. Daha fazla bilgi için bkz. <xref:Microsoft.VisualStudio.Shell.Interop.VsStateIcon>. Bu önceden tanımlanmış iade karakter için bir kilit ve kullanıma karakter için bir onay işareti gibi IDE tarafından belirlenen karakter kümesidir.

### <a name="custom-set-of-glyphs"></a>Özel karakter kümesi
 Kaynak denetimi VSPackage'ı yüklü olduğunda kendi karakterleri için benzersiz bir görünümü ve deneyimini kullanabilirsiniz. Yeni bir kaynak denetimi VSPackage'ı etkin olduğunda, kendi karakterleri önceki kaynak denetimi VSPackage'ı bile hala yüklendiği kullanmaya başlamak kullanabilirsiniz, ancak etkin olmalıdır. Bu modda, kaynak denetimi VSPackage'ı mevcut simgeler ile tutarlı bir görünüm sürdürmek için kullanmaya devam edebilirsiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] seçerse bu.

 <xref:Microsoft.VisualStudio.Shell.Interop.SVsSccManager> Hizmetini destekleyen bir arabirim <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccGlyphs>, hangi VSPackage isteğe bağlı olarak uygulayabilir ve hangi istenecektir için IDE tarafından. IDE bir istek yaptığında [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] sırayla bu arabirimin geçerli olarak kayıtlı kaynak denetimi VSPackage'ı almaya çalışır. Arabirimi içinde kayıtlı VSPackage varsa, özel karakterler iste IDE'nin başarılı; Aksi takdirde, [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE kendi varsayılan kümesine kullanır.

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccGlyphs.GetCustomGlyphList%2A> Yöntemi tarafından kullanılan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] çeşitli kaynak denetimi gösteren görüntülerin listesini almak için belirtir. Kaynak denetimi VSPackage'ı IDE, özel karakterler için resim listesi için bir tanıtıcı döndürür. IDE, bu noktada görüntü listesi kopyasını oluşturur ve daha sonra görüntülenecek karakterleri seçmek için kullanır. Yeni Arabirim desteklenmiyorsa veya `IVsSccGlyphs::GetCustomGlyphList` yöntemi döndürür `E_NOTIMPL`, IDE karakterleri tarafından sağlanan varsayılan listesinden kendi karakterleri alır, ardından [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccGlyphs>
- <xref:Microsoft.VisualStudio.Shell.Interop.VsStateIcon>
- <xref:Microsoft.VisualStudio.Shell.Interop.SVsSccManager>