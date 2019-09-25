---
title: 'CA1308: Dizeleri büyük harfe normalleştirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1308
- NormalizeStringsToUppercase
helpviewer_keywords:
- NormalizeStringsToUppercase
- CA1308
ms.assetid: 7e9a7457-3f93-4938-ac6f-1389fba8d9cc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c33f4b0b55728d659c34e0ffc8723f555a6d074d
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234922"
---
# <a name="ca1308-normalize-strings-to-uppercase"></a>CA1308: Dizeleri büyük harfe normalleştirin

|||
|-|-|
|TypeName|NormalizeStringsToUppercase|
|CheckId|CA1308|
|Kategori|Microsoft. Globalization|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir işlem, dizeyi küçük harfe normalleştirir.

## <a name="rule-description"></a>Kural açıklaması
Dizeler büyük harfe normalleştirilmeli. Küçük bir karakter grubu, küçük harfe dönüştürüldüğünde, gidiş dönüş yapamaz. Gidiş dönüş yapmak için, karakterleri farklı bir yerel ayara dönüştürmek için karakter verilerinin farklı bir yerel ayara dönüştürülmesi ve sonra özgün karakterlerin dönüştürülmüş karakterlerden doğru şekilde alınması anlamına gelir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Dizelerin büyük harfe dönüştürülmesi için dizeleri küçük harfe dönüştüren işlemleri değiştirin. Örneğin, olarak `String.ToUpper(CultureInfo.InvariantCulture)`değiştirin `String.ToLower(CultureInfo.InvariantCulture)` .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Sonuca göre güvenlik kararı verirken (örneğin, Kullanıcı arabiriminde görüntülerken) bir uyarı iletisini gizlemek güvenlidir.

## <a name="see-also"></a>Ayrıca bkz.
[Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)