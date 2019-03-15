---
title: 'CA1012: Soyut türlerin oluşturucuları olmamalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- AbstractTypesShouldNotHaveConstructors
- CA1012
helpviewer_keywords:
- CA1012
ms.assetid: 09f458ac-dd88-4cd7-a47f-4106c1e80ece
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 5114f6015d055c03d54d49deee1197b7e3d9c9da
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57867683"
---
# <a name="ca1012-abstract-types-should-not-have-constructors"></a>CA1012: Soyut türlerin oluşturucuları olmamalıdır

|||
|-|-|
|TypeName|AbstractTypesShouldNotHaveConstructors|
|CheckId|CA1012|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir türü soyuttur ve bir oluşturucusu vardır.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Soyut türler üzerindeki kurucular yalnızca türetilen türler tarafından çağrılabilir. Bir türün örneklerinin genel oluşturucular oluşturabilir ve bir soyut tür örneği oluşturulamıyor çünkü ortak yapıcıya sahip, soyut bir tür yanlış şekilde tasarlanmıştır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için korumalı Oluşturucu olun veya türü soyut olarak bildirmeyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın. Soyut tür, genel bir oluşturucusu vardır.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1012.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki kod parçacığını bu kuralı ihlal soyut bir tür içeriyor.

[!code-vb[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_1.vb)]
[!code-csharp[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_1.cs)]

Aşağıdaki kod parçacığı oluşturucudan erişilebilirliğini değiştirerek önceki ihlali düzeltmeleri `public` için `protected`.

[!code-csharp[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_2.cs)]
[!code-vb[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_2.vb)]