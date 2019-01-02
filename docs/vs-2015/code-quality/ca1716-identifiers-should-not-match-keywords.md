---
title: 'CA1716: Tanımlayıcılar, anahtar sözcükleri yok eşleşmelidir | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
helpviewer_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
ms.assetid: 900cc8a1-1089-4069-a4ce-10b109ac4fab
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 7a20547a33c2878f176e2adbb081fb6d0fd393ce
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967515"
---
# <a name="ca1716-identifiers-should-not-match-keywords"></a>CA1716: Tanımlayıcılar anahtar sözcükler ile eşleşmemelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|IdentifiersShouldNotMatchKeywords|
|CheckId|CA1716|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir ad alanı, bir tür veya viritual veya arabirim üye adı ayrılmış bir anahtar sözcük bir programlama dili ile eşleşir.

## <a name="rule-description"></a>Kural Tanımı
 Tanımlayıcı ad alanları, türler, için ve sanal ve arabirim üyeleri olmayan ortak dil çalışma zamanını hedefleyen diller tarafından tanımlanan anahtar sözcükleri eşleşmelidir. Kullanılan dil ve anahtar sözcüğü bağlı olarak, derleyici hataları ve belirsizlikler kitaplığı kullanmak zorlaştırabilir.

 Bu kural, anahtar sözcükleri şu dillerde karşı denetler:

- Visual Basic

- C#

- C++/CLI

  Büyük küçük harf duyarsız bir karşılaştırma için kullanılan [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] anahtar sözcükleri ve büyük küçük harfe duyarlı karşılaştırma diğer diller için kullanılır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Anahtar sözcükler listesinde görünmeyen bir adı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Tanımlayıcı kullanıcılara API'nin karıştırır değil ve kitaplık tüm kullanılabilir dilde kullanılabilir olduğunu ikna varsa bu kuraldan bir uyarıyı bastırmak [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].
