---
title: 'CA1722: Tanımlayıcıların önekleri yanlış olmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotHaveIncorrectPrefix
- CA1722
helpviewer_keywords:
- CA1722
- IdentifiersShouldNotHaveIncorrectPrefix
ms.assetid: c3313c51-d004-4f9a-a0d1-6c4c4a1fb1e6
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: bea94b555be5079deae5a021cb5ecbd2ccd07adb
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53904753"
---
# <a name="ca1722-identifiers-should-not-have-incorrect-prefix"></a>CA1722: Tanımlayıcıların önekleri yanlış olmamalıdır

|||
|-|-|
|TypeName|IdentifiersShouldNotHaveIncorrectPrefix|
|CheckId|CA1722|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir tanımlayıcı yanlış bir ön eki vardır.

## <a name="rule-description"></a>Kural açıklaması
 Kural gereği, programlama öğelerinin belirli bir önek ile başlayan adları vardır.

 Tür adları, belirli bir önek yoksa ve bir 'C' ön eki olmamalıdır değil. Bu kural ihlalleri 'CMyClass' gibi tür adları için raporları ve 'Önbellek' gibi tür adları ihlallerini raporlamaz.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu tutarlılık, yeni yazılım kitaplıkları için gerekli ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Önek tanımlayıcıdan kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kuralları
 [CA1715: Tanımlayıcılar doğru öneke sahip olmalıdır](../code-quality/ca1715-identifiers-should-have-correct-prefix.md)