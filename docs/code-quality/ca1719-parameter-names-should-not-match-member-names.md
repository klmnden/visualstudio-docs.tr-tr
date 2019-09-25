---
title: 'CA1719: Parametre adları üye adları ile eşleşmemelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ParameterNamesShouldNotMatchMemberNames
- CA1719
helpviewer_keywords:
- CA1719
- ParameterNamesShouldNotMatchMemberNames
ms.assetid: c6fea690-1659-4ee7-a1c5-125ad6754525
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2aa55993758df24346b78eb4d9ad022014d9d81c
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233982"
---
# <a name="ca1719-parameter-names-should-not-match-member-names"></a>CA1719: Parametre adları üye adları ile eşleşmemelidir

|||
|-|-|
|TypeName|ParameterNamesShouldNotMatchMemberNames|
|CheckId|CA1719|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Dışarıdan görünen bir üyenin adı, büyük/küçük harfe duyarsız bir karşılaştırmayla eşleşir, parametrelerinden birinin adı.

## <a name="rule-description"></a>Kural açıklaması
Parametre adı parametrenin anlamıyla iletişim kurmalı ve üyenin adını üye anlamıyla iliştirmelidir. Bunların aynı olduğu yerlerde nadir bir tasarım olur. Aynı üye adıyla parametreyi adlandırma sezgisel değildir ve kütüphane kullanımını zorlaştırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Üye adıyla eşleşmeyen bir parametre adı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Yeni geliştirme için, bu kuraldan bir uyarıyı bastırmalısınız hiçbir bilinen senaryo oluşmaz. Gönderim kitaplıkları için, bu kuraldan bir uyarıyı bastırın.

## <a name="related-rules"></a>İlgili kurallar
[CA1709 Tanımlayıcılar doğru şekilde yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)

[CA1708 Tanımlayıcılar, büyük/küçük harf bakımından farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

[CA1707 Tanımlayıcılar alt çizgi içermemelidir](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)