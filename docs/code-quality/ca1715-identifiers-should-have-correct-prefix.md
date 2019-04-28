---
title: 'CA1715: Tanımlayıcılar doğru ön eke sahip olmalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1715
- IdentifiersShouldHaveCorrectPrefix
helpviewer_keywords:
- IdentifiersShouldHaveCorrectPrefix
- CA1715
ms.assetid: cf45f8df-6855-4cb6-a4e2-7cfed714cf2f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: b794eb7c7a258a843763b2c68902000031c17eb3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62807153"
---
# <a name="ca1715-identifiers-should-have-correct-prefix"></a>CA1715: Tanımlayıcılar doğru ön eke sahip olmalıdır

|||
|-|-|
|TypeName|IdentifiersShouldHaveCorrectPrefix|
|CheckId|CA1715|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|-Arabirimlerde tetiklendiğinde kesiliyor.<br /><br /> Bölünemez - genel tür parametrelerinde oluştuğunda.|

## <a name="cause"></a>Sebep

Bir arabirimin adını bir büyük harf 'ı' başlamıyor.

-veya-

Adı bir [genel tür parametresi](/dotnet/csharp/programming-guide/generics/generic-type-parameters) bir türün veya yöntemin bir büyük harf ile 'T başlamıyor '.

Varsayılan olarak, bu kural yalnızca dışarıdan görünebilir arabirimler, türleri ve yöntemleri görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Kural gereği, programlama öğelerinin adlarını belirli bir önek ile başlayın.

Arabirim adına 'I' başka bir büyük harf tarafından izlenen büyük harf ile başlamalıdır. Bu kural ihlalleri için arabirim adına 'MyInterface' ve 'IsolatedInterface' gibi bildirir.

Genel tür parametresi adlarına başlamalıdır bir büyük harf ile 'T' ve isteğe bağlı olarak başka bir büyük harf tarafından izlenebilir. Bu kural ihlalleri için 'V' ve 'Type' gibi genel tür parametre adları bildirir.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), bu kural, kodun hangi kısımlarının çözümler yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

### <a name="single-character-type-parameters"></a>Tek karakterli tür parametreleri

Bu kuralın tek karakterli tür parametreleri hariç gerekip gerekmediğini yapılandırabilirsiniz. Örneğin, belirtmek için bu kural *barındırmamalıdır* tek karakterli tür parametreleri çözümlemek, projenize bir .editorconfig dosyasında şu anahtar-değer çiftleri birini ekleyin:

```
# Package version 2.9.0 and later
dotnet_code_quality.CA1715.exclude_single_letter_type_parameters = true

# Package version 2.6.3 and earlier
dotnet_code_quality.CA2007.allow_single_letter_type_parameters = true
```

> [!NOTE]
> Bu kural adlı bir tür parametresi için hiçbir zaman tetikler `T`, örneğin, `Collection<T>`.

### <a name="api-surface"></a>API yüzeyi

Hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1715.api_surface = private, internal
```

Bu kategoride (adlandırma), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Tanımlayıcı doğru önek yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="interface-naming-example"></a>Adlandırma örnek arabirimi

Aşağıdaki kod parçacığı yanlış adlandırılmış bir arabirimi gösterir:

[!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_1.cpp)]
[!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_1.vb)]
[!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_1.cs)]

Aşağıdaki kod parçacığı, arabirimi 'I' koyarak önceki ihlali giderir:

[!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_2.cs)]
[!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_2.cpp)]
[!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_2.vb)]

## <a name="type-parameter-naming-example"></a>Tür parametresi adlandırma örneği

Aşağıdaki kod parçacığı bir yanlış adlandırılmış genel tür parametresi gösterilmektedir:

[!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_3.cpp)]
[!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_3.vb)]
[!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_3.cs)]

Aşağıdaki kod parçacığı önceki ihlali 'T genel tür parametre ekleyerek düzeltmeleri ':

[!code-cpp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/CPP/ca1715-identifiers-should-have-correct-prefix_4.cpp)]
[!code-csharp[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/CSharp/ca1715-identifiers-should-have-correct-prefix_4.cs)]
[!code-vb[FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../code-quality/codesnippet/VisualBasic/ca1715-identifiers-should-have-correct-prefix_4.vb)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1722: Tanımlayıcıların önekleri yanlış olmamalıdır](../code-quality/ca1722-identifiers-should-not-have-incorrect-prefix.md)