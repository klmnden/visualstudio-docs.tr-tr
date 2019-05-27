---
title: IDebugProgramNodeAttach2::OnAttach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramNodeAttach2::OnAttach
helpviewer_keywords:
- IDebugProgramNodeAttach2::OnAttach
ms.assetid: 5fe52761-a508-4ab5-abdb-334fb6590334
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ce1b5635685971b3a9390533589975ff0f323021
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66203787"
---
# <a name="idebugprogramnodeattach2onattach"></a>IDebugProgramNodeAttach2::OnAttach
İlişkili programına iliştirir veya ekleme işlemi için erteler [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT OnAttach(
   [in] REFGUID guidProgramId
);
```

```csharp
int OnAttach(
   ref Guid guidProgramId
};
```

## <a name="parameters"></a>Parametreler
`guidProgramId`\
[in] `GUID` ilişkili programına atamak için.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi çağırılmalıdır. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem ekleme işlemi sırasında önce çağrılır [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi çağrılır. `OnAttach` Yöntemi ekleme işlemi gerçekleştirebilir (Bu durumda, bu yöntemi döndürür `S_FALSE`) veya ekleme işlemi için erteleme `IDebugEngine2::Attach` yöntemi ( `OnAttach` yöntemi döndürür `S_OK`). Ya da bir olay `OnAttach` yöntemi ayarlayabilirsiniz `GUID` için ayıklanan programın belirli `GUID`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)