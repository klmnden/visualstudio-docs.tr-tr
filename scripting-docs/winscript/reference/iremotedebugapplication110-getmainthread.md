---
title: IRemoteDebugApplication110::GetMainThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IRemoteDebugApplication110::GetMainThread
ms.assetid: 9982acc9-3d35-4dcf-8ca9-662469de4072
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 20d895f8bd6d4919def00625e9f285afdfe4f866
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349874"
---
# <a name="iremotedebugapplication110getmainthread"></a>IRemoteDebugApplication110::GetMainThread
Ana iş parçacığı çağrı konakları için döndürür [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439), aksi takdirde E_FAIL döndürür.  
  
> [!IMPORTANT]
>  [Iremotedebugapplication arabirimi](../../winscript/reference/iremotedebugapplication-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetMainThread([out] IRemoteDebugApplicationThread **ppThread);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppThread`  
 [out] Ana [Iremotedebugapplicationthread arabirimi](../../winscript/reference/iremotedebugapplicationthread-interface.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Iremotedebugapplication arabirimi](../../winscript/reference/iremotedebugapplication-interface.md)   
 [IRemoteDebugApplication110 Arabirimi](../../winscript/reference/iremotedebugapplication110-interface.md)