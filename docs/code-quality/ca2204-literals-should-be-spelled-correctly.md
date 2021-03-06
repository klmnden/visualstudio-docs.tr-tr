---
title: 'CA2204: Harfler doğru yazılmalıdır'
ms.date: 03/28/2018
ms.topic: reference
f1_keywords:
- Literals should be spelled correctly
- CA2204
- LiteralsShouldBeSpelledCorrectly
helpviewer_keywords:
- CA2204
ms.assetid: b0bbcbb6-c92d-4c14-8ef7-9c8b38c791a6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6763fd9f8999bd590511026f6571db6a747c43bc
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231852"
---
# <a name="ca2204-literals-should-be-spelled-correctly"></a>CA2204: Harfler doğru yazılmalıdır

|||
|-|-|
|TypeName|LiteralsShouldBeSpelledCorrectly|
|CheckId|CA2204|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir sabit dize, yerelleştirilebilir bir parametre veya yerelleştirilebilir bir özelliğe bağımsız değişken olarak geçirilir ve dize, Microsoft yazım denetleyicisi kitaplığı tarafından tanınmayan bir veya daha fazla sözcük içerir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, aşağıdaki durumlardan biri veya daha fazlası doğru olduğunda bir parametreye veya özelliğe değer olarak geçirilen bir sabit dize denetler:

- Parametrenin veya özelliğin özniteliği true olarak ayarlandı. <xref:System.ComponentModel.LocalizableAttribute>

- Parametre veya özellik adı "metin", "Ileti" veya "başlık" içerir.

- <xref:System.Console.Write%2A> Or<xref:System.Console.WriteLine> yöntemine geçirilen dize değişkeninin adı "Value" ya da "Format" değeridir.

Bu kural, değişmez dizeyi sözcük olarak ayrıştırır, bileşik sözcükleri simgeleştiriler ve her sözcüğün veya belirtecin yazımını denetler. Ayrıştırma algoritması hakkında daha fazla bilgi için bkz [. CA1704: Tanımlayıcılar doğru](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)yazılmalıdır.

## <a name="language"></a>Dil

Yazım denetleyicisi şu anda yalnızca Ingilizce tabanlı kültür sözlüklerine karşı kontrol eder. **Kod analysisculture** öğesini ekleyerek proje dosyasındaki projenizin kültürünü değiştirebilirsiniz.

Örneğin:

```xml
<Project ...>
  <PropertyGroup>
    <CodeAnalysisCulture>en-AU</CodeAnalysisCulture>
```

> [!IMPORTANT]
> Kültürü, Ingilizce tabanlı kültür dışında bir şeye ayarlarsanız, bu kod analizi kuralı sessizce devre dışıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini düzeltmek için sözcüğün yazımını düzeltin veya sözcüğü özel bir sözlüğe ekleyin. Özel sözlüklerin nasıl kullanılacağı hakkında bilgi için bkz [. nasıl yapılır: Kod Analizi sözlüğünü](../code-quality/how-to-customize-the-code-analysis-dictionary.md)özelleştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Doğru yazılmış sözcükler, yeni yazılım kitaplıkları için gereken öğrenme eğrisini azaltır.

## <a name="related-rules"></a>İlgili kurallar

- [CA1704 Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)
- [CA1703 Kaynak dizeleri doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)