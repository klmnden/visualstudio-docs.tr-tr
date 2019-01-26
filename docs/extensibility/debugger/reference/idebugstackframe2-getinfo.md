---
title: IDebugStackFrame2::GetInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugStackFrame2::GetInfo
helpviewer_keywords:
- IDebugStackFrame2::GetInfo
ms.assetid: 19c6870b-b94e-453c-bf19-82ce95b79d26
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b16d37061375dee569be7c6b17dd943a59a85ba1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54949655"
---
# <a name="idebugstackframe2getinfo"></a>IDebugStackFrame2::GetInfo
Yığın çerçevesinin açıklamasını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetInfo (   
   FRAMEINFO_FLAGS dwFieldSpec,  
   UINT            nRadix,  
   FRAMEINFO*      pFrameInfo  
);  
```  
  
```csharp  
int GetInfo (   
   enum_FRAMEINFO_FLAGS dwFieldSpec,  
   uint                 nRadix,  
   FRAMEINFO[]          pFrameInfo  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwFieldSpec`  
 [in] Bayraklarının bir birleşimi [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md) hangi alanları belirten numaralandırma `pFrameInfo` parametresi olan doldurulmalıdır.  
  
 `nRadix`  
 [in] Sayısal yedeklenmesine biçimlendirmede kullanılacak sayı tabanı.  
  
 `pFrameInfo`  
 [out] A [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yığın çerçevesini açıklamasını oturum girilir yapısının.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [FRAMEINFO_FLAGS](../../../extensibility/debugger/reference/frameinfo-flags.md)   
 [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)