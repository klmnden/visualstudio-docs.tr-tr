---
title: 'CA1704: Tanımlayıcılar doğru yazılmalıdır'
ms.date: 03/28/2018
ms.topic: reference
f1_keywords:
- CA1704
- IdentifiersShouldBeSpelledCorrectly
helpviewer_keywords:
- CA1704
- IdentifiersShouldBeSpelledCorrectly
ms.assetid: f2c7a44d-1690-44ca-9cd0-681b04b12b2a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8dbfc8081f980b7b9e978da782f1627a88a716a3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62809414"
---
# <a name="ca1704-identifiers-should-be-spelled-correctly"></a>CA1704: Tanımlayıcılar doğru yazılmalıdır

|||
|-|-|
|TypeName|IdentifiersShouldBeSpelledCorrectly|
|CheckId|CA1704|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tanımlayıcı ad Microsoft Yazım kitaplığı tarafından tanınmayan bir veya birkaç sözcük içerir. Bu kural olmayan oluşturucular veya özel adlı üye alma gibi denetleyin ve özellik erişimcileri ayarlayın.

## <a name="rule-description"></a>Kural açıklaması

Bu kural tanımlayıcısı belirteçlere ayrıştırmak ve her belirtecin yazımını denetler. Ayrıştırma algoritma şu dönüşümleri gerçekleştirir:

- Yeni bir belirteç harfle başlatın. Örneğin, MyNameIsJoe "My", "Name", "Is", "Joe" tokenizes.

- Birden çok büyük harf, yeni bir belirteç son büyük harfle başlar. Örneğin, "GUI", "Düzenleyicisi" GUIEditor tokenizes.

- Baştaki ve sondaki kesme kaldırılır. Örneğin, "sender" için 'sender' tokenizes.

- Alt çizgi, bir belirteç sonunu belirtmek ve kaldırılır. Örneğin, "Hello" Hello_world tokenizes "world".

- Katıştırılmış kodlarına kaldırılır. Örneğin, & mat tokenizes "biçimlendirmek için".

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

Bu kural ihlalini düzeltmek için sözcük yazımını düzeltin ya da sözcüğü bir özel sözlüğüne ekleyin.

### <a name="to-add-words-to-a-custom-dictionary"></a>Özel bir sözlüğe sözcüklerin eklemek için

Özel sözlük XML dosya adı *CustomDictionary.xml*. Sözlük proje dizinine aracının yükleme dizininde veya kullanıcı profili altındaki aracı ile ilişkili dizine yerleştirin (*%USERPROFILE%\Application veri\\...* ). Visual Studio'da bir proje özel sözlük ekleme hakkında bilgi edinmek için [nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md).

- Sözlük/sözcükleri/Recognized yolunda bir ihlali oluşmamalıdır sözcükler ekleyin.

- Sözlük/sözcükleri/tanınmayan yolunda bir ihlali neden olmamalıdır sözcükler ekleyin.

- Sözlük/sözcükleri/kullanım dışı yolunda geçersiz olarak işaretlenmiş sözcükler ekleyin. İlişkili kural konusuna [CA1726: Tercih edilen terimleri kullanın](../code-quality/ca1726-use-preferred-terms.md) daha fazla bilgi için.

- Sözlük/kısaltmalar/CasingExceptions yoluna kısaltma büyük/küçük harf kuralları için özel durumlar ekleyin.

Özel sözlük dosyası yapısı örneği verilmiştir:

```xml
<Dictionary>
   <Words>
      <Unrecognized>
         <Word>cb</Word>
      </Unrecognized>
      <Recognized>
         <Word>stylesheet</Word>
         <Word>GotDotNet</Word>
      </Recognized>
      <Deprecated>
         <Term PreferredAlternate="EnterpriseServices">ComPlus</Term>
      </Deprecated>
   </Words>
   <Acronyms>
      <CasingExceptions>
         <Acronym>CJK</Acronym>
         <Acronym>Pi</Acronym>
      </CasingExceptions>
   </Acronyms>
</Dictionary>
```

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan bir uyarıyı yalnızca bilerek yanlış yazılmış bir sözcüktür ve sınırlı bir kitaplık kümesi için Word'ün uyguladığı gösterme. Doğru bir şekilde yazılmış kelimeler yeni yazılım kitaplıkları için gerekli olan öğrenme eğrisini azaltır.

## <a name="related-rules"></a>İlgili kuralları

- [CA2204: Değişmez değerler doğru yazılmalıdır](../code-quality/ca2204-literals-should-be-spelled-correctly.md)
- [CA1703: Kaynak dizeler doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)
- [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
- [CA1707: Tanımlayıcılar alt çizgi içermemelidir](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)
- [CA1726: Tercih edilen terimleri kullanın](../code-quality/ca1726-use-preferred-terms.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Kod çözümleme dizinini özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md)
