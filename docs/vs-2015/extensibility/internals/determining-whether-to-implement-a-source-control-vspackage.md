---
title: Bir kaynak denetimi VSPackage'ı uygulanmayacağını belirleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control packages, about source control packages
ms.assetid: 60b3326e-e7e2-4729-95fc-b682e7ad5c99
caps.latest.revision: 25
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: cff53700dcd6a80f841108d5a2b486dcb0ba7a11
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60090848"
---
# <a name="determining-whether-to-implement-a-source-control-vspackage"></a>Kaynak Denetimi VSPackage’ının Uygulanıp Uygulanmayacağını Belirleme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bu bölümde, kaynak denetimi uygun tümleştirme yolu seçme hakkında çözümler ve verir geniş yönergeleri genişletmek için kaynak denetimi eklentileri ve kaynak denetimi VSPackage'ları seçimleri elaborates.  
  
## <a name="small-source-control-solution-with-limited-resources"></a>Küçük kaynak denetimine çözüm sınırlı kaynaklarla  
 Kaynakların sınırlı ve kaynak denetimi paketi yazma yüklerle burdened, kaynak denetimi eklentisi API tabanlı eklentiler oluşturabilirsiniz. Bu sayede kaynak denetimi paketleri ile yan yana çalışmaya ve kaynak denetimi eklentileri ve isteğe bağlı paketleri arasında geçiş yapabilirsiniz. Daha fazla bilgi için [kayıt ve seçim](../../extensibility/internals/registration-and-selection-source-control-vspackage.md).  
  
## <a name="large-source-control-solution-with-a-rich-feature-set"></a>Bir zengin özellik kümesiyle büyük kaynak denetimi çözümü  
 Kaynak Denetimi Eklentisi API kullanarak yeterince yakalanmaz bir zengin kaynak denetimi modeli sağlayan bir kaynak denetimi çözümü uygulamak istiyorsanız, bir kaynak denetim paketi tümleştirme yolu olarak düşünebilirsiniz. Özellikle yerine kaynak denetimi bağdaştırıcısı (kaynak denetimi eklentileri ile iletişim kurar ve bir temel kaynak denetim UI sağlar) paketini yerini alır, kaynak denetim olayları özel bir şekilde işleyebilmeniz bu kendi geçerlidir. UI denetim ve bu deneyimi korumak istiyorsanız tatmin edici bir kaynak zaten varsa [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], kaynak denetimi paket seçeneği bunu yapmanıza olanak tanır. Kaynak Denetim paketi genel değildir ve yalnızca ile kullanılmak üzere tasarlanmış [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE.  
  
 Esneklik ve daha zengin denetim Kaynak Denetim mantığı ve UI olanağı sağlayan bir kaynak denetimi çözümü uygulamak istiyorsanız, kaynak denetimi paket tümleştirme yolu tercih edebilirsiniz. Şunları yapabilirsiniz:  
  
1. Kendi kaynak denetimi VSPackage'ı kaydetmek (bkz [kayıt ve seçim](../../extensibility/internals/registration-and-selection-source-control-vspackage.md)).  
  
2. Varsayılan kaynak denetimi UI özel kullanıcı Arabirimi ile değiştirin (bkz [özel kullanıcı arabirimi](../../extensibility/internals/custom-user-interface-source-control-vspackage.md)).  
  
3. Kullanılması ve Çözüm Gezgini glif olayları işlemek için karakter belirtin (bkz [karakter denetimi](../../extensibility/internals/glyph-control-source-control-vspackage.md)).  
  
4. Sorgu düzenleme ve sorguyu kaydedin olaylarını işleme (bkz [sorgu düzenleme sorgu kaydetme](../../extensibility/internals/query-edit-query-save-source-control-vspackage.md)).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi Oluşturma](../../extensibility/internals/creating-a-source-control-plug-in.md)
