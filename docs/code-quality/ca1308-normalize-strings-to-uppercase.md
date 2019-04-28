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
ms.openlocfilehash: 4e8d8b5b522f805bd7e8826cea5ced394c50064f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546680"
---
# <a name="ca1308-normalize-strings-to-uppercase"></a>CA1308: Dizeleri büyük harfe normalleştirin

|||
|-|-|
|TypeName|NormalizeStringsToUppercase|
|CheckId|CA1308|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir işlem, bir dizeyi küçük harfe normalleştirir.

## <a name="rule-description"></a>Kural açıklaması
 Dizeler büyük harfe normalleştirilmeli. Küçük bir grup karakterlerin küçük harfe dönüştürülür, gidiş dönüş yapamaz. Gidiş dönüş yapmak dönüştürülmüş karakterlerinden özgün karakterler karakterleri bir yerel ayardan farklı karakter verileri temsil eden başka bir yerel ayar ve ardından için doğru bir şekilde dönüştürmek için yol alın.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Değiştirme dizelerini küçük harfe dönüştürmek ve böylece dizeleri dönüştürülür işlemleri yerine büyük. Örneğin, değiştirme `String.ToLower(CultureInfo.InvariantCulture)` için `String.ToUpper(CultureInfo.InvariantCulture)`.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 (Örneğin, kullanıcı Arabiriminde görüntülemekte olduğunuz) sonucuna dayalı güvenlik kararı yaparken değil, bir uyarı iletisi bastırmak güvenlidir.

## <a name="see-also"></a>Ayrıca bkz.
 [Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)