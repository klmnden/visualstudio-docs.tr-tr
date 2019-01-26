---
title: IDebugProgram2::GetDisassemblyStream | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgram2::GetDisassemblyStream
helpviewer_keywords:
- IDebugProgram2::GetDisassemblyStream
ms.assetid: beda0da5-267e-4bf3-96c4-b659d29e2254
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9a80dd1a97be20f6065f6a9e1444dececfa52141
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54975677"
---
# <a name="idebugprogram2getdisassemblystream"></a>IDebugProgram2::GetDisassemblyStream
Bu program veya bu programın bir parçası için Ayrıştırılmış kod akışı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetDisassemblyStream(   
   DISASSEMBLY_STREAM_SCOPE   dwScope,  
   IDebugCodeContext2*        pCodeContext,  
   IDebugDisassemblyStream2** ppDisassemblyStream  
);  
```  
  
```csharp  
int GetDisassemblyStream(   
   enum_DISASSEMBLY_STREAM_SCOPE  dwScope,  
   IDebugCodeContext2             pCodeContext,  
   out IDebugDisassemblyStream2   ppDisassemblyStream  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwScope`  
 [in] Bir değer belirtir [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md) ayrıştırılmış kodu akışın kapsamını tanımlayan sabit listesi.  
  
 `pCodeContext`  
 [in] Bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) Ayrıştırılmış kod akış başlangıç noktası konumunu temsil eden nesne.  
  
 `ppDisassemblyStream`  
 [out] Döndürür bir [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md) Ayrıştırılmış kod akışını temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_DISASM_NOTSUPPORTED` ayrıştırılmış kodu bu belirli bir mimari için desteklenmiyorsa.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa `dwScopes` parametresinin `DSS_HUGE` , bayrak [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md) numaralandırma ayarlayın ve ardından ayrıştırılmış kodu için bütün dosyasını ayrıştırma yönergeler, örneğin, çok sayıda döndürmesi beklenir veya modül. Varsa `DSS_HUGE` bayrağı ayarlı değil, sonra ayrıştırılmış kodu küçük bir bölgeye sýnýrlandýrýlmasýna beklenir genellikle, tek bir işlev.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)