---
title: IEEVisualizerService::GetValueDisplayStringCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IEEVisualizerService::GetValueDisplayStringCount
- GetValueDisplayStringCount
ms.assetid: d683a833-fbfb-4042-84df-6905124a268a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5bb70d58cb2f419661253f4aab135bef91d3700b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54978509"
---
# <a name="ieevisualizerservicegetvaluedisplaystringcount"></a>IEEVisualizerService::GetValueDisplayStringCount
Belirtilen özellik veya alan için görüntülenecek değer dizeleri sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetValueDisplayStringCount (  
   DWORD         displayKind,   
   IDebugField * propertyOrField,   
   ULONG *       pcelt  
);  
```  
  
```csharp  
int GetValueDisplayStringCount (  
   uint        displayKind,   
   IDebugField propertyOrField,   
   out ulong   pcelt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `displayKind`  
 [in] Değerini [DisplayKind](../../../extensibility/debugger/reference/displaykind.md) sabit listesi.  
  
 `propertyOrField`  
 [in] Bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) bir özellik veya alan temsil eden arabirim.  
  
 `pcelt`  
 [out] Görüntülenecek değer dizeleri sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)