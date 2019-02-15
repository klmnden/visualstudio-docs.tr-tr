---
title: CONST_GUID_ARRAY | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- CONST_GUID_ARRAY
helpviewer_keywords:
- CONST_GUID_ARRAY structure
ms.assetid: bd55e7d8-372c-4c3e-9eed-28f6b415a5db
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 40511cac0a6d731d451d1fb2e0e4c02d214297f7
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318543"
---
# <a name="constguidarray"></a>CONST_GUID_ARRAY
Bir listesini tutan bir yapı `GUID`s.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagCONST_GUID_ARRAY {
    DWORD       dwCount;
    CONST GUID* Members;
} CONST_GUID_ARRAY;
```

```csharp
public struct CONST_GUID_ARRAY {
    public uint   dwCount;
    public Guid[] Members;
}
```

## <a name="members"></a>Üyeler
dwCount  
Sayısı `GUID`s'te `Members` dizisi.

Üyeler  
Dizi `GUID`s.

## <a name="remarks"></a>Açıklamalar
Bu yapı geçirilir [PublishProgram](../../../extensibility/debugger/reference/idebugprogrampublisher2-publishprogram.md) yöntemi ve öğesinden döndürülen [GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md) ve [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md) yöntemleri.

Bu yapının bir örneğinin sahibi, ayrılan belleği serbest bırakma için sorumludur.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[PublishProgram](../../../extensibility/debugger/reference/idebugprogrampublisher2-publishprogram.md)  
[GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)  
[WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md)
