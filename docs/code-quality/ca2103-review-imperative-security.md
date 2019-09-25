---
title: 'CA2103: Kesin temelli güvenliği gözden geçirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2103
- ReviewImperativeSecurity
helpviewer_keywords:
- CA2103
- ReviewImperativeSecurity
ms.assetid: d24fde71-bdf6-46c0-8965-9a73dc33c1aa
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a2792f1cccad26fe5bb073af800a2fcf0ebcb4b4
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232979"
---
# <a name="ca2103-review-imperative-security"></a>CA2103: Kesin temelli güvenliği gözden geçirin

|||
|-|-|
|TypeName|ReviewImperativeSecurity|
|CheckId|CA2103|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir yöntem zorunlu güvenliği kullanır ve durum bilgileri veya dönüş değerlerini kullanarak izin oluşturursa, izin talebi etkin durumdayken değişebilir.

## <a name="rule-description"></a>Kural açıklaması
Zorunlu güvenlik, kod yürütme sırasında izinleri ve güvenlik eylemlerini belirtmek için yönetilen nesneleri kullanır ve meta verilerde izinleri ve eylemleri depolamak için öznitelikler kullanır. Zorunlu güvenlik, bir izin nesnesinin durumunu ayarlayabilmeniz ve çalışma zamanına kadar kullanılamayan bilgileri kullanarak güvenlik eylemleri seçeceğinden çok esnektir. Bu esneklikle birlikte, bir iznin durumunu belirlemede kullandığınız çalışma zamanı bilgilerinin, eylem yürürlükte olduğu sürece değişmeden kalmayacağı riski vardır.

Bildirime dayanan güvenliği mümkün olduğunca kullanın. Bildirim temelli taleplerin anlaşılması daha kolay.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
İzin durumunun kullanıldığı sürece değişebilir bilgilere dayanmadığından emin olmak için, zorunlu güvenlik taleplerini gözden geçirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
İzin değişen verilere bağlı değilse, bu kuraldan bir uyarı bastırması güvenlidir. Ancak, zorunlu talebin bildirime dayalı eşdeğerini değiştirmek daha iyidir.

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
- [Veri ve Modelleme](/dotnet/framework/data/index)