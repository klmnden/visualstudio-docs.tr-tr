---
title: IDebugApplicationThread110::AsynchronousCallIntoThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 06b3031a-4aec-4a47-afaa-04642a4c4870
caps.latest.revision: 2
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fd9fe0b7177c95aec675faaaa85896c52b375084
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440550"
---
# <a name="idebugapplicationthread110asynchronouscallintothread"></a>IDebugApplicationThread110::AsynchronousCallIntoThread
Ana iş parçacığında zaman uyumsuz bir çağrı yapar.  
  
> [!IMPORTANT]
> [Idebugapplicationthread110 arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
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