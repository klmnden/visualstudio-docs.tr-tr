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
ms.openlocfilehash: 06fe8d4fbd4def14bfb8a24f4f211a121c809930
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922246"
---
# <a name="ca1308-normalize-strings-to-uppercase"></a>CA1308: Dizeleri büyük harfe normalleştirin

|||
|-|-|
|TypeName|NormalizeStringsToUppercase|
|CheckId|CA1308|
|Kategori|Microsoft. Globalization|
|Yeni Değişiklik|Kırılmamış|

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