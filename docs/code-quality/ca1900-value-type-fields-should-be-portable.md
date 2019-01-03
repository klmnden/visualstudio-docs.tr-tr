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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ffac1cca87f3b1cbed23e2bbc8a9b463cd4adc6c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53987855"
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