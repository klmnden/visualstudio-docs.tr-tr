---
title: 'CA2132: Varsayılan oluşturucular en az taban tür varsayılan oluşturucular kadar kritik olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2132
ms.assetid: e758afa1-8bde-442a-8a0a-bd1ea7b0ce4d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6c5ca98219444515d01baf670489120238cb8dda
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232337"
---
# <a name="ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors"></a>CA2132: Varsayılan oluşturucular en az taban tür varsayılan oluşturucular kadar kritik olmalıdır

|||
|-|-|
|TypeName|Defaultconstructorsmusthavepotenttransparency|
|CheckId|CA2132|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

> [!NOTE]
> Bu uyarı yalnızca CoreCLR (CLR 'nin Silverlight Web uygulamalarına özgü sürümü) çalıştıran koda uygulanır.

## <a name="cause"></a>Sebep

Türetilmiş bir sınıfın varsayılan oluşturucusunun saydamlık özniteliği, temel sınıfın saydamlığı kadar kritik değildir.

## <a name="rule-description"></a>Kural açıklaması

' A sahip <xref:System.Security.SecurityCriticalAttribute> olan türler ve Üyeler Silverlight uygulama kodu tarafından kullanılamaz. Kritik güvenlik türleri ve üyeleri, yalnızca Silverlight sınıf kütüphanesi için .NET Framework'ündeki güvenilen kod tarafından kullanılabilir. Türetilmiş sınıftaki ortak veya korumalı oluşturma, onun temel sınıfından aynı düzeyde veya daha saydam olması gerektiğinden uygulama içindeki sınıf SecurityCritical olarak işaretlenmiş bir sınıftan türeyemez.

CoreCLR platform kodu için, bir temel türün ortak veya korumalı olmayan bir varsayılan Oluşturucusu varsa, türetilen tür varsayılan Oluşturucu devralma kurallarına uymalıdır. Türetilmiş türün aynı zamanda varsayılan bir oluşturucusu olmalıdır ve bu Oluşturucu en az temel türün kritik varsayılan oluşturucu olarak olmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

İhlalin giderilmesi için, türü kaldırın veya güvenlik açısından saydam olmayan türden türemeyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan gelen uyarıları göstermez. Bu kuralın uygulama kodu tarafından ihlal edilmesine yol <xref:System.TypeLoadException>açacaktır.

### <a name="code"></a>Kod

[!code-csharp[FxCop.Security.CA2132.DefaultConstructorsMustHaveConsistentTransparency#1](../code-quality/codesnippet/CSharp/ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors_1.cs)]