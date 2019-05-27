---
title: IDebugPointerField::GetDereferencedField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPointerField::GetDereferencedField
helpviewer_keywords:
- IDebugPointerField::GetDereferencedField method
ms.assetid: 8de988ab-cd79-4287-be72-3c900f2fe407
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a2fed1d2f0a9027f4570c4efdc41ddf1eeb5f9a3
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66209402"
---
# <a name="idebugpointerfieldgetdereferencedfield"></a>IDebugPointerField::GetDereferencedField
Bu yöntem, bu işaretçi nesnesinin işaret ettiği nesnenin türü döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDereferencedField(
   IDebugField** ppField
);
```

```csharp
int GetDereferencedField(
   out IDebugField ppField
);
```

## <a name="parameters"></a>Parametreler
`ppField`\
[out] Döndürür bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) açıklayan hedef nesnenin türü.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Örneğin, bir IF [IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md) nesneyi işaret eden bir tamsayıya [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) bu yöntem tarafından döndürülen tür, tamsayı türü açıklar.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPointerField](../../../extensibility/debugger/reference/idebugpointerfield.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)