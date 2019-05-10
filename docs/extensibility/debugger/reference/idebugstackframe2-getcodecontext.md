---
title: IDebugStackFrame2::GetCodeContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugStackFrame2::GetCodeContext
helpviewer_keywords:
- IDebugStackFrame2::GetCodeContext
ms.assetid: 93d66159-a41d-49ef-982f-91bb4d073b74
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 12ad4db6583c702115f5c97b2fa2c4485c891298
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65458574"
---
# <a name="idebugstackframe2getcodecontext"></a>IDebugStackFrame2::GetCodeContext
Bu yığın çerçevesi için kod bağlamı alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetCodeContext ( 
   IDebugCodeContext2** ppCodeCxt
);
```

```csharp
int GetCodeContext ( 
   out IDebugCodeContext2 ppCodeCxt
);
```

## <a name="parameters"></a>Parametreler
 `ppCodeCxt`\

 [out] Döndürür bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) dosyadaki geçerli yönerge işaretçisini Bu yığın çerçevesinde temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)
- [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)