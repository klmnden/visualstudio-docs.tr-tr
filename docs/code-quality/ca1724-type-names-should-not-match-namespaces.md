---
title: 'CA1724: Tür adları ad alanları ile eşleşmemelidir'
ms.date: 09/28/2018
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
ms.openlocfilehash: f81327324de937df57edfb36cae34d613f6298a5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546026"
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