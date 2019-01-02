---
title: Intellitest giriş
ms.date: 05/02/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- IntelliTest, Get started
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 41fd7b7b32a2e81ec2a217a54a6220cbafb38668
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53952930"
---
# <a name="get-started-with-microsoft-intellitest"></a>Microsoft IntelliTest ile çalışmaya başlama

* Intellitest ile ilk kez varsa:
  * İzleme [kanal 9 videosu](https://channel9.msdn.com/Shows/Visual-Studio-Toolbox/Intellitest)
  * Bu okuma [MSDN dergisi genel bakış](https://msdn.microsoft.com/magazine/dn904672.aspx)
  * Okuma bizim [belgeleri](../../test/generate-unit-tests-for-your-code-with-intellitest.md)
* Sorularınızı sorabilirsiniz [Stack Overflow](http://stackoverflow.com/questions/tagged/intellitest)
* Bu başvuru el ile geri kalanını okuyun
* Hızlı başvuru için bu sayfayı yazdır

## <a name="important-attributes"></a>Önemli öznitelikleri

* [PexClass](attribute-glossary.md#pexclass) işaretler türünü içeren **yerleştirin**
* [PexMethod](attribute-glossary.md#pexmethod) işaretleri bir **yerleştirin**
* [PexAssumeNotNull](attribute-glossary.md#pexassumenotnull) null olmayan bir parametre işaretler

```csharp
using Microsoft.Pex.Framework;

[..., PexClass(typeof(Foo))]
public partial class FooTest {
    [PexMethod]
    public void Bar([PexAssumeNotNull]Foo target, int i) {
        target.Bar(i);
    }
}
```

* [PexAssemblyUnderTest](attribute-glossary.md#pexassemblyundertest) bağlayan bir test projesi için bir proje
* [PexInstrumentAssembly](attribute-glossary.md#pexinstrumentassemblyattribute) aracına bir derleme belirtir

```csharp
[assembly: PexAssemblyUnderTest("MyAssembly")] // also instruments "MyAssembly"
[assembly: PexInstrumentAssembly("Lib")]
```

## <a name="helper-classes"></a> Önemli statik yardımcı sınıfları

* [PexAssume](static-helper-classes.md#pexassume) (giriş filtreleme) varsayımlar değerlendirir
* [PexAssert](static-helper-classes.md#pexassert) onaylar değerlendirir
* [PexChoose](static-helper-classes.md#pexchoose) yeni seçenekleri (ek girdileri) oluşturur.
* [PexObserve](static-helper-classes.md#pexobserve) dinamik değerler için üretilen testler günlüğe kaydeder.

```csharp
[PexMethod]
void StaticHelpers(Foo target) {
    PexAssume.IsNotNull(target);

    int i = PexChoose.Value<int>("i");
    string result = target.Bar(i);

    PexObserve.ValueForViewing<string>("result", result);
    PexAssert.IsNotNull(result);
}
```

## <a name="got-feedback"></a>Geri bildirim var mı?

Fikirlerinizi gönderin ve özellik istekleri [Geliştirici topluluğu](https://developercommunity.visualstudio.com/content/idea/post.html?space=8).
