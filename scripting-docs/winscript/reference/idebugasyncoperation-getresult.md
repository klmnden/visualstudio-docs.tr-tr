---
title: IDebugAsyncOperation::GetResult | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugAsyncOperation.GetResult
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugAsyncOperation::GetResult
ms.assetid: 56d43365-6b12-4213-a97c-953c40d7b7f6
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d86e9eb2b934bc6bd4027405d06960cd107f81c1
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087483"
---
# <a name="idebugasyncoperationgetresult"></a>IDebugAsyncOperation::GetResult
Zaman uyumlu hata ayıklama işlemi dönüş nesne parametresi ve dönüş değeri sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetResult(  
   HRESULT*    phrResult,  
   IUnknown**  ppunkResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `phrResult`  
 [out] İşlem tamamlandığında `phrResult` dönüş değeri `IDebugSyncOperation::Execute`.  
  
 `ppunkResult`  
 [out] İşlem tamamlandığında `ppunkResult` işlem tarafından döndürülen nesne parametresi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_PENDING`|İşlem tamamlanmadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 İşlem, tamamlandı, bu yöntemi döndürür `HRESULT` parametresinden nesneyi `IDebugSyncOperation::Execute`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugasyncoperation arabirimi](../../winscript/reference/idebugasyncoperation-interface.md)   
 [IDebugSyncOperation::Execute](../../winscript/reference/idebugsyncoperation-execute.md)