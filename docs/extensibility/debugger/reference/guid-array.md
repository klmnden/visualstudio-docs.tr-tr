---
title: GUID_ARRAY | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- GUID_ARRAY structure
ms.assetid: 9e12500c-2c1c-49b1-a0ba-e08366c97eb8
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: d53413ee56700fe39470d3bbc3229f4b8b668373
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317534"
---
# <a name="guidarray"></a>GUID_ARRAY
Bir dizi benzersiz tanımlayıcıları kullanılabilir hata ayıklama altyapıları için açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagGUID_ARRAY
{
    DWORD dwCount;
    GUID *Members;
} GUID_ARRAY;
```

```csharp
public struct GUID_ARRAY
{
    public uint dwCount;
    public Guid Members;
}
```

## <a name="members"></a>Üyeler
`dwCount`\
Dizide benzersiz tanımlayıcıları sayısı.

`Members`\
Benzersiz tanımlayıcıları içeren bir dizi.

## <a name="remarks"></a>Açıklamalar
Bu yapı tarafından döndürülen [GetEngineFilter](../../../extensibility/debugger/reference/idebugprocess3-getenginefilter.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetEngineFilter](../../../extensibility/debugger/reference/idebugprocess3-getenginefilter.md)
