---
title: IDebugObject2::GetField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject2::GetField
helpviewer_keywords:
- IDebugObject2::GetField method
ms.assetid: add6a6b5-e752-47dd-9613-29206ea809b0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 829ee652ce1d1d2ebb713d4b52e1ea255624f07d
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66209842"
---
# <a name="idebugobject2getfield"></a>IDebugObject2::GetField
Bu nesne türünü alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetField(
 IDebugField** ppField
);
```

```csharp
int GetField(
   out IDebugField ppField
);
```

## <a name="parameters"></a>Parametreler
`ppField`\
[out] Döndürür bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne yoksa null değeri.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir alan nesne türünü açıklar.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)