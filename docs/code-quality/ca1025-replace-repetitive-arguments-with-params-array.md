---
title: 'CA1025: Yinelenen bağımsız değişkenleri params dizisiyle değiştirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1025
- ReplaceRepetitiveArgumentsWithParamsArray
helpviewer_keywords:
- ReplaceRepetitiveArgumentsWithParamsArray
- CA1025
ms.assetid: f009b340-dea3-4459-8fe1-2143aa8b5d0b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f65d64dd4e881c41b17cd7cb9dc072a6fe800766
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236142"
---
# <a name="ca1025-replace-repetitive-arguments-with-params-array"></a>CA1025: Yinelenen bağımsız değişkenleri params dizisiyle değiştirin

|||
|-|-|
|TypeName|ReplaceRepetitiveArgumentsWithParamsArray|
|CheckId|CA1025|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Ortak bir türdeki ortak veya korumalı yöntemin üçten fazla parametresi vardır ve son üç parametresi aynı türde.

## <a name="rule-description"></a>Kural açıklaması
Bağımsız değişkenlerin tam sayısı bilindiğinde ve değişken bağımsız değişkenleri aynı türde olduğunda veya aynı türde bir değer geçirirse tekrarlanabilir bağımsız değişkenler yerine bir parametre dizisi kullanın. Örneğin, <xref:System.Console.WriteLine%2A> yöntemi herhangi bir <xref:System.Object> sayıda bağımsız değişken kabul etmek için bir parametre dizisi kullanan genel amaçlı bir aşırı yükleme sağlar.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için yinelenen bağımsız değişkenleri bir parametre dizisi ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarının gösterilmemesi her zaman güvenlidir; Ancak, bu tasarım kullanılabilirlik sorunlarına neden olabilir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden bir türü gösterir.

[!code-csharp[FxCop.Design.RepeatArgs#1](../code-quality/codesnippet/CSharp/ca1025-replace-repetitive-arguments-with-params-array_1.cs)]