---
title: 'CA1809: Aşırı yerellerden kaçının'
ms.date: 11/04/2016
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
ms.openlocfilehash: 89d6ee4d1a53f63cffb31439a124d3d9358e976f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233642"
---
# <a name="ca1809-avoid-excessive-locals"></a>CA1809: Aşırı yerellerden kaçının

|||
|-|-|
|TypeName|AvoidExcessiveLocals|
|CheckId|CA1809|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir üye, biri derleyicinin ürettiği 64 taneden fazla yerel değişken içerir.

## <a name="rule-description"></a>Kural açıklaması
Yaygın bir performans iyileştirmesi, değeri *kayıt* olarak adlandırılan bellek yerine işlemci kaydındaki bir değeri depolmedir. Ortak dil çalışma zamanı, kayıt için 64 yerel değişkene kadar kabul eder. Kayıtlı olmayan değişkenler yığına konur ve düzenlemeden önce bir kayda taşınması gerekir. Tüm yerel değişkenlerin kaydolma ihtimaline izin vermek için yerel değişken sayısını 64 olarak sınırlandırın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, uygulamayı 64 ' den fazla yerel değişken kullanmak üzere yeniden düzenleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı gizlemek veya performans bir sorun değilse kuralı devre dışı bırakmak güvenlidir.

## <a name="related-rules"></a>İlgili kurallar
[CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md)