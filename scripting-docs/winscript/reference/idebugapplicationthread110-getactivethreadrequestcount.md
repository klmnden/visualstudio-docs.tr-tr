---
title: IDebugApplicationThread110::GetActiveThreadRequestCount | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationThread110::GetActiveThreadRequestCount
ms.assetid: 025d2072-1d7f-4448-8aa3-38a014313570
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d9bda0cc59560d90ebc0a382d858c881e7372c15
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58145076"
---
# <a name="idebugapplicationthread110getactivethreadrequestcount"></a>IDebugApplicationThread110::GetActiveThreadRequestCount
İş parçacığı istek sayısı, şu anda işlenmekte olan mekanizmaları geçiş PDM'ın iş parçacığından döndürür. Bu sayı genellikle 0 veya 1 olur. Bir iş parçacığı çağrı işlemeye başlıyor ancak iş parçacığı dışında bir zaman uyumlu çağrıyı tetikler veya aksi halde iş parçacığını askıya alır ve yeniden işlenmek üzere gelen çağrıları sağlar ancak sayı daha yüksek olabilir (örneğin, tetikleme tarafından bir [ Iremotedebugapplicationevents arabirimi](../../winscript/reference/iremotedebugapplicationevents-interface.md) hata ayıklayıcı iş parçacığı üzerinde veren olay).  
  
> [!IMPORTANT]
>  [Idebugapplicationthread110 arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetActiveThreadRequestCount([out, annotation("_Out_")] UINT * puiThreadRequests);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `puiThreadRequests`  
 [out] İş parçacığı isteklerinin sayısı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThread110 Arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md)