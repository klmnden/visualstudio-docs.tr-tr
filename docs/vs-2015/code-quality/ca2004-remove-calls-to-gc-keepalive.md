---
title: 'CA2004: GC kaldırın. KeepAlive | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- RemoveCallsToGCKeepAlive
- CA2004
helpviewer_keywords:
- RemoveCallsToGCKeepAlive
- CA2004
ms.assetid: bc543b5b-23eb-4b45-abc2-9325cd254ac2
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e75ab22212945e5a6b4465e1e1f64ca48a9daa4a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68189050"
---
# <a name="ca2004-remove-calls-to-gckeepalive"></a>CA2004: GC.KeepAlive'a çağrıları kaldırın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|RemoveCallsToGCKeepAlive|
|CheckId|CA2004|
|Kategori|Microsoft.Reliability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Sınıfları kullanın `SafeHandle` ancak yine de çağrıları içeren `GC.KeepAlive`.

## <a name="rule-description"></a>Kural Tanımı
 İçin dönüştürüyorsanız `SafeHandle` kullanım, tüm çağrıları kaldırın `GC.KeepAlive` (nesne). Bu durumda, sınıflar çağrı yapmamalıdır `GC.KeepAlive`, bir sonlandırıcı olmayan ancak dayanır varsayılarak `SafeHandle` kendileri için işletim sistemini tamamlanması.  Ancak bir çağrıda bırakmanın maliyeti `GC.KeepAlive` ölçülen performans, perception Önemsiz olabilir, çağrı `GC.KeepAlive` gerekli ya da artık mevcut olabilecek bir sorunu kod için daha zor yapar bir ömrü çözmek yeterli korur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Kaldırın `GC.KeepAlive`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Yalnızca dönüştürmek teknik olarak doğru değilse, bu uyarının gösterilmemesi `SafeHandle` sınıfınıza kullanımı.
