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
ms.openlocfilehash: 1cbd6d3999525808180f69652290807d327b6814
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55917746"
---
# <a name="ca1707-identifiers-should-not-contain-underscores"></a>CA1707: Tanımlayıcılar alt çizgi içermemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotContainUnderscores|
|CheckId|CA1707|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|-Derlemelerini oluştuğunda kesme<br /><br /> Tür parametrelerinde oluştuğunda bölünemez-|

## <a name="cause"></a>Sebep

Tanımlayıcı adı alt çizgi içeriyor (\_) karakter.

## <a name="rule-description"></a>Kural açıklaması

Kural gereği, tanımlayıcı adları alt çizgi içermez (\_) karakter. Kural ad alanlarını, türleri, üyeleri ve parametreleri denetler.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Tüm alt çizgi karakterleri adından kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kuralları

- [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708: Tanımlayıcılar örnekten daha fazla farklı olmalıdır](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
