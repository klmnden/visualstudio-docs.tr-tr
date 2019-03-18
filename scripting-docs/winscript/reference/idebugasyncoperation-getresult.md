---
title: IDebugAsyncOperation::GetResult | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 49cf761c85fce3f8fc2f6705d114ab042e0c2ecd
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58158006"
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