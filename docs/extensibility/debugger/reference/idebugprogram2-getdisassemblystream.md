---
title: IDebugProgram2::GetDisassemblyStream | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 61d9b728dd45b22b170c497b1d3ea1995ba92920
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212290"
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

## <a name="parameters"></a>Parametreler
`dwScope`\
[in] Bir değer belirtir [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md) ayrıştırılmış kodu akışın kapsamını tanımlayan sabit listesi.

`pCodeContext`\
[in] Bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) Ayrıştırılmış kod akış başlangıç noktası konumunu temsil eden nesne.

`ppDisassemblyStream`\
[out] Döndürür bir [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md) Ayrıştırılmış kod akışını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_DISASM_NOTSUPPORTED` ayrıştırılmış kodu bu belirli bir mimari için desteklenmiyorsa.

## <a name="remarks"></a>Açıklamalar
 Varsa `dwScopes` parametresinin `DSS_HUGE` , bayrak [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md) numaralandırma ayarlayın ve ardından ayrıştırılmış kodu için bütün dosyasını ayrıştırma yönergeler, örneğin, çok sayıda döndürmesi beklenir veya modül. Varsa `DSS_HUGE` bayrağı ayarlı değil, sonra ayrıştırılmış kodu küçük bir bölgeye sýnýrlandýrýlmasýna beklenir genellikle, tek bir işlev.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [DISASSEMBLY_STREAM_SCOPE](../../../extensibility/debugger/reference/disassembly-stream-scope.md)
- [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
- [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)