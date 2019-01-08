---
title: IDebugAsyncOperation::Start | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 099e256496278a33ccae77351641cfdd23447b1f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094789"
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