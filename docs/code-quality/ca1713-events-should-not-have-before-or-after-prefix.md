---
title: 'CA1713: Olaylar önce ya da sonra önekine sahip olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- EventsShouldNotHaveBeforeOrAfterPrefix
- CA1713
helpviewer_keywords:
- CA1713
- EventsShouldNotHaveBeforeOrAfterPrefix
ms.assetid: 855772a4-aa9e-410b-88c1-c5fba1ca63da
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 834c0f73a1fdc26f06c62e1c6e3a2d19372a244d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234096"
---
# <a name="ca1713-events-should-not-have-before-or-after-prefix"></a>CA1713: Olaylar önce ya da sonra önekine sahip olmamalıdır

|||
|-|-|
|TypeName|EventsShouldNotHaveBeforeOrAfterPrefix|
|CheckId|CA1713|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir olayın adı ' before ' veya ' After ' ile başlar.

## <a name="rule-description"></a>Kural açıklaması
Olay adları, olayı oluşturan eylemi betimlemelidir. Belirli bir sırayla ilgili olayları adlandırmak için şimdiki veya geçmiş zamanı göreceli konumun sıralı eylemlerini belirtmek için kullanın. Örneğin, bir kaynağı kapatırken oluşan bir çift olayı adlandırırken, ' Beforeckaybetme ' ve ' AfterClose ' yerine ' Closing ' ve ' Closed ' adını yazabilirsiniz.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıklar için ortak bir görünüm sağlar. Bu, yeni yazılım kitaplıkları için gerekli olan öğrenme eğrisini azaltır ve müşterinin, kitaplığın yönetilen kod geliştirme konusunda uzmanlığa sahip olan birisi tarafından geliştirildiğini arttırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Olay adından öneki kaldırın ve bir fiilin var olan veya geçmiş zaman hali kullanacak şekilde adı değiştirmeyi göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.