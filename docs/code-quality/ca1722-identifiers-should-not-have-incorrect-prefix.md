---
title: 'CA1722: Tanımlayıcılar yanlış ön ek içermemelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotHaveIncorrectPrefix
- CA1722
helpviewer_keywords:
- CA1722
- IdentifiersShouldNotHaveIncorrectPrefix
ms.assetid: c3313c51-d004-4f9a-a0d1-6c4c4a1fb1e6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eb41f2ad4548933d10137e7f72cae59643d33043
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233884"
---
# <a name="ca1722-identifiers-should-not-have-incorrect-prefix"></a>CA1722: Tanımlayıcılar yanlış ön ek içermemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotHaveIncorrectPrefix|
|CheckId|CA1722|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Tanımlayıcının ön eki yanlış.

## <a name="rule-description"></a>Kural açıklaması
Kural gereği, programlama öğelerinin belirli bir önek ile başlayan adları vardır.

Tür adlarında belirli bir önek yoktur ve ' C ' öneki eklenmelidir. Bu kural, ' CMyClass ' gibi tür adları için ihlalleri raporlar ve ' cache ' gibi tür adları için ihlalleri rapor etmez.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıklar için ortak bir görünüm sağlar. Bu tutarlılık, yeni yazılım kitaplıkları için gerekli olan öğrenme eğrisini azaltır ve bu, kitaplığın yönetilen kod geliştirme konusunda uzmanlığa sahip olan birisi tarafından geliştirildiği müşterinin güvenini artırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Öneki tanımlayıcıdan kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kurallar
[CA1715 Tanımlayıcılar doğru öneke sahip olmalıdır](../code-quality/ca1715-identifiers-should-have-correct-prefix.md)