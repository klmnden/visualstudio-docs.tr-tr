---
title: 'CA1713: Olaylarda önce veya sonra önek olmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f5133cf03567eabab9eea95b7fadc52304a1d7c9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53890754"
---
# <a name="ca1713-events-should-not-have-before-or-after-prefix"></a>CA1713: Olaylarda önce veya sonra önek olmamalıdır

|||
|-|-|
|TypeName|EventsShouldNotHaveBeforeOrAfterPrefix|
|CheckId|CA1713|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Olay adı, 'Before' veya 'After' ile başlar.

## <a name="rule-description"></a>Kural açıklaması
 Olay adları olayı oluşturan eylem açıklamalıdır. Belirli bir sırayla ilgili olayları adlandırmak için şimdiki veya geçmiş zamanı göreceli konumun sıralı eylemlerini belirtmek için kullanın. Olay çifti adlandırma kaynak kapatırken oluştuğunda, örneğin, 'Kapanış' ve 'Kapalı' yerine 'BeforeClose' ve 'AfterClose' adını.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Olay adı ön ekini kaldırın ve mevcut ya da bir fiil, geçmiş şimdiki kullanılacak adını değiştirmeyi göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.