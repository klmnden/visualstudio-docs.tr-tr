---
title: Söz dizimi renklendirmesi uygulama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- syntax coloring, implementing
- editors [Visual Studio SDK], colorizing text
- text, colorizing in editors
ms.assetid: 96e762ca-efd0-41e7-8958-fda4897c8c7a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3e82246a750c26881a055e372baa7d5eb0386952
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596094"
---
# <a name="implementing-syntax-coloring"></a>Söz Dizimi Renklendirmesi Uygulama
Söz dizimi renklendirme dil hizmetinin sağladığı, ayrıştırıcının metin satırı renklendirilebilir öğeleri bir diziye dönüştürür ve belirteç türleri bu renklendirilebilir öğeleri karşılık gelen döndürür. Ayrıştırıcının renklendirilebilir öğeler listesine ait belirteç türleri döndürmeniz gerekir. [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] renklendirilebilir her öğe için uygun belirteç türü Renklendirici nesne tarafından atanan öznitelikler göre kod penceresinde görüntüler.

 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Bir Ayrıştırıcı arabirim belirtmiyor ve ayrıştırıcı uygulamasıdır tamamen size bağlıdır. Bununla birlikte, varsayılan bir ayrıştırıcı uygulama, Visual Studio dil paketini projeye sağlanır. Yönetilen kod için yönetilen paket çerçevesini (MPF), metin renklendirmesi için tam destek sağlar.

 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Sözdizimi renklendirme uygulamak için en yeni yolu hakkında daha fazla bilgi için bkz: [izlenecek yol: Metin vurgulama](../../extensibility/walkthrough-highlighting-text.md).

> [!NOTE]
>  Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.

## <a name="steps-followed-by-an-editor-to-colorize-text"></a>Metin renklendirmek için bir düzenleyici tarafından izlenen adımları

1.  Çağırarak Renklendirici düzenleyiciyi alır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo.GetColorizer%2A> metodunda <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo> nesne.

2.  Düzenleyici çağrıları <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.GetStateMaintenanceFlag%2A> Renklendirici Renklendirici dışında tutulması gerektiğini, her satırın durum gerekip gerekmediğini belirlemek için yöntemi.

3.  Düzenleyici Renklendirici Renklendirici dışında tutulması durumuna gerektiriyorsa, çağıran <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.GetStartState%2A> ilk satırı durumunu almak için yöntemi.

4.  Arabellekteki her satır için düzenleyici çağırır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> yöntemi aşağıdaki adımları gerçekleştirir:

    1.  Metin satırının metni belirteçlere dönüştürmek için bir tarayıcı geçirilir. Her simge, belirteç metni ve belirteç türü belirtir.

    2.  Belirteç türü renklendirilebilir öğeleri listesini bir dizine dönüştürülür.

    3.  Belirteç bilgileri sağlayacak şekilde dizinin her öğesi satırında bir karaktere karşılık gelen bir dizide doldurmak için kullanılır. Dizide depolanan renklendirilebilir öğeler listeye dizinler değerlerdir.

    4.  Her satırı için satır sonunda durumu döndürülür.

5.  Düzenleyici Renklendirici sürdürülmesi durumuna gerektiriyorsa, bu satırı durumunu önbelleğe alır.

6.  Öğesinden döndürülen bilgileri kullanarak metin satırının Düzenleyicisi işler <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> yöntemi. Bu, aşağıdaki adımları gerektirir:

    1.  Satırdaki her karakter için renklendirilebilir öğe dizini alın.

    2.  Varsayılan renklendirilebilir öğeleri kullanma, düzenleyicinin renklendirilebilir öğeleri listesi erişin.

    3.  Aksi takdirde, dil hizmetin çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems.GetColorableItem%2A> renklendirilebilir öğesi elde etmek için yöntemi.

    4.  Bilgileri renklendirilebilir öğesinde ekranını metin işlemek için kullanın.

## <a name="managed-package-framework-colorizer"></a>Yönetilen paket Framework Renklendirici
 Yönetilen paket çerçevesini (MPF) bir Renklendirici uygulamak için gereken tüm sınıflar sağlar. Dil hizmeti sınıfınıza alması gerektiğini <xref:Microsoft.VisualStudio.Package.LanguageService> sınıfı ve gerekli yöntemleri uygular. Uygulayarak, bir tarayıcı ve ayrıştırıcı sağlamalısınız <xref:Microsoft.VisualStudio.Package.IScanner> arabirim ve arabirimden örneğini döndürmesi <xref:Microsoft.VisualStudio.Package.LanguageService.GetScanner%2A> yöntemi (içinde uygulanması gereken yöntemlerden birini <xref:Microsoft.VisualStudio.Package.LanguageService> sınıfı). Daha fazla bilgi için [eski dil hizmetinde söz dizimi renklendirme](../../extensibility/internals/syntax-colorizing-in-a-legacy-language-service.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [Nasıl yapılır: Yerleşik renklendirilebilir öğeleri kullanma](../../extensibility/internals/how-to-use-built-in-colorable-items.md)
- [Özel Renklendirilebilir Öğeler](../../extensibility/internals/custom-colorable-items.md)
- [Eski Dil Hizmeti Geliştirme](../../extensibility/internals/developing-a-legacy-language-service.md)
- [Eski Dil Hizmetinde Söz Dizimi Renklendirmesi](../../extensibility/internals/syntax-colorizing-in-a-legacy-language-service.md)