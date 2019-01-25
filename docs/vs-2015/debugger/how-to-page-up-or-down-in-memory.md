---
title: 'Nasıl yapılır: Sayfa yukarı veya aşağı bellekte | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, paging up or down in memory
- memory, paging up or down
- Disassembly window, viewing memory space
- Memory window, paging up or down in memory
ms.assetid: 50b30a68-66f6-43f8-a48b-59ce12c95471
caps.latest.revision: 23
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 8859bac6f2cfe992c3c0d8005830985598934b88
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752479"
---
# <a name="how-to-page-up-or-down-in-memory"></a>Nasıl yapılır: Sayfa yukarı veya aşağı bellekte
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bellek içeriğini görüntülediğinizde bir **bellek** penceresi veya **ayrıştırılmış kodu** penceresinde bellek alanı yukarı veya aşağı taşımak için dikey kaydırma çubuğunu kullanabilirsiniz.  
  
### <a name="to-page-up-or-down-in-memory"></a>Yukarı veya aşağı bellekte sayfa için  
  
1. Page DOWN (daha yüksek bir bellek adresi taşıma) için dikey bir kaydırma çubuğuna ait kaydırma kutusunun altındaki'ı tıklatın.  
  
2. (Daha düşük bir bellek adresi taşıma) ayarlama sayfası için thumb yukarıda dikey kaydırma çubuğunu tıklayın.  
  
   Ayrıca dikey kaydırma çubuğu standart olmayan bir şekilde çalıştığını görürsünüz. Çok büyük modern bir bilgisayarın adres alanı ve kaydırma çubuğunun Kaydırma kutusu yazılımdır ve rastgele bir konuma sürükleyerek kayıp kolaydır. Bu nedenle, thumb "springloaded" olduğundan ve her zaman kaydırma çubuğunu Merkezi'nde kalır. Yerel kod uygulamalarında yukarı veya aşağı sayfa ancak hakkında ücretsiz kaydırma yapılamıyor.  
  
   Yönetilen uygulamalarda Ayrıştırılmış kod bir işleve sınırlıdır ve normalde gezinebilirsiniz.  
  
   Daha büyük adresleri penceresinin en altında göründüğünü fark edeceksiniz. Daha yüksek bir adresi görüntülemek için aşağı, en fazla değil taşımanız gerekir.  
  
#### <a name="to-move-up-or-down-one-instruction"></a>Bir yönerge aşağı veya yukarı taşımak için  
  
-   Dikey kaydırma çubuğu ortasından altına veya üstüne oka tıklayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bellek Windows](../debugger/memory-windows.md)   
 [Nasıl yapılır: Ayrıştırılmış kod penceresini kullanma](../debugger/how-to-use-the-disassembly-window.md)   
 [Hata Ayıklayıcıda Verileri Görüntüleme](../debugger/viewing-data-in-the-debugger.md)
