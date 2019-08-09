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
ms.openlocfilehash: df6ab704c2dfdbf8ebdf8eb42f56d8d64600736f
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921823"
---
# <a name="ca1504-review-misleading-field-names"></a>CA1504: Yanıltıcı alan adlarını gözden geçirin

|||
|-|-|
|TypeName|ReviewMisleadingFieldNames|
|CheckId|CA1504|
|Kategori|Microsoft. Bakımolmaması|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir örnek alanının adı "s_" ile başlar veya bir `static` (`Shared` ın [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) alanının adı "m_" ile başlar.

## <a name="rule-description"></a>Kural açıklaması
"S_" ile başlayan alan adları, birçok kullanıcı tarafından statik verilerle ilişkilendirilir. Benzer şekilde, "m_" ile başlayan alan adları, örnek (üye) verilerle ilişkilendirilir. Daha kolay yönetilebilir kod için adlar genellikle kullanılan kurallara uymalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, uygun öneki kullanarak alanı yeniden adlandırın. Alternatif olarak, `static` değiştirici ekleyerek veya kaldırarak alanı geçerli sonek ile kabul edin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.