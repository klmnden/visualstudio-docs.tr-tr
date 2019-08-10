---
title: "CA2004: GC.KeepAlive'a çağrıları kaldırın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- RemoveCallsToGCKeepAlive
- CA2004
helpviewer_keywords:
- RemoveCallsToGCKeepAlive
- CA2004
ms.assetid: bc543b5b-23eb-4b45-abc2-9325cd254ac2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a716da8eb0fb1b741c302ed32408e63a4933567b
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921128"
---
# <a name="ca2004-remove-calls-to-gckeepalive"></a>CA2004: GC.KeepAlive'a çağrıları kaldırın

|||
|-|-|
|TypeName|RemoveCallsToGCKeepAlive|
|CheckId|CA2004|
|Kategori|Microsoft. güvenilirliği|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Sınıflar kullanır `SafeHandle` , ancak yine de `GC.KeepAlive`çağrıları içerir.

## <a name="rule-description"></a>Kural açıklaması
`SafeHandle` Kullanım alanına dönüştürüyorsanız tüm `GC.KeepAlive` (nesne) çağrılarını kaldırın. Bu durumda, bir sonlandırıcısının olmadığı varsayıldığında `GC.KeepAlive`, ancak işletim sistemi tanıtıcısını tamamlamaya yönelik açık `SafeHandle` olan, bu durumda sınıfların çağrı yapması gerekmez.  Bir çağrıda `GC.KeepAlive` bırakma maliyeti performansa göre ölçülerek göz ardı edilebilir olsa da, bir `GC.KeepAlive` çağrının, artık mevcut olmayan bir yaşam süresi sorununu gidermek için gerekli veya yeterli olduğunu düşünülüyor, kodu daha zor hale getirir korumanız.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Çağrıları `GC.KeepAlive`kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu uyarıyı yalnızca sınıfınızın `SafeHandle` kullanımına dönüştürmek için teknik olarak doğru değilse gizleyebilirsiniz.