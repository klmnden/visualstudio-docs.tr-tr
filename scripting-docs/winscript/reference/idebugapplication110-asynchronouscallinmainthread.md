---
title: IDebugApplication110::AsynchronousCallInMainThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplication110::AsynchronousCallInMainThread
ms.assetid: 13b80ff0-4bed-48c1-8031-d4147b51bf6c
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6e3f98ff917475f0f0733163862ff20ef56f04bb
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344128"
---
# <a name="idebugapplication110asynchronouscallinmainthread"></a>IDebugApplication110::AsynchronousCallInMainThread
Ana iş parçacığında zaman uyumsuz bir çağrı yapar.  
  
> [!IMPORTANT]
>  [Idebugapplication110 arabirimi](../../winscript/reference/idebugapplication110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT AsynchronousCallInMainThread([in] IDebugThreadCall* pptc, [in] DWORD_PTR dwParam1, [in] DWORD_PTR dwParam2, [in] DWORD_PTR dwParam3);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pptc`  
 [Idebugthreadcall arabirimi](../../winscript/reference/idebugthreadcall-interface.md) aranacak nesne.  
  
 `dwParam1`  
 Çağrısının ilk parametresi.  
  
 `dwParam1`  
 Çağrısının ilk parametresi.  
  
 `dwParam2`  
 Çağrı, ikinci parametre.  
  
 `dwParam3`  
 Çağrı'öğesinin üçüncü parametresi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication110 Arabirimi](../../winscript/reference/idebugapplication110-interface.md)