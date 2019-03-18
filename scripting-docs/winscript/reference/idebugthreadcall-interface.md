---
title: Idebugthreadcall arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 89f0fba2f5210cdcf4bb8f17443f948cb9ba1f4e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58149529"
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