---
title: GETNAME_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
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
ms.openlocfilehash: ae68c77e2d6a41adfff6b49e55bbc6df4393fec7
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56701725"
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
GN_NAME belge veya bağlam kolay adı belirtir.

GN_FILENAME belge veya bağlam tam yolunu belirtir.

GN_BASENAME belgenin veya bağlam tam yol yerine temel dosya adını belirtir.

GN_MONIKERNAME bilinen adı biçiminde bir belge veya bağlam benzersiz adı belirtir.

GN_URL belge veya bağlam URL adını belirtir.

İf One exists GN_TITLE belgesinin bir başlığı belirtir.

İşler GN_STARTPAGEURL başlangıç sayfası URL'sini alır.

## <a name="remarks"></a>Açıklamalar
Bu değerler için parametre olarak geçirilen [GetName](../../../extensibility/debugger/reference/idebugdocument2-getname.md), [GetName](../../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md), ve [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md) ne tür bir geri dönmek için ad belirtmek için yöntemleri.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetName](../../../extensibility/debugger/reference/idebugdocument2-getname.md)
- [GetName](../../../extensibility/debugger/reference/idebugdocumentcontext2-getname.md)
- [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md)
