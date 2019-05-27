---
title: IDebugStackFrame3::GetUnwindCodeContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugStackFrame3::GetUnwindCodeContext
helpviewer_keywords:
- IDebugStackFrame3::GetUnwindCodeContext method
ms.assetid: b25f7e7d-2b24-48e4-93b3-829e61d73ebf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7e8d75d33afc3078fc480c6a99d33dd975904f24
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66203274"
---
# <a name="idebugstackframe3getunwindcodecontext"></a>IDebugStackFrame3::GetUnwindCodeContext
Bir yığın geriye doğru işlem durumunda bir konumu temsil eden kod bağlamı oluştu döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetUnwindCodeContext(
   IDebugCodeContext2 **ppCodeContext
);
```

```csharp
int GetUnwindCodeContext(
   out IDebugCodeContext2 ppCodeContext
);
```

## <a name="parameters"></a>Parametreler
`ppCodeContext`\
[out] Döndürür bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) bir yığının geriye doğru oluştuysa kod bağlamı konumu temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, bir yığının geriye doğru konumu için bir kod bağlamı döndürebilir olsa da, bunu mutlaka yığının geriye doğru gerçekten geçerli yığın çerçevesi ortaya çıkabilir gelmez.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugStackFrame3](../../../extensibility/debugger/reference/idebugstackframe3.md)
- [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)