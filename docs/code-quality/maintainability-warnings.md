---
title: Bakım Uyarıları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.maintainabilityrules
helpviewer_keywords:
- warnings, maintainability
- managed code analysis warnings, maintainability warnings
- maintainability warnings
ms.assetid: 537e70ca-a88c-49df-bfc7-0ee63bbe4f16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7d5508e203b8ed5087f456c715c492d8f1ca7c86
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55943460"
---
# <a name="maintainability-warnings"></a>Bakım Uyarıları

Bakım uyarıları, kitaplık ve Uygulama Bakımı desteklemez.

## <a name="in-this-section"></a>Bu Bölümde

| Kural | Açıklama |
|-----------|-----------------------------------|
| [CA1500: Değişken adları alan adlarıyla eşleşmemelidir](../code-quality/ca1500-variable-names-should-not-match-field-names.md) | Bir örnek yöntemi, bir parametre veya hataları müşteri adayları bildirim türü bir örnek alan adıyla eşleşen bir yerel değişken bildirir. |
| [CA1501: Aşırı devralmadan kaçının](../code-quality/ca1501-avoid-excessive-inheritance.md) | Devralma hiyerarşisinde düzeyleri dörtten fazla olan türdür. İç içe yuvalanmış hiyerarşileri izlemek, anlamak ve muhafaza etmek zor olabilir. |
| [CA1502: Aşırı karmaşıklıktan kaçının](../code-quality/ca1502-avoid-excessive-complexity.md) | Bu kural, sayılarla ve şartlı şubelerle tanımlanan, yönteme giden doğrusal bağımsız yolların sayısını ölçer. |
| [CA1504: Yanıltıcı alan adlarını gözden geçirin](../code-quality/ca1504-review-misleading-field-names.md) | Örnek alan adı "kendisinin" ya da statik adını başlatılır (paylaşılan [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) alanı "m_" ile başlar. |
| [CA1505: Kodlardan kaçının](../code-quality/ca1505-avoid-unmaintainable-code.md) | Bir tür veya yöntemin düşük bakım dizin değeri vardır. Düşük bakım dizini muhtemelen koruması zor olan ve yeniden tasarım için iyi bir aday olan tür veya yöntemi içerir. |
| [CA1506: Aşırı sınıf bağlantısından kaçının](../code-quality/ca1506-avoid-excessive-class-coupling.md) | Bu kural türü veya yöntemini içeren benzersiz türde başvuru sayısı belirlenerek eşlenmesiyle sınıfı ölçer. |

## <a name="see-also"></a>Ayrıca Bkz.

- [Yönetilen Kodun Ölçüm Karmaşıklığı ve Bakımı](../code-quality/code-metrics-values.md)