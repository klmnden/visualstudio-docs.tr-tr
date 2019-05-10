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
ms.openlocfilehash: 1c09245056bf7e947985bfa55dc9cc4a3a96b8cf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62846280"
---
# <a name="message-codes"></a>İleti Kodları
Gösterilen her ileti satırı [iletiler görünümünü](../debugger/messages-view.md) içeren bir 'P,' kullanıcının,' ın,' veya 'R' kod. Bu kodları, aşağıdaki anlamlara sahiptir:

|Kod|Açıklama|
|----------|-------------|
|P|İleti kuyruğuyla deftere nakledilen **PostMessage** işlevi. Son Değerlendirme iletisinin ilgili hiçbir bilgi kullanılabilir.|
|S|İle gönderilen iletinin **SendMessage** işlevi. Başka bir deyişle, alıcı işler ve ileti döndürür kadar gönderen denetim gerekse değil. Alıcı bu nedenle, dönüş değeri gönderene geçirebilirsiniz.|
|s|İleti gönderildi ancak güvenlik dönüş değerini erişimi engeller.|
|R|Her bir kişinin ' satırı, ileti dönüş değerini listeler karşılık gelen bir 'R' (başı) satır içeriyor. Bazen, bir ileti işleyicisi başka bir ileti gönderir. yani ileti çağrıları yerleştirilir.|