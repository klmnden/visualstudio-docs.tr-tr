---
title: 'CA1030: uygun yerlerde olaylar kullanın | Microsoft Docs'
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
- UseEventsWhereAppropriate
- CA1030
helpviewer_keywords:
- CA1030
- UseEventsWhereAppropriate
ms.assetid: ea051367-deeb-40f9-9b65-eb818f1e133a
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f4f318c747f6408e44546a04054ad1e534ebd9dc
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296523"
---
# <a name="ca1030-use-events-where-appropriate"></a>CA1030: Uygun yerlerde olaylar kullanın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]
|||
|-|-|
|TypeName|UseEventsWhereAppropriate|
|CheckId|CA1030|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Genel, korumalı veya özel yöntem adı aşağıdakilerden biri ile başlar:

-   Eklenti fiyatı

-   RemoveOn

-   Ateş

-   artırma

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, normalde olaylar için kullanılan adlara sahip yöntemleri algılar. Olayları gözlemci ya da Yayımla-abone ol tasarım desenini izler; Bunlar, bir nesnede bir durum değişikliği diğer nesnelere iletileceği olduğunda kullanılır. Yanıt olarak açıkça tanımlanmış bir durum değişikliği bir yöntem çağrıldığında, bir olay işleyicisi tarafından yöntemin çağrılması gerekir. Yöntemi direkt olarak çağırmak yerine olayları yükselterek çağıran nesneler.

 Olayların bazı genel örnekleri burada bir düğmeye tıklanması gibi bir kullanıcı eylemi yürütmek için kod kesiminin neden olan kullanıcı arabirimi uygulamalarında bulunur. [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] Olay modeli için kullanıcı arabirimleri sınırlı değil; bunu her yerden, iletişim kurması gereken durumu değiştirir. bir veya daha fazla nesneye kullanılmalıdır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bir nesnenin durumu değiştiğinde yöntemi çağrılırsa, kullanılacak tasarım değiştirme düşünmelisiniz [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] olay modeli.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Yöntem ile çalışmazsa bu kuraldan bir uyarıyı bastırmak [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] olay modeli.



