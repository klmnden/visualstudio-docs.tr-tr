---
title: İleti kodları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- message codes
ms.assetid: 9f91f4e2-c1f1-4349-9f11-2fbbf59654be
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c3899da3b668406a701ce5c1c4935b531754d10e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55017090"
---
# <a name="message-codes"></a>İleti Kodları
Gösterilen her ileti satırı [iletiler görünümünü](../debugger/messages-view.md) içeren bir 'P,' kullanıcının,' ın,' veya 'R' kod. Bu kodları, aşağıdaki anlamlara sahiptir:  
  
|Kod|Açıklama|  
|----------|-------------|  
|P|İleti kuyruğuyla deftere nakledilen **PostMessage** işlevi. Son Değerlendirme iletisinin ilgili hiçbir bilgi kullanılabilir.|  
|S|İle gönderilen iletinin **SendMessage** işlevi. Başka bir deyişle, alıcı işler ve ileti döndürür kadar gönderen denetim gerekse değil. Alıcı bu nedenle, dönüş değeri gönderene geçirebilirsiniz.|  
|s|İleti gönderildi ancak güvenlik dönüş değerini erişimi engeller.|  
|R|Her bir kişinin ' satırı, ileti dönüş değerini listeler karşılık gelen bir 'R' (başı) satır içeriyor. Bazen, bir ileti işleyicisi başka bir ileti gönderir. yani ileti çağrıları yerleştirilir.|