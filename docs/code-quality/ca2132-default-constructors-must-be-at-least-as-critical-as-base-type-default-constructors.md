---
title: 'CA2132: Varsayılan oluşturucular en az taban tür varsayılan oluşturucular kadar kritik olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2132
ms.assetid: e758afa1-8bde-442a-8a0a-bd1ea7b0ce4d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cfe6e4f3ce896e5ae3d728a002bf2caf9f1948ef
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55013541"
---
# <a name="ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors"></a>CA2132: Varsayılan oluşturucular en az taban tür varsayılan oluşturucular kadar kritik olmalıdır

|||
|-|-|
|TypeName|DefaultConstructorsMustHaveConsistentTransparency|
|CheckId|CA2132|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

> [!NOTE]
> Bu uyarı yalnızca CoreCLR (Silverlight web uygulamalarına özel olan CLR sürümü) çalışan kodu uygulanır.

## <a name="cause"></a>Sebep

Türetilmiş bir sınıfın varsayılan oluşturucusu saydamlık özniteliklerini temel sınıf saydamlığı önemli değildir.

## <a name="rule-description"></a>Kural açıklaması

Türleri ve üyeleri olan <xref:System.Security.SecurityCriticalAttribute> Silverlight uygulama kodu tarafından kullanılamaz. Kritik güvenlik türleri ve üyeleri, yalnızca Silverlight sınıf kütüphanesi için .NET Framework'ündeki güvenilen kod tarafından kullanılabilir. Türetilmiş sınıftaki ortak veya korumalı oluşturma, onun temel sınıfından aynı düzeyde veya daha saydam olması gerektiğinden uygulama içindeki sınıf SecurityCritical olarak işaretlenmiş bir sınıftan türeyemez.

Ortak veya korumalı saydam olmayan varsayılan bir oluşturucu bir taban türü varsa, CoreCLR platform kodunu ardından türetilmiş bir tür varsayılan oluşturucu devralma kurallara uyan gerekir. Türetilmiş bir tür aynı zamanda bir varsayılan oluşturucusu olmalıdır ve bu oluşturucu temel tür kritik varsayılan oluşturucu en az olmalıdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

İhlali gidermek için türü kaldırın veya güvenlik saydam olmayan türden türetilmiş değil.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıları bastırmayın. Uygulama kodu tarafından bu kural ihlalleri türüyle yüklenecek reddediyor CoreCLR sonuçlanır bir <xref:System.TypeLoadException>.

### <a name="code"></a>Kod

[!code-csharp[FxCop.Security.CA2132.DefaultConstructorsMustHaveConsistentTransparency#1](../code-quality/codesnippet/CSharp/ca2132-default-constructors-must-be-at-least-as-critical-as-base-type-default-constructors_1.cs)]