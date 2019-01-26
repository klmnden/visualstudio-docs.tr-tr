---
title: 'CA1900: Değer tür alanları taşınabilir olmalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 84861aa1d17f041061d1666d6f78c9d273b948b4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55037778"
---
# <a name="ca1900-value-type-fields-should-be-portable"></a>CA1900: Değer tür alanları taşınabilir olmalıdır

|||
|-|-|
|TypeName|ValueTypeFieldsShouldBePortable|
|CheckId|CA1900|
|Kategori|Microsoft.Portability|
|Yeni Değişiklik|Alan derlemesi dışında görülebilir, - kesiliyor.<br /><br /> Bölünemez - alanın derlemenin dışında görünür değilse.|

## <a name="cause"></a>Sebep
 Bu kural ile açık düzene bildirilen yapıları için 64-bit işletim sistemlerinde yönetilmeyen kod sıralandığı zaman doğru olarak hizalamayı denetler. IA-64 hizalanmamış bellek erişir ve bu ihlal düzeltilmezse süreci kilitlenecek izin vermez.

## <a name="rule-description"></a>Kural açıklaması
 Sahip 64 bit işletim sistemlerinde Çökmelere neden olur yanlış hizalanmış alanlar içeren açık Yerleşimli yapılar.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 8 bayttan küçük olan tüm alanlar, boyutunun bir katı olan uzaklık ve 8 bayt alanlar olmalıdır veya daha fazla 8'in katı olan uzaklık olması gerekir. Başka bir çözüm `LayoutKind.Sequential` yerine `LayoutKind.Explicit`makul verilebilir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu uyarı yalnızca hata oluşursa atlanması.