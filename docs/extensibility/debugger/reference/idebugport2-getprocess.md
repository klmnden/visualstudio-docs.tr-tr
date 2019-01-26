---
title: IDebugPort2::GetProcess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPort2::GetPortSupplier
helpviewer_keywords:
- IDebugPort2::GetPortSupplier
ms.assetid: 3e2431b0-0e19-450d-8e1d-d7c314c8f872
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 68beeb8267116885a0e2a3026f5b0e36a65f7b9c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55007444"
---
# <a name="idebugport2getprocess"></a>IDebugPort2::GetProcess
Bir bağlantı noktası üzerinde çalıştırılan belirtilen işlemi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetProcess(   
   AD_PROCESS_ID    ProcessId,  
   IDebugProcess2** ppProcess  
);  
```  
  
```csharp  
int GetProcess(   
   AD_PROCESS_ID      ProcessId,  
   out IDebugProcess2 ppProcess  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ProcessId`  
 [in] Bir [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) yapı işlemi tanımlayıcısını belirtir.  
  
 `ppProcess`  
 [out] Döndürür bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) işlemi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md)