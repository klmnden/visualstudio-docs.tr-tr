---
title: Yerel kod iş parçacıklarında hata ayıklama ipuçları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], threads
ms.assetid: 0374c8c6-57a3-4cfe-8047-2effef5ff5dc
caps.latest.revision: 25
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2c4bed2506fef0c4f066e58e158b062c2a6b39aa
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60074183"
---
# <a name="tips-for-debugging-threads-in-native-code"></a>Yerel Kod İş Parçacıklarında Hata Ayıklama İpuçları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yerel kod iş parçacıklarında hata ayıklama sırasında kullanabileceğiniz bazı ipuçları şunlardır:  
  
- Yazarak iş parçacığı bilgileri bloğu içeriğini görüntüleyebilirsiniz `@TIB` içinde **Watch** penceresi veya **QuickWatch** iletişim kutusu.  
  
- Geçerli iş parçacığı için son hata kodunu girerek görüntüleyebileceğiniz `@Err` içinde **Watch** penceresi veya **QuickWatch** iletişim kutusu.  
  
- C çalışma zamanı kitaplıkları (CRT) işlevleri, çok iş parçacıklı uygulamada hata ayıklama için yararlı olabilir. Daha fazla bilgi için [_malloc_dbg](http://msdn.microsoft.com/library/c97eca51-140b-4461-8bd2-28965b49ecdb).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çok iş parçacıklı uygulamalarda hata ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)
