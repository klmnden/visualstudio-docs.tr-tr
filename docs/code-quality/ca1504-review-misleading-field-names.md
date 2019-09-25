---
title: 'CA1504: Yanıltıcı alan adlarını gözden geçirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ReviewMisleadingFieldNames
- CA1504
helpviewer_keywords:
- CA1504
- ReviewMisleadingFieldNames
ms.assetid: 94136ff1-4aaf-4dc2-9170-48c171ab7499
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 31c147c67854dd59f1fb7c9202f553edfb4a77a8
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234503"
---
# <a name="ca1504-review-misleading-field-names"></a>CA1504: Yanıltıcı alan adlarını gözden geçirin

|||
|-|-|
|TypeName|ReviewMisleadingFieldNames|
|CheckId|CA1504|
|Kategori|Microsoft. Bakımolmaması|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir örnek alanının adı "s_" ile başlar veya bir `static` (`Shared` ın [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) alanının adı "m_" ile başlar.

## <a name="rule-description"></a>Kural açıklaması
"S_" ile başlayan alan adları, birçok kullanıcı tarafından statik verilerle ilişkilendirilir. Benzer şekilde, "m_" ile başlayan alan adları, örnek (üye) verilerle ilişkilendirilir. Daha kolay yönetilebilir kod için adlar genellikle kullanılan kurallara uymalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, uygun öneki kullanarak alanı yeniden adlandırın. Alternatif olarak, `static` değiştirici ekleyerek veya kaldırarak alanı geçerli sonek ile kabul edin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.