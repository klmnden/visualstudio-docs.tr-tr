---
title: 'CA1030: Uygun yerlerde olayları kullanın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- UseEventsWhereAppropriate
- CA1030
helpviewer_keywords:
- CA1030
- UseEventsWhereAppropriate
ms.assetid: ea051367-deeb-40f9-9b65-eb818f1e133a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 89ee195da621ea9d7342302efadf582e21f7e619
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54956733"
---
# <a name="ca1030-use-events-where-appropriate"></a>CA1030: Uygun yerlerde olayları kullanın

|||
|-|-|
|TypeName|UseEventsWhereAppropriate|
|CheckId|CA1030|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Genel, korumalı veya özel yöntem adı aşağıdakilerden biri ile başlar:

- Eklenti fiyatı

- RemoveOn

- Ateş

- artırma

## <a name="rule-description"></a>Kural açıklaması
 Bu kural, normalde olaylar için kullanılan adlara sahip yöntemleri algılar. Olayları gözlemci ya da Yayımla-abone ol tasarım desenini izler; Bunlar, bir nesnede bir durum değişikliği diğer nesnelere iletileceği olduğunda kullanılır. Yanıt olarak açıkça tanımlanmış bir durum değişikliği bir yöntem çağrıldığında, bir olay işleyicisi tarafından yöntemin çağrılması gerekir. Yöntemi direkt olarak çağırmak yerine olayları yükselterek çağıran nesneler.

 Olayların bazı genel örnekleri burada bir düğmeye tıklanması gibi bir kullanıcı eylemi yürütmek için kod kesiminin neden olan kullanıcı arabirimi uygulamalarında bulunur. .NET Framework olay modeli için kullanıcı arabirimleri sınırlı değildir; bir veya daha fazla nesneye durum değişikliklerini iletişim kurması gereken herhangi bir yere kullanılmalıdır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bir nesnenin durumu değiştiğinde yöntemi çağrılırsa, .NET Framework olay modelini kullanmak için tasarım değiştirme düşünmelisiniz.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Yöntemi .NET Framework olay modeliyle çalışmazsa bu kuraldan bir uyarıyı gizler.