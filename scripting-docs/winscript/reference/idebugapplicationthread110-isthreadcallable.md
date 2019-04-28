---
title: IDebugApplicationThread110::IsThreadCallable | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThread110::IsThreadCallable
ms.assetid: 2a75a366-801d-47e0-bba3-51aa669e03a7
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 90f0010a513adef67af1285ac15bc35d4573df57
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440521"
---
# <a name="idebugapplicationthread110isthreadcallable"></a>IDebugApplicationThread110::IsThreadCallable
Bu iş parçacığı PDM'ın iş parçacığı SynchronousCallInThread rehberlik gibi keşif mekanizmaları geçiş kullanarak yapılan çağrılar işleyecek bir durumda olup olmadığını belirler.  
  
> [!IMPORTANT]
> [Idebugapplicationthread110 arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT IsThreadCallable([out, annotation("_Out_")] BOOL * pfIsCallable);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pfIsCallable`  
 [out] `true` iş parçacığı çağrılabilir, yanlışsa `false`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThread110 Arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md)