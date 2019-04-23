---
title: 'Nasıl yapılır: Sayfa yukarı veya aşağı bellekte | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugger, paging up or down in memory
- memory, paging up or down
- Disassembly window, viewing memory space
- Memory window, paging up or down in memory
ms.assetid: 50b30a68-66f6-43f8-a48b-59ce12c95471
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4b8452100eb744d019c0f4c8d5e62566ac761210
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60072754"
---
# <a name="how-to-page-up-or-down-in-memory"></a>Nasıl yapılır: Sayfa yukarı veya aşağı bellekte

Bellek içeriğini görüntülediğinizde bir **bellek** penceresi veya **ayrıştırılmış kodu** penceresinde bellek alanı yukarı veya aşağı taşımak için dikey kaydırma çubuğunu kullanabilirsiniz.

### <a name="to-page-up-or-down-in-memory"></a>Yukarı veya aşağı bellekte sayfa için

1. Page DOWN (daha yüksek bir bellek adresi taşıma) için dikey bir kaydırma çubuğuna ait kaydırma kutusunun altındaki'ı tıklatın.

2. (Daha düşük bir bellek adresi taşıma) ayarlama sayfası için thumb yukarıda dikey kaydırma çubuğunu tıklayın.

   Ayrıca dikey kaydırma çubuğu standart olmayan bir şekilde çalıştığını görürsünüz. Çok büyük modern bir bilgisayarın adres alanı ve kaydırma çubuğunun Kaydırma kutusu yazılımdır ve rastgele bir konuma sürükleyerek kayıp kolaydır. Bu nedenle, thumb "springloaded" olduğundan ve her zaman kaydırma çubuğunu Merkezi'nde kalır. Yerel kod uygulamalarında yukarı veya aşağı sayfa ancak hakkında ücretsiz kaydırma yapılamıyor.

   Yönetilen uygulamalarda Ayrıştırılmış kod bir işleve sınırlıdır ve normalde gezinebilirsiniz.

   Daha büyük adresleri penceresinin en altında göründüğünü fark edeceksiniz. Daha yüksek bir adresi görüntülemek için aşağı, en fazla değil taşımanız gerekir.

#### <a name="to-move-up-or-down-one-instruction"></a>Bir yönerge aşağı veya yukarı taşımak için

- Dikey kaydırma çubuğu ortasından altına veya üstüne oka tıklayın.

## <a name="see-also"></a>Ayrıca Bkz.
- [Bellek Pencereleri](../debugger/memory-windows.md)
- [Nasıl yapılır: Ayrıştırılmış Kod Penceresini Kullanma](../debugger/how-to-use-the-disassembly-window.md)
- [Hata Ayıklayıcıda Verileri Görüntüleme](../debugger/viewing-data-in-the-debugger.md)