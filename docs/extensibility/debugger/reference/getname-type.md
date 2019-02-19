---
title: GETNAME_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- GETNAME_TYPE
helpviewer_keywords:
- GETNAME_TYPE enumeration
ms.assetid: 2f9f1679-e9e8-4c9c-ac90-aa07bfe69914
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ba394d725afd45664ad6cf4f69c9e048b7e1a74d
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56413117"
---
# <a name="getnametype"></a>GETNAME_TYPE
Alınacak dosya adı türünü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_GETNAME_TYPE {
    GN_NAME         = 0,
    GN_FILENAME     = 1,
    GN_BASENAME     = 2,
    GN_MONIKERNAME  = 3,
    GN_URL          = 4,
    GN_TITLE        = 5,
    GN_STARTPAGEURL = 6
};
typedef DWORD GETNAME_TYPE;
```

```csharp
public enum enum_GETNAME_TYPE {
    GN_NAME         = 0,
    GN_FILENAME     = 1,
    GN_BASENAME     = 2,
    GN_MONIKERNAME  = 3,
    GN_URL          = 4,
    GN_TITLE        = 5,
    GN_STARTPAGEURL = 6
};
```

## <a name="members"></a>Üyeler
GN_NAME  
Belge veya bağlam kolay adı belirtir.

GN_FILENAME  
Belge veya bağlam tam yolunu belirtir.

GN_BASENAME  
Bir temel dosya adı yerine bir belge veya bağlam tam yolunu belirtir.

GN_MONIKERNAME  
Belge veya bağlam benzersiz bir adla bir bilinen ad biçiminde belirtir.

GN_URL  
Belge veya bağlam URL adını belirtir.

GN_TITLE  
Varsa, bir belgenin başlığını belirtir.

GN_STARTPAGEURL  
İşlemler için başlangıç sayfası URL'si alır.

## <a name="remarks"></a>Açıklamalar
Bu değerler için parametre olarak geçirilen [GetName](../../../extensibility/debugger/reference/idebugdocument2-getname.md), [GetName](../../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md), ve [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md) ne tür bir geri dönmek için ad belirtmek için yöntemleri.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[GetName](../../../extensibility/debugger/reference/idebugdocument2-getname.md)  
[GetName](../../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md)  
[GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md)
