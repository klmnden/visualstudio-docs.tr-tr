---
title: 'CA1505: Bakımı yapılamayan kodlardan kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AvoidUnmaintainableCode
- CA1505
helpviewer_keywords:
- AvoidUnmaintainableCode
- CA1505
ms.assetid: 8292b268-5929-4221-b699-f9c414bcec5d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 740ef26af6f1f84d23ef27de5176df1b3de98b34
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62797322"
---
# <a name="ca1505-avoid-unmaintainable-code"></a>CA1505: Bakımı yapılamayan kodlardan kaçının

|||
|-|-|
|TypeName|AvoidUnmantainableCode|
|CheckId|CA1505|
|Kategori|Microsoft.Maintainability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir tür veya yöntemin düşük bakım dizin değeri vardır.

## <a name="rule-description"></a>Kural açıklaması

Bakım dizini aşağıdaki ölçümleri kullanarak hesaplanır: kod, programın toplu ve döngüzel karmaşıklığına satır. Programın toplu bir türün veya yöntemin işleçler ve işlenenleri kodda sayısını temel alan bir anlayış zorluk ölçüsüdür. Döngüsel karmaşıklık yapısal türü veya yönteminde karmaşıklığını ölçüsüdür. Kod ölçümleri hakkında daha fazla bilgi [ölçüm karmaşıklığı ve yönetilen kod bakımı](../code-quality/code-metrics-values.md).

Düşük bakım dizini bir türün veya yöntemin korumak muhtemelen koruması zor olan ve yeniden tasarlamanız için iyi bir aday olabilir gösterir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu ihlali gidermek için tür veya yöntem yeniden tasarlayın ve daha küçük ve daha fazla odaklanmış türleri veya yöntemleri bölmek deneyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu uyarı, tür veya yöntem bölünemez veya en büyük boyutuna rağmen sürdürülebilir olarak kabul edilir gösterilmemesini sağlayabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Bakım uyarıları](../code-quality/maintainability-warnings.md)
- [Ölçüm karmaşıklığı ve yönetilen kod bakımı](../code-quality/code-metrics-values.md)