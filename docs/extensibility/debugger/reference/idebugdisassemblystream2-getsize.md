---
title: IDebugDisassemblyStream2::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugDisassemblyStream2::GetSize
helpviewer_keywords:
- IDebugDisassemblyStream2::GetSize
ms.assetid: 8f512704-12d0-46d2-959a-4f8dffe117b5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ed9db83ed17b27090efef3e1d892d28f0078ce6c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988850"
---
# <a name="idebugdisassemblystream2getsize"></a>IDebugDisassemblyStream2::GetSize
Bu çözümü akış yönergelerinde boyutunu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetSize(   
   UINT64* pnSize  
);  
```  
  
```csharp  
int GetSize(   
   out ulong pnSize  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pnSize`  
 [out] Yönergeleri boyutunu döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemi tarafından döndürülen değer, bir dizi ayırmak için kullanılabilir [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md) geçirilerek yapılar [okuma](../../../extensibility/debugger/reference/idebugdisassemblystream2-read.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)   
 [Read](../../../extensibility/debugger/reference/idebugdisassemblystream2-read.md)