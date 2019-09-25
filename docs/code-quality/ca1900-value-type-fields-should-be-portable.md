---
title: 'CA1900: Değer tür alanları taşınabilir olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1900
- ValueTypeFieldsShouldBePortable
helpviewer_keywords:
- ValueTypeFieldsShouldBePortable
- CA1900
ms.assetid: 1787d371-389f-4d39-b305-12b53bc0dfb9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4bef51c547d4a1614137e0691343bef635aed50d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233282"
---
# <a name="ca1900-value-type-fields-should-be-portable"></a>CA1900: Değer tür alanları taşınabilir olmalıdır

|||
|-|-|
|TypeName|ValueTypeFieldsShouldBePortable|
|CheckId|CA1900|
|Kategori|Microsoft. taşınabilirlik|
|Son değişiklik|Parçalama-alan, derleme dışında görünebilirler.<br /><br /> Bölünmez olmayan-alan, derleme dışında görünür değilse.|

## <a name="cause"></a>Sebep
Bu kural, 64 bit işletim sistemlerinde yönetilmeyen koda kopyalandıklarında açık düzen ile belirtilen yapıların doğru şekilde hizalanmasını denetler. IA-64 hizalanmamış bellek erişimine izin vermez ve bu ihlalin düzeltilmediğinde işlem kilitlenir.

## <a name="rule-description"></a>Kural açıklaması
Yanlış hizalanmış alanlar içeren açık düzene sahip yapılar 64 bitlik işletim sistemlerinde kilitlenmelere neden olur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
8 bayttan küçük olan tüm alanlar, boyutunun birden çok katı olan uzaklıklara sahip olmalıdır ve 8 bayt ya da daha fazla alan, 8 ' in katı olan uzaklıklara sahip olmalıdır. Makul ise `LayoutKind.Explicit`, yerine başka `LayoutKind.Sequential` bir çözüm kullanılır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu uyarı yalnızca hatada gerçekleşirse bastırılmalıdır.