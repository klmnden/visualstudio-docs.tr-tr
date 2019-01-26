---
title: 'CA1504: Yanıltıcı alan adlarını gözden geçirin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: da99bab4235028f75146be1807162e93759d3eb9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54926468"
---
# <a name="ca1504-review-misleading-field-names"></a>CA1504: Yanıltıcı alan adlarını gözden geçirin

|||
|-|-|
|TypeName|ReviewMisleadingFieldNames|
|CheckId|CA1504|
|Kategori|Microsoft.Maintainability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Örnek alan adı "kendisinin" ya da adı ile başlatılır bir `static` (`Shared` içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) alanı "m_" ile başlar.

## <a name="rule-description"></a>Kural açıklaması
 "Kendisinin" ile başlayan alan adları ile statik verileri birden çok kullanıcı tarafından ilişkilendirilir. Benzer şekilde, "m_" ile başlayan alan adlarını, örneği (üye) verileri ile ilişkilidir. Daha kolay tutulan kodunu adları genel olarak kullanılan kuralları izlemelidir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için uygun önekle kullanarak alanı'nı yeniden adlandırın. Alternatif olarak, geçerli son eki ile ekleyerek veya kaldırarak kabul alan olun `static` değiştiricisi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.