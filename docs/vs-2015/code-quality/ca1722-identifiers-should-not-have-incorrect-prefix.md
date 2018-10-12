---
title: 'CA1722: Tanımlayıcıların önekleri yanlış olmamalıdır | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IdentifiersShouldNotHaveIncorrectPrefix
- CA1722
helpviewer_keywords:
- CA1722
- IdentifiersShouldNotHaveIncorrectPrefix
ms.assetid: c3313c51-d004-4f9a-a0d1-6c4c4a1fb1e6
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 305e0f251ee64165a9a25481aa6c45299d888b33
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49215598"
---
# <a name="ca1722-identifiers-should-not-have-incorrect-prefix"></a>CA1722: Tanımlayıcıların önekleri yanlış olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|IdentifiersShouldNotHaveIncorrectPrefix|
|CheckId|CA1722|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir tanımlayıcı yanlış bir ön eki vardır.

## <a name="rule-description"></a>Kural Tanımı
 Kural gereği, programlama öğelerinin belirli bir önek ile başlayan adları vardır.

 Tür adları, belirli bir önek yoksa ve bir 'C' ön eki olmamalıdır değil. Bu kural ihlalleri 'CMyClass' gibi tür adları için raporları ve 'Önbellek' gibi tür adları ihlallerini raporlamaz.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni yazılım kitaplıkları için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır öğrenme eğrisini azaltır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Önek tanımlayıcıdan kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kuralları
 [CA1715: Tanımlayıcıların önekleri doğru olmalıdır](../code-quality/ca1715-identifiers-should-have-correct-prefix.md)



