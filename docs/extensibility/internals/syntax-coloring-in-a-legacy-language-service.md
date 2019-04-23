---
title: Eski dil hizmetinde söz dizimi renklendirmesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- syntax coloring
- language services, syntax coloring
ms.assetid: f65ff67e-8c20-497a-bebf-5e2a5b5b012f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e193f5c8363cda4e3519df45d001a1972865813e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60057770"
---
# <a name="syntax-coloring-in-a-legacy-language-service"></a>Eski Dil Hizmetinde Söz Dizimi Renklendirmesi

Visual Studio renklendirme hizmet dilinin öğelerini tanımlamak ve bunları belirtilen bir Düzenleyicisi renkleri görüntülemek için kullanır.

## <a name="colorizer-model"></a>Renklendirici modeli
 Dil hizmeti uygulayan <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer> ardından düzenleyiciler tarafından kullanılan arabirim. Bu uygulama, aşağıdaki çizimde gösterildiği gibi dil hizmeti ayrı bir nesneden geçerlidir:

 ![SVC Renklendirici grafiği](../../extensibility/internals/media/figlgsvccolorizer.gif)

> [!NOTE]
>  Hizmet renklendirme söz dizimi renklendirme metin için genel Visual Studio mekanizması ayrıdır. Genel hakkında daha fazla bilgi için [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] renklendirme, destekleyici mekanizması bkz [kullanarak yazı tipleri ve renkler](../../extensibility/using-fonts-and-colors.md).

 Renklendirici yanı sıra özel renklendirilebilir öğeler sağlayan advertising tarafından düzenleyici tarafından kullanılan özel renklendirilebilir öğeler dil hizmeti sağlayabilirsiniz. Bunu uygulayarak yapabilirsiniz <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems> arabirimi uygulayan aynı nesne üzerinde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo> arabirimi. Düzenleyici çağırdığında, özel renklendirilebilir öğeler sayısını döndürür. <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems.GetItemCount%2A> Yöntemi Düzenleyicisi çağırdığında, ayrı bir özel renklendirilebilir öğe döndürür <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems.GetColorableItem%2A> yöntemi.

 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems.GetColorableItem%2A> Yöntemini uygulayan bir nesne döndürür <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorableItem> arabirimi. Dil hizmeti 24-bit ya da yüksek renk değerleri destekliyorsa, uygulamalıdır <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiColorItem> arabirimi aynı nesne üzerinde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorableItem> arabirimi.

## <a name="how-a-vspackage-uses-a-language-service-colorizer"></a>Dil hizmeti Renklendirici bir VSPackage'ı kullanma

1. VSPackage'ı VSPackage'ı, aşağıdakileri yapmak için dil hizmeti gerektirir uygun dil hizmeti almanız gerekir:

    1. Bir nesneyi uygulama kullanmak <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> renklendirilmiş için metin almak için arabirim.

         Metin, uygulayan bir nesne kullanarak genellikle görüntülenir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> arabirimi.

    2. Dil hizmeti VSPackage GUID dil hizmeti için hizmet sağlayıcısı sorgulayarak alın. Dil Hizmetleri kayıt defterinde dosya uzantısı ile tanımlanır.

    3. Dil hizmeti ile ilişkilendirme <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> çağırarak kendi <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer.SetLanguageServiceID%2A> yöntemi.

2. VSPackage'ı şimdi alabilir ve Renklendirici nesnesini şu şekilde kullanın:

    > [!NOTE]
    > Çekirdek Düzenleyicisi'ni VSPackage'ları, bir dil hizmetin Renklendirici nesneleri açıkça elde gerekmez. Çekirdek Düzenleyici örneği uygun dil hizmeti edinir hemen sonra burada gösterilen tüm renklendirme görevleri gerçekleştirir.

    1. Uygulayan dil hizmetin Renklendirici nesnesi elde <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer>, ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer2> çağırarak arabirimleri <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo.GetColorizer%2A> dil hizmetin metodunda <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo> nesne.

    2. Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> belirli bir aralık metin Renklendirici bilgileri almak için yöntemi.

         <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> renklendirilmiş metin aralığı her karakter için bir değer dizisi döndürür. Çekirdek düzenleyici tarafından tutulan varsayılan renklendirilebilir öğesi listesinden veya dil hizmeti kendisi tarafından tutulan bir özel renklendirilebilir öğesi listesinden bir renklendirilebilir öğesi liste içine dizinler değerlerdir.

    3. Tarafından döndürülen renklendirme bilgileri <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> seçili metni görüntülemek için yöntemi.

> [!NOTE]
>  Dil hizmeti Renklendirici kullanmanın yanı sıra bir VSPackage mekanizması renklendirme genel amaçlı Visual Studio metin de kullanabilirsiniz. Bu mekanizması hakkında daha fazla bilgi için bkz. [kullanarak yazı tipleri ve renkler](../../extensibility/using-fonts-and-colors.md).

## <a name="in-this-section"></a>Bu Bölümde
- [Söz Dizimi Renklendirmesi Uygulama](../../extensibility/internals/implementing-syntax-coloring.md)

 Bir düzenleyici bir dil hizmetin söz dizimi renklendirme ve dil hizmeti gerekir sözdizimini desteklemek üzere uygulama renklendirme nasıl eriştiğini açıklanır.

- [Nasıl yapılır: Yerleşik renklendirilebilir öğeleri kullanma](../../extensibility/internals/how-to-use-built-in-colorable-items.md)

 Dil hizmeti yerleşik renklendirilebilir öğeleri kullanma işlemini gösterir.

- [Özel Renklendirilebilir Öğeler](../../extensibility/internals/custom-colorable-items.md)

 Özel renklendirilebilir öğeler uygulamak nasıl ele alınmaktadır.

## <a name="see-also"></a>Ayrıca Bkz.

- [Yazı Tiplerini ve Renkleri Kullanma](../../extensibility/using-fonts-and-colors.md)