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
ms.openlocfilehash: c495357b837c4ae10d4dfe1e25237d6caaefcc4c
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233108"
---
# <a name="ca2004-remove-calls-to-gckeepalive"></a>CA2004: GC.KeepAlive'a çağrıları kaldırın

|||
|-|-|
|TypeName|RemoveCallsToGCKeepAlive|
|CheckId|CA2004|
|Kategori|Microsoft. güvenilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Sınıflar kullanır `SafeHandle` , ancak yine de `GC.KeepAlive`çağrıları içerir.

## <a name="rule-description"></a>Kural açıklaması
`SafeHandle` Kullanım alanına dönüştürüyorsanız tüm `GC.KeepAlive` (nesne) çağrılarını kaldırın. Bu durumda, bir sonlandırıcısının olmadığı varsayıldığında `GC.KeepAlive`, ancak işletim sistemi tanıtıcısını tamamlamaya yönelik açık `SafeHandle` olan, bu durumda sınıfların çağrı yapması gerekmez.  Bir çağrıda `GC.KeepAlive` bırakma maliyeti performansa göre ölçülerek göz ardı edilebilir olsa da, bir `GC.KeepAlive` çağrının, artık mevcut olmayan bir yaşam süresi sorununu gidermek için gerekli veya yeterli olduğunu düşünülüyor, kodu daha zor hale getirir korumanız.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Çağrıları `GC.KeepAlive`kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu uyarıyı yalnızca sınıfınızın `SafeHandle` kullanımına dönüştürmek için teknik olarak doğru değilse gizleyebilirsiniz.