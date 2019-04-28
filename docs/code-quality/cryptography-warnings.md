---
title: Şifreleme Uyarıları
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: d96723ea-a293-488d-b9db-adb437e50cdd
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 669b7806e01772e6a871b6c6a9bf47907cf9a5a4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62816594"
---
# <a name="cryptography-warnings"></a>Şifreleme Uyarıları
Şifreleme uyarıları daha güvenli kütüphaneleri ve şifreleme aracılığıyla doğru uygulamaları destekler. Bu uyarılar, programınızdaki güvenlik açıklarını önlemeye yardımcı olur. Bu uyarılardan birini devre dışı bırakırsanız, bunun sebebini kodunuzda açıkça işaretlemelisiniz ve ayrıca geliştirme projeniz için güvenlik çalışanını bilgilendirmelisiniz.

|Kural|Açıklama|
|----------|-----------------|
|[CA5350: Zayıf şifreleme algoritmaları kullanmayın](../code-quality/ca5350-do-not-use-weak-cryptographic-algorithms.md)|Zayıf şifreleme algoritmalarını ve karma işlevler bir dizi nedenden ötürü bugün kullanılır, ancak bunlar bunların koruduğu veri bütünlüğü ve gizliliği güvence altına almak için kullanılmamalıdır.        Kodda TripleDES, SHA1 veya RIPEMD160 algoritmaları bulduğunda bu kural tetiklenir.|
|[CA5351: Bozuk Şifreleme Algoritmaları Kullanmayın](../code-quality/ca5351-do-not-use-broken-cryptographic-algorithms.md)|Bozuk şifreleme algoritmaları güvenli kabul edilmeyen ve bunların kullanılması kesinlikle önerilmez. Bu kodda DES veya RC2 şifreleme algoritmaları ve MD5 karma algoritması bulduğunda bu kural tetikler.|