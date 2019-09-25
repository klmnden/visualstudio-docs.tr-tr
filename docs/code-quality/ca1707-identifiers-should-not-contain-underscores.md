---
title: 'CA1707: Tanımlayıcılar alt çizgi içermemelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotContainUnderscores
- CA1707
helpviewer_keywords:
- CA1707
- IdentifiersShouldNotContainUnderscores
ms.assetid: 5fb539ef-c304-4323-90c0-b14386da9774
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: adfa0ccd63d0433d367b0e7278693608bb83d685
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234265"
---
# <a name="ca1707-identifiers-should-not-contain-underscores"></a>CA1707: Tanımlayıcılar alt çizgi içermemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotContainUnderscores|
|CheckId|CA1707|
|Kategori|Microsoft. Naming|
|Son değişiklik|Parçalara ayırma-derlemeler üzerinde ne zaman tetiklenir<br /><br /> Tür parametrelerine ne zaman kabarık olmayan|

## <a name="cause"></a>Sebep

Tanımlayıcının adı alt çizgi (\_) karakterini içerir.

## <a name="rule-description"></a>Kural açıklaması

Kurala göre, tanımlayıcı adları alt çizgi (\_) karakterini içermez. Kural ad alanlarını, türleri, üyeleri ve parametreleri denetler.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıklar için ortak bir görünüm sağlar. Bu, yeni yazılım kitaplıkları için gerekli olan öğrenme eğrisini azaltır ve müşterinin, kitaplığın yönetilen kod geliştirme konusunda uzmanlığa sahip olan birisi tarafından geliştirildiğini arttırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Adın tüm alt çizgi karakterlerini kaldırır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kurallar

- [CA1709 Tanımlayıcılar doğru şekilde yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708 Tanımlayıcılar, büyük/küçük harf bakımından farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
