---
title: IDebugBinder3::GetEEService | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBinder3::GetEEService
helpviewer_keywords:
- IDebugBinder3::GetEEService method
ms.assetid: eb07aa40-8cd9-4a52-a4c7-4affd2307a01
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bdc3470d07ebe8061a1e8b0c452cd55480af94c6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54926196"
---
# <a name="idebugbinder3geteeservice"></a>IDebugBinder3::GetEEService
Bu yöntem, istenen hizmeti döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetEEService(  
   [in] GUID        vendor,  
   [in] GUID        language,  
   [in] GUID        iid,  
   [out] IUnknown** ppService  
);  
```  
  
```csharp  
Int GetEEService(  
   Guid       vendor,  
   Guid       language,  
   Guid       iid,  
   out object ppService  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `vendor`  
 [in] `GUID` bir satıcının (bir null değer kabul edilebilir).  
  
 `language`  
 [in] `GUID` dilinin (bir null değer kabul edilebilir).  
  
 `iid`  
 [in] `IID` almak için hizmeti.  
  
 `ppService`  
 [out] İstenen hizmet için bir arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Geçirmek `IID` için [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md) arabirimi (`IID_IEEVisualizerServiceProvider`) tür görselleştiricisi hizmetin kullanılabilir olup olmadığını görmek için. Bu nedenle, ifade değerlendiricisi elde [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md) tür görselleştiricileri desteklemek için arabirim. Bkz: [Visualizing ve verileri görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md) Ayrıntılar için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)   
 [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)   
 [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)   
 [Verileri Görselleştirme ve Görüntüleme](../../../extensibility/debugger/visualizing-and-viewing-data.md)