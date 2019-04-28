---
title: IDebugObject::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::GetSize
helpviewer_keywords:
- IDebugObject::GetSize method
ms.assetid: 89af423b-36eb-479d-b2de-2693455eca15
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a44f7c20784ca7f253db1d44c4079603f363d616
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62918498"
---
# <a name="idebugobjectgetsize"></a>IDebugObject::GetSize
Nesnenin boyutu bayt cinsinden alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSize( 
   UINT* pnSize
);
```

```csharp
int GetSize(
   out uint pnSize
);
```

#### <a name="parameters"></a>Parametreler
 `pnSize`

 [out] Boyutu bayt cinsinden döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kullanım [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md) bayt dizisi olarak değerini almak için yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)