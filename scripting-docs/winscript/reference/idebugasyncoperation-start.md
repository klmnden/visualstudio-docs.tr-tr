---
title: IDebugAsyncOperation::Start | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugAsyncOperation.Start
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugAsyncOperation::Start
ms.assetid: a7272364-28e0-48ae-8405-b8bce8a6b9fd
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b3e02869abab65878412f96b77d5782b9717a1b6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62821934"
---
# <a name="idebugasyncoperationstart"></a>IDebugAsyncOperation::Start
Başlamak zaman uyumsuz işlem neden olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Start(  
   IDebugAsyncOperationCallBack*  padocb  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `padocb`  
 Bu işlemden durumu olaylarını alır geri çağırma arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_UNEXPECTED`|Bir işlem zaten beklemede.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem neden `IDebugSyncOperation::Execute` alınan iş parçacığında zaman uyumsuz olarak çağrılan `IDebugSyncOperation::GetTargetThread`. Bu yöntem yalnızca hata ayıklayıcı iş parçacığının içinden çağrılmalıdır; Aksi takdirde işlemi tamamlanana kadar bu döndürmez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugAsyncOperation::Abort](../../winscript/reference/idebugasyncoperation-abort.md)   
 [Idebugasyncoperation arabirimi](../../winscript/reference/idebugasyncoperation-interface.md)   
 [IDebugSyncOperation::Execute](../../winscript/reference/idebugsyncoperation-execute.md)   
 [IDebugSyncOperation::GetTargetThread](../../winscript/reference/idebugsyncoperation-gettargetthread.md)