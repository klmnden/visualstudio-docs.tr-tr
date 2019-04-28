---
title: IDebugApplicationThread110::IsSuspendedForBreakPoint | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThread110::IsSuspendedForBreakPoint
ms.assetid: 60688222-557f-4a43-a19b-846cee393cd0
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 82b8957ae9f2b6674af7addf2239c745115e4e3f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440532"
---
# <a name="idebugapplicationthread110issuspendedforbreakpoint"></a>IDebugApplicationThread110::IsSuspendedForBreakPoint
Belirler olmadığını [IDebugApplicationThreadEvents110::OnSuspendForBreakPoint](../../winscript/reference/idebugapplicationthreadevents110-onsuspendforbreakpoint.md) bu iş parçacığı üzerinde çağrılmış var ve henüz tamamlanmadı.  
  
> [!IMPORTANT]
> [Idebugapplicationthread110 arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT IsSuspendedForBreakPoint([out, annotation("_Out_")] BOOL * pfIsSuspended);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pfIsSuspended`  
 [out] `true` iş parçacığı bir kesme noktası için Aksi takdirde askıda değilse `false`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThread110 Arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md)