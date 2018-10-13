---
title: Kendi İşaretçilerimin Bellek Adresini Bozup Bozmadığını Nasıl Anlarım? | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- addresses, pointers corrupting memory address
- memory, corruption
- pointers, corrupting memory addresses
- memory address corruption by pointers
- debugging [C++], memory corruption
- corrupted memory address
ms.assetid: a147c939-4fb1-415c-8410-cf303781e9e8
caps.latest.revision: 22
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04df8c5dfc0d6fbf57183cf90ab0fd8a4fc79686
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49217335"
---
# <a name="how-can-i-find-out-if-my-pointers-corrupt-a-memory-address"></a>Kendi İşaretçilerimin Bellek Adresini Bozup Bozmadığını Nasıl Anlarım?
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sorun açıklaması  
 İşaretçilerimden birinin 0x00408000 adresinde belleği bozabileceğini düşünüyorum. Nasıl öğrenebilirim orada neler olduğunu kullanıma?  
  
## <a name="solution"></a>Çözüm  
  
#### <a name="check-for-heap-corruption"></a>Yığın bozulmasını denetleme  
  
-   Çoğu Bellek Bozulması gerçekten Öbek Bozulması nedeniyledir ' dir. Genel bayraklar yardımcı programı'nı (gflags.exe) veya pageheap.exe'yi kullanmayı deneyin. Bkz: [ http://support.microsoft.com/default.aspx?scid=kb; en-us; 286470](http://support.microsoft.com/default.aspx?scid=kb;en-us;286470).  
  
#### <a name="to-find-where-the-memory-address-is-modified"></a>Bellek adresinin nerede değiştirildiğini bulmak için  
  
1.  0x00408000 veri kesme noktası ayarlayın. Bkz: [veri değişikliği kesme noktası (yalnızca yerel C++'da) ayarla](../debugger/using-breakpoints.md#BKMK_set_a_data_breakpoint_native_cplusplus_only).  
  
2.  Kesme noktasına ulaştığınızda kullanın **bellek** bellek görüntülemek için pencere içeriği 0x00408000 başlatılıyor. Daha fazla bilgi için [bellek Windows](../debugger/memory-windows.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yerel kod hata ayıklaması SSS](../debugger/debugging-native-code-faqs.md)   
 [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)



