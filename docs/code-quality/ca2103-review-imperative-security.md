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
ms.openlocfilehash: 7acbb9d0127dd2ddb6668e72db8fa88124ec2b3c
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921423"
---
# <a name="ca2103-review-imperative-security"></a>CA2103: Kesin temelli güvenliği gözden geçirin

|||
|-|-|
|TypeName|ReviewImperativeSecurity|
|CheckId|CA2103|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

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