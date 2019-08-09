---
title: Özel bir konak kullanarak metin şablonlarını işleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- text templates, in application or VS extension
- text templates, custom directive hosts
ms.assetid: affa3296-854d-47d6-9685-285f6d9ba5dc
caps.latest.revision: 35
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 1c8f306315ad236843b6fcd5551d9aed13c26a92
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68871794"
---
# <a name="processing-text-templates-by-using-a-custom-host"></a>Bir Özel Ana Bilgisayar kullanarak Metin Şablonlarını İşleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

*Metin şablonu dönüştürme* işlemi, girdi olarak bir *metin şablonu* dosyası alır ve çıktı olarak bir metin dosyası üretir. Metin dönüştürme altyapısını bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] uzantıdan veya yüklü bir makinede [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] çalışan tek başına bir uygulamadan çağırabilirsiniz. Ancak, bir *metin şablonu oluşturma Konağı*sağlamanız gerekir. Bu sınıf, derlemeler ve ekleme dosyaları gibi kaynakları bularak ve çıktı ve hata iletilerini işleme alarak şablonu ortama bağlar.

> [!TIP]
> İçinde [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]çalışacak bir paket veya uzantı yazıyorsanız, kendi ana bilgisayarınızı yazmak yerine metin şablonu oluşturma hizmetini kullanmayı göz önünde bulundurun. Daha fazla bilgi için bkz. [BIR vs uzantısında metin dönüştürmeyi çağırma](../modeling/invoking-text-transformation-in-a-vs-extension.md).

> [!NOTE]
> Metin şablonu dönüştürmelerinin sunucu uygulamalarında kullanılması önerilmez. Metin şablonu dönüştürmelerinin tek bir iş parçacığı dışında kullanılması önerilmez. Bunun nedeni, metin şablonu oluşturma motorunun şablonları çevirmek, derlemek ve yürütmek için tek bir AppDomain öğesini yeniden kullanmasıdır. Çevrilen kod, iş parçacığı açısından güvenli olmak üzere tasarlanmamıştır. Altyapı, bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] projede, tasarım zamanında olduğu gibi dosyaları işlemek için tasarlanmıştır.
>
> Çalışma zamanı uygulamaları için, önceden işlenmiş metin şablonlarını kullanmayı düşünün: bkz. [T4 metin şablonlarıyla çalışma zamanı metin oluşturma](../modeling/run-time-text-generation-with-t4-text-templates.md).

 Uygulamanız, derleme zamanında sabitlenmiş bir grup şablon kullanıyorsa, Önceden İşlenmiş Metin Şablonlarının kullanılması daha kolaydır. Uygulamanız yüklü olmayan bir makinede [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] çalışıyorsa, bu yaklaşımı de kullanabilirsiniz. Daha fazla bilgi için bkz. [T4 metin şablonlarıyla çalışma zamanı metin üretimi](../modeling/run-time-text-generation-with-t4-text-templates.md).

## <a name="executing-a-text-template-in-your-application"></a>Uygulamanızda Metin Şablonu Yürütme
 Bir metin şablonunu yürütmek için ProcessTemplate yöntemini <xref:Microsoft.VisualStudio.TextTemplating.Engine?displayProperty=fullName>çağırın:

```
using Microsoft.VisualStudio.TextTemplating;
...
Engine engine = new Engine();
string output = engine.ProcessTemplate(templateString, host);
```

 Uygulamanızın şablonu bularak sağlaması ve çıktı ile işlem yapması gerekir.

 Parametresinde, ITextTemplatingEngineHost uygulayan bir sınıf sağlamanız gerekir. [](/previous-versions/visualstudio/visual-studio-2012/bb126505(v=vs.110)) `host` Bu, Motor tarafından geri çağrılır.

 Ana bilgisayar hataları günlüğe kaydedebilmeli, derleme ve ekleme dosyalarına yapılan başvuruları çözümleyebilmeli, şablonun yürütülebileceği bir Uygulama Etki Alanı sağlayabilmeli ve her yönerge için uygun işlemciyi çağırabilmelidir.

 <xref:Microsoft.VisualStudio.TextTemplating.Engine?displayProperty=fullName>, **Microsoft. VisualStudio.\*textşablon oluşturma içinde tanımlanmıştır. 0. dll**ve [ITextTemplatingEngineHost](/previous-versions/visualstudio/visual-studio-2012/bb126505(v=vs.110)) , **Microsoft. VisualStudio. Textşablon oluşturma. Interfaces içinde tanımlanmıştır.\* 0. dll**.

## <a name="in-this-section"></a>Bu Bölümde
 [İzlenecek yol: Özel metin şablonu ana bilgisayarı](../modeling/walkthrough-creating-a-custom-text-template-host.md) oluşturma, metin şablonu işlevselliğinin dışında [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]kullanılabilir hale getiren bir özel metin şablonu ana bilgisayarı oluşturmayı gösterir.

## <a name="reference"></a>Başvuru
 [ITextTemplatingEngineHost](/previous-versions/visualstudio/visual-studio-2012/bb126505(v=vs.110))

## <a name="related-sections"></a>İlgili Bölümler
 [Metin şablonu dönüştürme işlemi](../modeling/the-text-template-transformation-process.md) Metin dönüşümünün nasıl çalıştığını ve hangi parçaları özelleştirebileceğinizi açıklar.

 [Özel T4 metin şablonu yönerge Işlemcileri oluşturma](../modeling/creating-custom-t4-text-template-directive-processors.md) Metin şablonu yönerge işlemcilere genel bakış sağlar.
