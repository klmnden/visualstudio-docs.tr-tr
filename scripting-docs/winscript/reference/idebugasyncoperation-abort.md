---
title: IDebugAsyncOperation::Abort | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugAsyncOperation.Abort
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugAsyncOperation::Abort
ms.assetid: 232541c6-81b8-4eb7-96a7-a8e5fe087b31
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: af8b063f86bd08f293518b1494b41e4f01d61b2c
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093320"
---
# <a name="idebugasyncoperationabort"></a>IDebugAsyncOperation::Abort
Bir işlem iptal eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Abort();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|S_OK|Yöntem başarılı oldu.|  
|E_NOTIMPL|İşlem iptal edilemez.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem genellikle bir yanıt işlemi iptal etmek için hata ayıklayıcı iş parçacığı içinde çağrılır. Bu yöntem neden `InProgressAbort` metodunda `IDebugSyncOperation` çağrılacak nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugasyncoperation arabirimi](../../winscript/reference/idebugasyncoperation-interface.md)   
 [IDebugAsyncOperation::Start](../../winscript/reference/idebugasyncoperation-start.md)   
 [IDebugSyncOperation::InProgressAbort](../../winscript/reference/idebugsyncoperation-inprogressabort.md)