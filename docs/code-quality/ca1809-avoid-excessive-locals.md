---
title: 'CA1809: Aşırı yerellerden kaçının'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1809
- AvoidExcessiveLocals
helpviewer_keywords:
- AvoidExcessiveLocals
- CA1809
ms.assetid: 5c81ea43-cb49-448f-980f-a1dd9764043c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5adce9ea32cb29154d88538d7b142e29b3e29761
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54957682"
---
# <a name="ca1809-avoid-excessive-locals"></a>CA1809: Aşırı yerellerden kaçının

|||
|-|-|
|TypeName|AvoidExcessiveLocals|
|CheckId|CA1809|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Üye bazıları derleyici tarafından oluşturulmuş olabilir, 64'ten fazla yerel değişkenler içerir.

## <a name="rule-description"></a>Kural açıklaması
 Olarak adlandırılan bellek yerine işlemci kayıttaki değeri depolamak için yaygın bir performans iyileştirmesidir olduğu *kayıt* değeri. Ortak dil çalışma zamanı enregistration için en fazla 64 yerel değişkenler olarak değerlendirir. Kaydedilme olmayan değişkenler yığına yerleştirilir ve işleme önce bir kayıt taşınması gerekir. Fırsat izin vermek için tüm yerel değişkenlerin kaydedilme alın, 64 yerel değişken sayısını sınırlayın.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için en fazla 64 yerel değişken kullanmak için uygulama yeniden düzenleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Performans sorunu değilse bu kuraldan bir uyarıyı bastırmak için veya kuralı devre dışı bırakmak için güvenlidir.

## <a name="related-rules"></a>İlgili kuralları
 [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)