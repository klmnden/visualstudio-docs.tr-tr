---
title: Paket hatalarını ayıklama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], packages
ms.assetid: 99947fd4-fb87-4c69-b26c-65634e17d285
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4eb843e63dbc4ff711b56ff457ca930dc9df0207
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55010187"
---
# <a name="debug-package"></a>Paket hatalarını ayıklama
Hata ayıklama paketi, Visual Studio Kabuğu'nda çalışır ve tüm UI işler. Visual Studio hata ayıklama arabirimleri kullanır ve oturum hata ayıklama Yöneticisi (SDM) ile iletişim kurar.  
  
 SDM gönderilen break olayları kesme modu ve odağı sonu oluştuğu programın değiştirmek için hata ayıklayıcı çalışma modundan geçin. Hata ayıklama paketi olaylar tarafından gönderilen bilgileri yığın çerçevesi ve iş parçacığı izler.  
  
 Hata ayıklama paketi hiçbir dil veya çalışma zamanı ortamı bağımlılıkları vardır. Uygulama veya hata ayıklama paketi değiştirmek gerekli değildir.  
  
 Hata ayıklama paketi tarafından uygulanan *vsdebug.dll*.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Oturum hata ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md)   
 [Yığın çerçeveleri](../../extensibility/debugger/stack-frames.md)   
 [İş parçacıkları](../../extensibility/debugger/threads.md)   
 [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)