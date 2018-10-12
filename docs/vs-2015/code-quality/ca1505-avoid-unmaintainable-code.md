---
title: 'CA1505: kodlardan kaçının | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- AvoidUnmaintainableCode
- CA1505
helpviewer_keywords:
- AvoidUnmaintainableCode
- CA1505
ms.assetid: 8292b268-5929-4221-b699-f9c414bcec5d
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: d5c333299f323e03a01b121fb18799e9249bcc11
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223294"
---
# <a name="ca1505-avoid-unmaintainable-code"></a>CA1505: Bakımı yapılamayan kodlardan kaçının
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|AvoidUnmantainableCode|
|CheckId|CA1505|
|Kategori|Microsoft.Maintainability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir tür veya yöntemin düşük bakım dizin değeri vardır.

## <a name="rule-description"></a>Kural Tanımı
 Bakım dizini aşağıdaki ölçümleri kullanarak hesaplanır: kod, programın toplu ve döngüzel karmaşıklığına satır. Programın toplu bir türün veya yöntemin işleçler ve işlenenleri kodda sayısını temel alan bir anlayış zorluk ölçüsüdür. Döngüsel karmaşıklık yapısal türü veya yönteminde karmaşıklığını ölçüsüdür. Kod ölçümleri hakkında daha fazla bilgi [ölçüm karmaşıklığı ve yönetilen kod bakımı](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md).

 Düşük bakım dizini bir türün veya yöntemin korumak muhtemelen koruması zor olan ve yeniden tasarlamanız için iyi bir aday olabilir gösterir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu ihlali gidermek için tür veya yöntem yeniden tasarlayın ve daha küçük ve daha fazla odaklanmış türleri veya yöntemleri bölmek deneyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu uyarı, bir türün veya yöntemin hala en büyük boyutuna rağmen veya türü veya yönteminde bölünemez sürdürülebilir edildiği durumlarda hariç tutun.

## <a name="see-also"></a>Ayrıca Bkz.
 [Bakım uyarıları](../code-quality/maintainability-warnings.md) [ölçüm karmaşıklığı ve yönetilen kod bakımı](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)



