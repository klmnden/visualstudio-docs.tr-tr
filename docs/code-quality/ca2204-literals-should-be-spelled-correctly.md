---
title: 'CA2204: Harfler doğru yazılmalıdır'
ms.date: 03/28/2018
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 62ad30516720a843d519a9e514cd325a957b3cff
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55017129"
---
# <a name="ca2204-literals-should-be-spelled-correctly"></a>CA2204: Harfler doğru yazılmalıdır

|||
|-|-|
|TypeName|LiteralsShouldBeSpelledCorrectly|
|CheckId|CA2204|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Bir sabit dize yerelleştirilebilir parametresi veya yerelleştirilebilir bir özellik için bir bağımsız değişken olarak geçirilir ve dizesi Microsoft Yazım kitaplığı tarafından tanınmayan bir veya daha fazla sözcük içerir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, bir parametre veya bir özellik için bir değer olarak geçirilen bir sabit dize denetler veya aşağıdaki durumlarda daha fazla doğrudur:

- <xref:System.ComponentModel.LocalizableAttribute> Özniteliği parametre ya da özelliğin true.

- Parametresi veya özellik adı "Metin", "İleti" veya "Başlık" içeriyor.

- Geçirilen dize değişkeninin adı bir <xref:System.Console.Write%2A> veya <xref:System.Console.WriteLine> yöntemdir "value" veya "biçim".

Bu kural sabit dizesini bileşik sözcüklerin kelimelere, ayrıştırır ve her sözcük veya belirtecin yazımını denetler. Ayrıştırma algoritma hakkında daha fazla bilgi için bkz. [CA1704: Tanımlayıcıları yazıldığından](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md).

## <a name="language"></a>Dil

Yazım denetleyicisi şu anda yalnızca İngilizce tabanlı kültürü sözlükleri karşı denetler. Proje dosyası projenize kültürü ekleyerek değiştirebilirsiniz **CodeAnalysisCulture** öğesi.

Örneğin:

```xml
<Project ...>
  <PropertyGroup>
    <CodeAnalysisCulture>en-AU</CodeAnalysisCulture>
```

> [!IMPORTANT]
> İngilizce-tabanlı bir kültür dışında bir kültürü ayarlarsanız, bu kod çözümleme kural sessiz bir şekilde devre dışı bırakıldı.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için sözcük yazımını düzeltin ya da sözcüğü bir özel sözlüğüne ekleyin. Özel sözlükler kullanma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md).

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın. Doğru bir şekilde yazılmış kelimeler yeni yazılım kitaplıkları için gereken öğrenme eğrisini azaltır.

## <a name="related-rules"></a>İlgili kuralları

- [CA1704: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1704-identifiers-should-be-spelled-correctly.md)
- [CA1703: Kaynak dizeler doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)