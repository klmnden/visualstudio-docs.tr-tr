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
ms.openlocfilehash: b4a292cb3f3221b36c163c87881fd23db0606399
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55916043"
---
# <a name="ca1025-replace-repetitive-arguments-with-params-array"></a>CA1025: Yinelenen bağımsız değişkenleri params dizisiyle değiştirin

|||
|-|-|
|TypeName|ReplaceRepetitiveArgumentsWithParamsArray|
|CheckId|CA1025|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Ortak türde ortak veya korumalı bir yöntem üçten fazla parametre içeriyor ve son üç parametrelerini aynı türdedir.

## <a name="rule-description"></a>Kural açıklaması
 Bir parametre dizisi bağımsız değişken bir tam sayısı bilinmiyor ve değişken bağımsız değişkenler aynı türde olan ya da aynı türde geçirilebilir geçirilebileceğinde bağımsız değişkenleri kullanın. Örneğin, <xref:System.Console.WriteLine%2A> yöntemi herhangi bir sayıda kabul etmek için bir parametre dizisi kullanan bir genel amaçlı bir aşırı yüklemesini sağlar <xref:System.Object> bağımsız değişkenler.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için yinelenen bağımsız değişken bir parametre dizisi ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak her zaman güvenlidir; Ancak, bu tasarım, kullanılabilirlik sorunlara neden olabilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

 [!code-csharp[FxCop.Design.RepeatArgs#1](../code-quality/codesnippet/CSharp/ca1025-replace-repetitive-arguments-with-params-array_1.cs)]