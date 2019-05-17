---
title: 'CA1051: Görünür örnek alanlarını bildirmeyin'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1051
- DoNotDeclareVisibleInstanceFields
helpviewer_keywords:
- CA1051
- DoNotDeclareVisibleInstanceFields
ms.assetid: 2805376c-824c-462c-81d1-c51aaf7cabe7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6c77678b1f09b1cf51a63f260252ddeaf9321fd5
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65842078"
---
# <a name="ca1051-do-not-declare-visible-instance-fields"></a>CA1051: Görünür örnek alanlarını bildirmeyin

|||
|-|-|
|TypeName|DoNotDeclareVisibleInstanceFields|
|CheckId|CA1051|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir türün özel olmayan örnek alanı var.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir alanın birincil kullanım alanının uygulama ayrıntısı olması gerekir. Alanlar olmalıdır `private` veya `internal` ve özelliklerini kullanmaya maruz kalması. Bir alana erişmek olduğu ve özellikleri türünde bozucu değişiklikler oluşturmaksızın genişlettikçe özellik erişimcileri kodda değiştirebilirsiniz bir özelliğe erişmek oldukça kolaydır. Yalnızca özel veya iç alan değerini döndüren özellikler, bir alana erişim özellik gerçekleştirmek için optimize edilmiş; çok az performans kazancı özellikler üzerinde dışarıdan görünen alanları kullanımı ile ilişkilidir.

Dışarıdan görünen başvurduğu `public`, `protected`, ve `protected internal` (`Public`, `Protected`, ve `Protected Friend` Visual Basic'te) erişilebilirlik düzeyleri.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için alanın olmasını `private` veya `internal` ve dışarıdan görünen bir özelliğini kullanarak üzerinden kullanıma sunacaksınız.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın. Dışarıdan görünen alanlar, özellikler için kullanılabilir olan herhangi bir avantaj sağlamaz. Ayrıca, ortak alanları tarafından korunamaz [bağlantı talepleri](/dotnet/framework/misc/link-demands). Bkz: [CA2112: Güvenli türler alanları kullanıma](../code-quality/ca2112-secured-types-should-not-expose-fields.md).

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1051.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bir tür gösterir (`BadPublicInstanceFields`), bu kuralı ihlal ediyor. `GoodPublicInstanceFields` Düzeltilen kod gösterilmektedir.

[!code-csharp[FxCop.Design.TypesPublicInstanceFields#1](../code-quality/codesnippet/CSharp/ca1051-do-not-declare-visible-instance-fields_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA2112: Güvenli türler alanları açığa çıkarmamalıdır](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Bağlantı talepleri](/dotnet/framework/misc/link-demands)