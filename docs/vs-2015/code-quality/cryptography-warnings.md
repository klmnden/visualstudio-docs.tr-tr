---
title: Şifreleme uyarıları | Microsoft Docs
ms.date: 11/15/2016
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
ms.assetid: d96723ea-a293-488d-b9db-adb437e50cdd
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c573d461b477bbcdc7e988ea66f03d5a7cc0fdb6
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54833893"
---
# <a name="cryptography-warnings"></a>Şifreleme Uyarıları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Şifreleme uyarıları daha güvenli kütüphaneleri ve şifreleme aracılığıyla doğru uygulamaları destekler. Bu uyarılar, programınızdaki güvenlik açıklarını önlemeye yardımcı olur. Bu uyarılardan birini devre dışı bırakırsanız, bunun sebebini kodunuzda açıkça işaretlemelisiniz ve ayrıca geliştirme projeniz için güvenlik çalışanını bilgilendirmelisiniz.  
  
|Kural|Açıklama|  
|----------|-----------------|  
|[CA5350: Zayıf şifreleme algoritmaları kullanmayın](../code-quality/ca5350-do-not-use-weak-cryptographic-algorithms.md)|Zayıf şifreleme algoritmalarını ve karma işlevler bir dizi nedenden ötürü bugün kullanılır, ancak bunlar bunların koruduğu veri bütünlüğü ve gizliliği güvence altına almak için kullanılmamalıdır.        Kodda TripleDES, SHA1 veya RIPEMD160 algoritmaları bulduğunda bu kural tetiklenir.|  
|[CA5351: Bozuk Şifreleme Algoritmaları Kullanmayın](../code-quality/ca5351-do-not-use-broken-cryptographic-algorithms.md)|Bozuk şifreleme algoritmaları güvenli kabul edilmeyen ve bunların kullanılması kesinlikle önerilmez. Bu kodda DES veya RC2 şifreleme algoritmaları ve MD5 karma algoritması bulduğunda bu kural tetikler.|
