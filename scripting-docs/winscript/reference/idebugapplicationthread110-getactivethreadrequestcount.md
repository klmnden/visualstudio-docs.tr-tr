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
ms.openlocfilehash: 3df2f0c44e42cf9e2c2aa846db4b88821fd73996
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63440564"
---
# <a name="idebugapplicationthread110getactivethreadrequestcount"></a>IDebugApplicationThread110::GetActiveThreadRequestCount
İş parçacığı istek sayısı, şu anda işlenmekte olan mekanizmaları geçiş PDM'ın iş parçacığından döndürür. Bu sayı genellikle 0 veya 1 olur. Bir iş parçacığı çağrı işlemeye başlıyor ancak iş parçacığı dışında bir zaman uyumlu çağrıyı tetikler veya aksi halde iş parçacığını askıya alır ve yeniden işlenmek üzere gelen çağrıları sağlar ancak sayı daha yüksek olabilir (örneğin, tetikleme tarafından bir [ Iremotedebugapplicationevents arabirimi](../../winscript/reference/iremotedebugapplicationevents-interface.md) hata ayıklayıcı iş parçacığı üzerinde veren olay).  
  
> [!IMPORTANT]
> [Idebugapplicationthread110 arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetActiveThreadRequestCount([out, annotation("_Out_")] UINT * puiThreadRequests);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `puiThreadRequests`  
 [out] İş parçacığı isteklerinin sayısı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationThread110 Arabirimi](../../winscript/reference/idebugapplicationthread110-interface.md)