---
title: 'CA1720: Tanımlayıcılar tür adları içermemelidir'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1720
- IdentifiersShouldNotContainTypeNames
helpviewer_keywords:
- IdentifiersShouldNotContainTypeNames
- CA1720
ms.assetid: c95ee48f-f23a-45f0-ac9e-a3c1ecfabdea
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d0eb7cfeb2271b7ed01f59d4892987fb2ef72808
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546576"
---
# <a name="ca1720-identifiers-should-not-contain-type-names"></a>CA1720: Tanımlayıcılar tür adları içermemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotContainTypeNames|
|CheckId|CA1720|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Üye bir parametre adını veri türü adı içerir.

-veya-

Bir üyenin adını bir dile bağlı veri türü adı içerir.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen üyeleri görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Parametreleri ve üyelerin adları, daha iyi geliştirme araçları tarafından sağlanan bekleniyor, türü tanımlamak üzere daha anlamları iletişim kurmak için kullanılır. Bir veri türü adı kullanılmalıdır, üyelerinin adları için dile özgü bir yerine dilden bağımsız bir ad kullanın. Örneğin, yerine, C# tür adı `int`, dilden bağımsız veri türü adını `Int32`.

Parametre ya da üye adını ayrık her belirteç aşağıdaki dile bağlı veri türü adların büyük küçük harf duyarlı bir şekilde denetlenir:

- Bool
- WChar
- Int8
- UInt8
- Kısa
- UShort
- int
- UInt
- Tamsayı
- Uınteger
- Uzun
- ULong
- İşaretsiz
- İmzalı
- Float
- float32
- float64

Ayrıca, bir parametre adlarını aşağıdaki dilden bağımsız veri türü adları ayrıca büyük küçük harf duyarlı bir şekilde denetlenir:

- Nesne
- Obj
- Boole değeri
- Char
- Dize
- SByte
- Bayt
- UByte
- Int16
- UInt16
- Int32
- UInt32
- Int64
- UInt64
- IntPtr
- PTR
- İşaretçi
- UInptr
- UPtr
- UPointer
- Tek
- Çift
- Ondalık
- Guid

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

**Bir parametre karşı harekete varsa:**

Parametre adını veri türü tanımlayıcısı, daha iyi anlamını açıklayan bir terim ya da 'value' gibi daha genel bir terim ile değiştirin.

**Üye karşı harekete varsa:**

Bunun anlamı, bir dil bağımsız eşdeğeriyle ya da 'value' gibi daha genel bir terim daha iyi açıklayan bir terim ile dile bağlı veri türü tanımlayıcısı ' üye adını değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Parametre ve üye adları türüne göre ara sıra kullanılmasını uygun olabilir. Ancak, hiçbir bilinen yeni geliştirme için senaryolar ortaya burada bu kuraldan bir uyarıyı bastırmak. Daha önce sevk kitaplıkları için bu kuraldan bir uyarıyı bastırmak olabilir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1720.api_surface = private, internal
```

Bu kategoride (adlandırma), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="related-rules"></a>İlgili kuralları

- [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
- [CA1707: Tanımlayıcılar alt çizgi içermemelidir](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)
- [CA1719: Parametre adları üye adlarıyla eşleşmemelidir](../code-quality/ca1719-parameter-names-should-not-match-member-names.md)