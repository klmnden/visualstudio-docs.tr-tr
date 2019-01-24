---
title: Güvenlik sorunları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- security [Debugging SDK]
- debugging [Debugging SDK], security
ms.assetid: d6ffff0a-afb4-4f38-86d8-476c881c4e4b
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 874231333c87020c126eac4c066d53512ba0bbc9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752457"
---
# <a name="security-issues"></a>Güvenlik Sorunları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Visual Studio kullanarak bir programda hata ayıklamak için gerekli tek izinler programı çalıştırmak için bir geliştiricinin ihtiyaç duyduğu bilgilerle aynı değil. Bu, çoğu durum için (Internet bilgi hizmeti gibi diğer hizmetlerle ilgili bazı durumlarda, daha yüksek düzeyde izinleri gerektirebilir) uzaktan hata ayıklamayı içerir.  
  
 Visual Studio çalışırken, işlem hata ayıklama Yöneticisi (PDM) yerel makine üzerinde hata ayıklama işlemlerini izler. Uzaktan msvsmon.exe adlı bir program, uzaktan hata ayıklama işlemek ve PDM kullanılabilir hale getirmek için geliştirici tarafından başlatılır. (Unutmayın. msvsmon.exe'in hizmet değildir ve bu makinede uzaktan hata ayıklamayı etkinleştirmek için el ile başlatılması gerekir.) Visual Studio'nun (veya msvsmon.exe) çalışmadığında, hiçbir işlem hata ayıklama için izlenir.  
  
 Başka bir deyişle, bir geliştirici isterse, hiçbir özel izinlerle başlatılan programlar ayıklayabilirsiniz. Geliştirici, başka bir kişi aynı güvenlik grubunun bir üyesi ise başkası tarafından başlatılan işlemler bile hata ayıklaması yapabilirsiniz. Ve yalnızca gerekli kopyalamak için dosyaları uzak makine'ı ve msvsmon.exe Başlat uzaktan hata ayıklamayı etkinleştirmek için gerekli olur (bkz [ayarlanmış yukarı uzak Araçlar cihazda](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c) daha fazla ayrıntı için).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md)   
 [İşlem Hata Ayıklama Yöneticisi](../../extensibility/debugger/process-debug-manager.md)   
 [Cihazda uzak araçları ayarlama](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)
