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
ms.openlocfilehash: fa04ca237134c1947b5c58b921f87f32a1ecfb16
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234300"
---
# <a name="ca1704-identifiers-should-be-spelled-correctly"></a>CA1704: Tanımlayıcılar doğru yazılmalıdır

|||
|-|-|
|TypeName|IdentifiersShouldBeSpelledCorrectly|
|CheckId|CA1704|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Tanımlayıcının adı, Microsoft yazım denetleyicisi kitaplığı tarafından tanınmayan bir veya daha fazla sözcük içeriyor. Bu kural oluşturucuları veya Get ve set özellik erişimcileri gibi özel adlandırılmış üyeleri denetlemez.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, tanımlayıcıyı belirteçlere ayrıştırır ve her belirtecin yazımını denetler. Ayrıştırma algoritması aşağıdaki dönüşümleri gerçekleştirir:

- Büyük harfler yeni bir belirteç başlatır. Örneğin, Mynameisali, "My", "Name", "The", "ali" olarak simgeleştirir.

- Birden çok büyük harf için, son büyük harf yeni bir belirteç başlatır. Örneğin, Gudüzenleyici "GUI", "Düzenleyici" olarak simgeleştirir.

- Baştaki ve sondaki kesme işaretleri kaldırılır. Örneğin, ' sender ' simgeleştirir "sender".

- Alt çizgiler bir belirtecin sonunu işaret eder ve kaldırılır. Örneğin, hello_world Token, "Hello", "World" olarak simgeleştirir.

- Gömülü ve işaretleri kaldırılır. Örneğin, & "biçim" olarak simgeleştirir.

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

Bu kural ihlalini düzeltmek için sözcüğün yazımını düzeltin veya sözcüğü özel bir sözlüğe ekleyin.

### <a name="to-add-words-to-a-custom-dictionary"></a>Özel bir sözlüğe sözcükler eklemek için

Özel sözlük XML dosyasını *CustomDictionary. xml*olarak adlandırın. Sözlüğü aracının yükleme dizinine, proje dizinine veya Kullanıcı profili altındaki araçla ilişkili dizine yerleştirin ( *%USERPROFILE%\Application Data\\...* ). Özel sözlüğün Visual Studio 'daki bir projeye nasıl ekleneceğini öğrenmek için bkz [. nasıl yapılır: Kod Analizi sözlüğünü](../code-quality/how-to-customize-the-code-analysis-dictionary.md)özelleştirin.

- Sözlük/kelimeler/tanınan yol altında ihlale neden olmaması gereken sözcükler ekleyin.

- Sözlük/kelimeler/tanınmayan yol altında ihlalin neden olması gereken sözcükler ekleyin.

- Sözlük/kelimeler/kullanım dışı yol altında, eski olarak işaretlenmek zorunda olan sözcükler ekleyin. İlgili kural konusuna [bakın CA1726: Daha fazla bilgi](../code-quality/ca1726-use-preferred-terms.md) için tercih edilen terimleri kullanın.

- Sözlük/Kısaltmalar/CasingExceptions yoluna kısaltma büyük/küçük harf kuralları için özel durumlar ekleyin.

Aşağıda bir özel sözlük dosyası yapısına örnek verilmiştir:

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

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı, yalnızca sözcüğün kasıtlı olarak yanlış yazıldığına ve sözcüğün sınırlı bir kitaplık kümesine uygulandığına karşı gizleyin. Doğru yazılmış sözcükler, yeni yazılım kitaplıkları için gerekli olan öğrenme eğrisini azaltır.

## <a name="related-rules"></a>İlgili kurallar

- [CA2204 Değişmez değerler doğru yazılmalıdır](../code-quality/ca2204-literals-should-be-spelled-correctly.md)
- [CA1703 Kaynak dizeleri doğru yazılmalıdır](../code-quality/ca1703-resource-strings-should-be-spelled-correctly.md)
- [CA1709 Tanımlayıcılar doğru şekilde yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708 Tanımlayıcılar, büyük/küçük harf bakımından farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
- [CA1707 Tanımlayıcılar alt çizgi içermemelidir](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)
- [CA1726 Tercih edilen terimleri kullanın](../code-quality/ca1726-use-preferred-terms.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Kod Analizi sözlüğünü özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md)
