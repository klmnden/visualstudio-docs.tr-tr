---
title: 'CA1044: Özellikler salt yazılır olmamalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- PropertiesShouldNotBeWriteOnly
- CA1044
helpviewer_keywords:
- CA1044
- PropertiesShouldNotBeWriteOnly
ms.assetid: 8386bf3a-b161-4841-bf8b-92591595aea9
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 374bc4e9252dc07bde1f056aaf542811953fd69d
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57868223"
---
# <a name="ca1044-properties-should-not-be-write-only"></a>CA1044: Özellikler salt yazılır olmamalıdır

|||
|-|-|
|TypeName|PropertiesShouldNotBeWriteOnly|
|CheckId|CA1044|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Ayarlama erişimcisine ancak bir alma erişimcisi bir özelliğe sahiptir.

Varsayılan olarak, bu kural yalnızca genel türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Alma erişimcisi bir özelliği okuma erişimi ve set erişimcileri yazma erişimi sağlar. Salt okunur özelliğe sahip olmasına karşın kabul edilebilir ve genellikle gereklidir, tasarıma ilişkin yönergeler salt yazılır özellik kullanılmasını engeller. Bunun nedeni, bir kullanıcı bir değere ayarlayın, ve ardından kullanıcı değeri görüntülemeyi engellerse herhangi bir güvenlik sağlamaz. Ayrıca, okuma erişimi olmadan, yararsız olduklarını sınırlayan paylaşılan nesnelerin durumu görüntülenemez.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için özelliği bir alma erişimcisi ekleyin. Salt yazılır özelliği davranışını gerekliyse, alternatif olarak, bu özelliği yönteme dönüştürmek göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıları bastırmayın önerilir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1044.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnekte, `BadClassWithWriteOnlyProperty` salt yazma özelliğine sahip bir tür. `GoodClassWithReadWriteProperty` Düzeltilen kod içerir.

[!code-vb[FxCop.Design.PropertiesNotWriteOnly#1](../code-quality/codesnippet/VisualBasic/ca1044-properties-should-not-be-write-only_1.vb)]
[!code-csharp[FxCop.Design.PropertiesNotWriteOnly#1](../code-quality/codesnippet/CSharp/ca1044-properties-should-not-be-write-only_1.cs)]