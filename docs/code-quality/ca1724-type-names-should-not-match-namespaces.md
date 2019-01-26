---
title: 'CA1724: Tür adları ad alanları ile eşleşmemelidir'
ms.date: 09/28/2018
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- TypeNamesShouldNotMatchNamespaces
- CA1724
helpviewer_keywords:
- TypeNamesShouldNotMatchNamespaces
- CA1724
ms.assetid: 329af3b5-5600-4101-831d-531ab3eb7060
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b0bd410fabbeebc05d13eaee94db79cc346881e5
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54989227"
---
# <a name="ca1724-type-names-should-not-match-namespaces"></a>CA1724: Tür adları ad alanlarıyla eşleşmemelidir

|||
|-|-|
|TypeName|TypeNamesShouldNotMatchNamespaces|
|CheckId|CA1724|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür adı, bir veya daha fazla dışarıdan görülebilen türler olan bir başvurulan ad alanı adı ile eşleşir. Ad karşılaştırma büyük/küçük harfe duyarsızdır.

## <a name="rule-description"></a>Kural açıklaması

Kullanıcı tarafından oluşturulan tür adları dışarıdan görülebilen türler sahip başvurulan ad alanlarının adlarıyla eşleşmemelidir. Bu kuralın ihlali kitaplığın kitaplığınızın azaltabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Türü olan dışarıdan görülebilen türler başvurulan bir ad alanının adı eşleşmiyorsa gibi yeniden adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Yeni geliştirme, hiçbir bilinen senaryolar ortaya burada bu kuraldan bir uyarıyı bastırmak gerekir. Uyarının gösterilmemesi önce kitaplığınızın kullanıcılar tarafından eşleşen adı nasıl yanıltıcı dikkatlice düşünün. Kitaplıkları sevk edilmesi için bu kuraldan bir uyarıyı bastırmak gerekebilir.