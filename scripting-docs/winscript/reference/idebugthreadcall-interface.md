---
title: Idebugthreadcall arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugThreadCall interface
ms.assetid: 9a9a9892-f310-4ef3-8db2-4f868be52d7e
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a2167538f2251d961dfcad4a873658d9635a612e
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346273"
---
# <a name="idebugthreadcall-interface"></a>IDebugThreadCall Arabirimi
`IDebugThreadCall` Arabirimi iş parçacıkları arası çağrılar ile bir bileşen tarafından uygulanan genellikle `IDebugThread` işlem hata ayıklama Yöneticisi (PDM) tarafından sağlanan uygulama taşıma.  
  
 PDM çağrıları `IDebugThreadCall` istenen iş parçacığı, arabirimi ve `IDebugThreadCall` arabirimi çağrısı istenen uygulamaya gönderir. `IDebugThreadCall` Arabirimi yayınlar için uygun üst parametrelerinde geçirilen parametre bilgileri.  
  
 `IDebugThreadCall` Arabirimidir ücretsiz iş parçacıklı bir nesne.  
  
## <a name="methods"></a>Yöntemler  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugThreadCall` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugThreadCall::ThreadCallHandler](../../winscript/reference/idebugthreadcall-threadcallhandler.md)|Başka bir iş parçacığında kod çalıştırmak için çağrılar işler.|