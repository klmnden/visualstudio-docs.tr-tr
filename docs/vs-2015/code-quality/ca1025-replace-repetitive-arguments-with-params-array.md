---
title: 'CA1025: Tekrarlanan bağımsız değişkenleri params dizisi ile değiştirin. | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1025
- ReplaceRepetitiveArgumentsWithParamsArray
helpviewer_keywords:
- ReplaceRepetitiveArgumentsWithParamsArray
- CA1025
ms.assetid: f009b340-dea3-4459-8fe1-2143aa8b5d0b
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 83d36f1f5cd31b1ad1833dd805f4386ac71a3ed1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68144803"
---
# <a name="ca1025-replace-repetitive-arguments-with-params-array"></a>CA1025: Yinelenen bağımsız değişkenleri params dizisiyle değiştirin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ReplaceRepetitiveArgumentsWithParamsArray|
|CheckId|CA1025|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Ortak türde ortak veya korumalı bir yöntem üçten fazla parametre içeriyor ve son üç parametrelerini aynı türdedir.

## <a name="rule-description"></a>Kural Tanımı
 Bir parametre dizisi bağımsız değişken bir tam sayısı bilinmiyor ve değişken bağımsız değişkenler aynı türde olan ya da aynı türde geçirilebilir geçirilebileceğinde bağımsız değişkenleri kullanın. Örneğin, <xref:System.Console.WriteLine%2A> yöntemi herhangi bir sayıda kabul etmek için bir parametre dizisi kullanan bir genel amaçlı bir aşırı yüklemesini sağlar <xref:System.Object> bağımsız değişkenler.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için yinelenen bağımsız değişken bir parametre dizisi ile değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak her zaman güvenlidir; Ancak, bu tasarım, kullanılabilirlik sorunlara neden olabilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

 [!code-csharp[FxCop.Design.RepeatArgs#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.RepeatArgs/cs/FxCop.Design.RepeatArgs.cs#1)]
