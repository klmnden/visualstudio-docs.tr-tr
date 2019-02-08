---
title: 'CA1814: Çok boyutlu diziler yerine basit dizileri tercih edin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PreferJaggedArraysOverMultidimensional
- CA1814
helpviewer_keywords:
- PreferJaggedArraysOverMultidimensional
- CA1814
ms.assetid: b1ccf563-2ec8-42e5-b89c-731a9de1ea1d
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 6d3dc26964a62c952b9c8d18c710e6163bf8ab08
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55955329"
---
# <a name="ca1814-prefer-jagged-arrays-over-multidimensional"></a>CA1814: Çok boyutlu diziler yerine basit dizileri tercih edin

|||
|-|-|
|TypeName|PreferJaggedArraysOverMultidimensional|
|CheckId|CA1814|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Üye, çok boyutlu bir dizi bildirilir.

## <a name="rule-description"></a>Kural açıklaması
 Basit bir dizi, öğeleri dizi olan bir dizidir. Öğeleri olan diziler bazı veri kümeler için daha az harcanmış önde gelen farklı boyutlarda olabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için basit bir dizi çok boyutlu dizi değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Çok boyutlu dizi alanı boşa değil, bu kuraldan bir uyarıyı gizler.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, basit ve çok boyutlu diziler için bildirimi gösterir.

 [!code-vb[FxCop.Performance.JaggedArrays#1](../code-quality/codesnippet/VisualBasic/ca1814-prefer-jagged-arrays-over-multidimensional_1.vb)]
 [!code-csharp[FxCop.Performance.JaggedArrays#1](../code-quality/codesnippet/CSharp/ca1814-prefer-jagged-arrays-over-multidimensional_1.cs)]