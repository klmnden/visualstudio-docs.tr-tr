---
title: IEnumDebugModules2::Reset | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugModules2::Reset
helpviewer_keywords:
- IEnumDebugModules2::Reset
ms.assetid: f6ff364c-2644-4919-b950-3cb82eb6f601
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: bd20b852e8715aa9a5783eccbbaeb820dd455bf1
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66203539"
---
# <a name="ienumdebugmodules2reset"></a>IEnumDebugModules2::Reset
Numaralandırma ilk öğeyi sıfırlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Reset(
   void
);
```

```csharp
int Reset();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem çağrıldığında sonra yapılan sonraki çağrıda [sonraki](../../../extensibility/debugger/reference/ienumdebugmodules2-next.md) yöntemi numaralandırma ilk öğeyi döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)