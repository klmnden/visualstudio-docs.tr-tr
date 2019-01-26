---
title: İşlemler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], processes
ms.assetid: a6a1efdc-b243-40c8-a778-6f69f6b018be
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 85cfadc626ac28061ec91da2ea1c0d9c063994bb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54948208"
---
# <a name="processes"></a>İşlemler
Hata ayıklayıcı mimarisinde bir *işlem*:  
  
- Bir dizi program için bir kapsayıcıdır. Bu iş parçacığı bir dizi için bir kapsayıcı bir Windows işlem yakından benzerdir.  
  
- Kendisini adı, tanımlayıcı veya fiziksel tanımlayıcısı tarafından tespit edebilirsiniz.  
  
- Tüm çalışan programları (ve bunların iş parçacıkları) sıralayabilirsiniz.  
  
- Kendisi, içinde çalıştığı bağlantı noktası ve içerdiği makine tanımlayabilirsiniz.  
  
- Bir tane oluşturabilirsiniz veya daha fazla program oluşturduğu programlardan herhangi biriyle sonlandırmak veya bir programın durmasına neden.  
  
- Tarafından temsil edilen bir [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md) işlemi başlatıldığında oluşturulduğu arabirimi. Bir işlem ya da oturum hata ayıklama Yöneticisi tarafından (SDM) başlatılmadı veya [LaunchSuspended](../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md).  
  
  Hata ayıklama paketi bir hata ayıklama altyapısı (DE) bir işleme çağırarak iliştirilebilir [iliştirme](../../extensibility/debugger/reference/idebugprocess2-attach.md), işleyebileceği işlemde çalışan tüm olası programlar için DE bağlayan anlamına gelir. Örneğin, ortak dil çalışma zamanı DE bir işleme iliştirir, yönetilen kod çalışan programlar ekler.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Programlar](../../extensibility/debugger/programs.md)   
 [İş parçacıkları](../../extensibility/debugger/threads.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Paket hatalarını ayıklama](../../extensibility/debugger/debug-package.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md)   
 [LaunchSuspended](../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)   
 [Attach](../../extensibility/debugger/reference/idebugprocess2-attach.md)