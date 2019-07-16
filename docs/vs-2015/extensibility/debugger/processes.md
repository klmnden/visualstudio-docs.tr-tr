---
title: İşlemler | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], processes
ms.assetid: a6a1efdc-b243-40c8-a778-6f69f6b018be
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 82718a7ceb7a18f9978840f35ca0c5fce5628e81
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153661"
---
# <a name="processes"></a>İşlemler
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **işlem**:  
  
- Bir dizi program için bir kapsayıcıdır. Bu iş parçacığı bir dizi için bir kapsayıcı bir Windows işlem yakından benzerdir.  
  
- Kendisini adı, tanımlayıcı veya fiziksel tanımlayıcısı tarafından tespit edebilirsiniz.  
  
- Tüm çalışan programları (ve bunların iş parçacıkları) sıralayabilirsiniz.  
  
- Kendisi, içinde çalıştığı bağlantı noktası ve içerdiği makine tanımlayabilirsiniz.  
  
- Bir tane oluşturabilirsiniz veya daha fazla program oluşturduğu programlardan herhangi biriyle sonlandırmak veya bir programın durmasına neden.  
  
- Tarafından temsil edilen bir [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md) işlemi başlatıldığında oluşturulduğu arabirimi. Bir işlem ya da oturum hata ayıklama Yöneticisi tarafından (SDM) başlatılmadı veya [LaunchSuspended](../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md).  
  
  Hata ayıklama paketi bir hata ayıklama altyapısı (DE) bir işleme çağırarak iliştirilebilir [iliştirme](../../extensibility/debugger/reference/idebugprocess2-attach.md). Bu, işleyebileceği işlemde çalışan tüm olası programlara ekler DE anlamına gelir. Örneğin, ortak dil çalışma zamanı DE bir işleme iliştirir, yönetilen kod çalışan programlar ekler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Programlar](../../extensibility/debugger/programs.md)   
 [İş parçacıkları](../../extensibility/debugger/threads.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Paket hatalarını ayıklama](../../extensibility/debugger/debug-package.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [IDebugProcess2](../../extensibility/debugger/reference/idebugprocess2.md)   
 [LaunchSuspended](../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)   
 [Attach](../../extensibility/debugger/reference/idebugprocess2-attach.md)
