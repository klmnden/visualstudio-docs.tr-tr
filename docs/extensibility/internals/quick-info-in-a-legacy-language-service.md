---
title: Eski dil hizmetinde hızlı bilgi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Quick Info, supporting in language services [managed package framework]
- IntelliSense, Quick Info
- language services [managed package framework], IntelliSense Quick Info
ms.assetid: 159ccb0b-f5d6-4912-b88b-e9612924ed5e
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6180e34135197c60276bf119ce0ac34c859b2f3d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341371"
---
# <a name="quick-info-in-a-legacy-language-service"></a>Eski Dil Hizmetinde Hızlı Bilgiler
Hızlı bilgi IntelliSense kullanıcı giriş işaretini bir tanımlayıcıda yerleştirir ve seçer bu tanımlayıcının hakkında bilgileri kaynakta gösterir **hızlı bilgi** gelen **IntelliSense** menüsü veya fare tutar tanımlayıcı imleci. Bu tanımlayıcı bilgiler görüntülenecek araç ipucu neden olur. Bu bilgiler genellikle tanımlayıcı türü oluşur. Hata ayıklama altyapısı etkin olduğunda, bu bilgiler, geçerli değer içerebilir. Dil hizmeti yalnızca, tanımlayıcıları işlerken hata ayıklama altyapısı ifade değerleri sağlar.

 Eski dil Hizmetleri bir VSPackage'ı bir parçası olarak uygulanır, ancak dil hizmeti özellikleri uygulamak için daha yeni MEF uzantıları kullanmaktır. Daha fazla bilgi için bkz: [izlenecek yol: Hızlıbilgi araç ipuçlarını görüntüleme](../../extensibility/walkthrough-displaying-quickinfo-tooltips.md).

> [!NOTE]
> Yeni bir düzenleyici API hemen kullanmaya başlamak öneririz. Bu dil hizmetinizin performansını ve yeni düzenleyici özellikleri yararlanmanıza olanak tanır.

 Yönetilen paket framework (MPF) dil hizmeti sınıfları, hızlı bilgi IntelliSense araç ipucu görüntülemek için tam destek sağlar. Yapmanız gereken tek şey görüntülenmesi ve hızlı bilgi özelliği etkinleştirmek için metin girin.

 Görüntülenecek metni çağırılarak alınır <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A> ayrıştırma neden değerini yöntemi ayrıştırıcı <xref:Microsoft.VisualStudio.Package.ParseReason>. Bu nedenle tür bilgilerini (veya her hızlı bilgi araç ipucunda görüntülenecek uygundur) elde etmek için ayrıştırıcı söyler tanımlayıcısının belirtilen konumda <xref:Microsoft.VisualStudio.Package.ParseRequest> nesne. <xref:Microsoft.VisualStudio.Package.ParseRequest> Nesnedir ne geçildi <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A> yöntemi.

 Ayrıştırıcının konumu kadar her şeyi ayrıştırma gerekir <xref:Microsoft.VisualStudio.Package.ParseRequest> tüm tanımlayıcıları türlerini belirlemek için nesne. Ardından, ayrıştırma istek konumda tanımlayıcısı ayrıştırıcı almanız gerekir. Son olarak, ayrıştırıcının için kimlikle ilişkili araç ipucu verisi geçmelidir <xref:Microsoft.VisualStudio.Package.AuthoringScope> söz konusu nesne metinden dönebilmeniz nesne <xref:Microsoft.VisualStudio.Package.AuthoringScope.GetDataTipText%2A> yöntemi.

## <a name="enabling-the-quick-info-feature"></a>Hızlı bilgi özelliğini etkinleştirme
 Hızlı bilgi özelliği etkinleştirmek için ayarlamalısınız `CodeSense` ve `QuickInfo` parametrelerinin adlı <xref:Microsoft.VisualStudio.Shell.ProvideLanguageServiceAttribute>. Bu öznitelikler <xref:Microsoft.VisualStudio.Package.LanguagePreferences.EnableCodeSense%2A> ve <xref:Microsoft.VisualStudio.Package.LanguagePreferences.EnableQuickInfo%2A> özellikleri.

## <a name="implementing-the-quick-info-feature"></a>Hızlı bilgi özelliği uygulama
 <xref:Microsoft.VisualStudio.Package.ViewFilter> Sınıfı hızlı bilgi IntelliSense işlemi işler. Zaman <xref:Microsoft.VisualStudio.Package.ViewFilter> sınıfı alır <xref:Microsoft.VisualStudio.VSConstants.VSStd2KCmdID> komutu, sınıf çağrıları <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A> yöntemi ayrıştırma nedeni ile <xref:Microsoft.VisualStudio.Package.ParseReason> ve zaman giriş işaretinin konumunu <xref:Microsoft.VisualStudio.VSConstants.VSStd2KCmdID> komut gönderildi. <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A> Yöntemi ayrıştırıcı sonra belirtilen konuma kadar kaynak ayrıştırma ve ardından hızlı bilgi araç ipucunda görüntülenecek öğeleri belirlemek için verilen konuma tanımlayıcısı ayrıştırılamıyor.

 Çoğu Çözümleyicileri tüm kaynak dosyasının ilk bir ayrıştırma yapın ve sonuçları bir ayrıştırma ağacı içinde depolamak. Tam ayrıştırma zaman taşınan <xref:Microsoft.VisualStudio.Package.ParseReason> geçirilir <xref:Microsoft.VisualStudio.Package.LanguageService.ParseSource%2A> yöntemi. Diğer türleri ayrıştırma, ayrıştırma ağacı istenen bilgileri edinmek için daha sonra kullanabilirsiniz.

 Örneğin, ayrıştırma neden değerini <xref:Microsoft.VisualStudio.Package.ParseReason> kaynak konumundaki tanımlayıcısını bulmak ve arayın tür bilgilerini almak için ayrıştırma ağacı. Bu tür bilgiler geçirilerek <xref:Microsoft.VisualStudio.Package.AuthoringScope> sınıfı ve tarafından döndürülen <xref:Microsoft.VisualStudio.Package.AuthoringScope.GetDataTipText%2A> yöntemi.