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
ms.openlocfilehash: 5014bfe809cb5d56a22e971833128d1f48d77319
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922976"
---
# <a name="ca1025-replace-repetitive-arguments-with-params-array"></a>CA1025: Yinelenen bağımsız değişkenleri params dizisiyle değiştirin

|||
|-|-|
|TypeName|ReplaceRepetitiveArgumentsWithParamsArray|
|CheckId|CA1025|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

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