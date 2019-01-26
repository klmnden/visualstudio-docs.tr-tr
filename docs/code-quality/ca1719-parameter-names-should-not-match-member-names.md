---
title: 'CA1719: Parametre adları üye adları ile eşleşmemelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 86f7b2b79136f2a65a56f0bd1271258b32c97f02
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54935598"
---
# <a name="ca1719-parameter-names-should-not-match-member-names"></a>CA1719: Parametre adları üye adları ile eşleşmemelidir

|||
|-|-|
|TypeName|ParameterNamesShouldNotMatchMemberNames|
|CheckId|CA1719|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir üyenin adını, büyük küçük harf duyarsız karşılaştırma içinde parametrelerinden birinin adını eşleşir.

## <a name="rule-description"></a>Kural açıklaması
 Parametre adı parametrenin anlamıyla iletişim kurmalı ve üyenin adını üye anlamıyla iliştirmelidir. Bunların aynı olduğu yerlerde nadir bir tasarım olur. Aynı üye adıyla parametreyi adlandırma sezgisel değildir ve kütüphane kullanımını zorlaştırır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Üye adıyla eşleşmiyor bir parametre adı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Yeni geliştirme, hiçbir bilinen senaryolar ortaya burada bu kuraldan bir uyarıyı bastırmak gerekir. Kitaplıkları sevk edilmesi için bu kuraldan bir uyarıyı bastırmak gerekebilir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)

 [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)

 [CA1707: Tanımlayıcılar alt çizgi içermemelidir](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)