---
title: DUMPTYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DUMPTYPE
helpviewer_keywords:
- DUMPTYPE enumeration
ms.assetid: ea8160db-8732-4056-a1d7-892ef72da71e
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7edb3129733aec29bb5eda64d388024bec4d5ece
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66318198"
---
# <a name="dumptype"></a>DUMPTYPE
Döküm için ne kadar bir programın durumu ' (örneğin, çalışan iş parçacıkları, yığın çerçeveleri ve geçerli yönerge adresi) belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_DUMPTYPE {
    DUMP_MINIDUMP = 0,
    DUMP_FULLDUMP = 1
};
typedef DWORD DUMPTYPE;
```

```csharp
public enum enum_DUMPTYPE {
    DUMP_MINIDUMP = 0,
    DUMP_FULLDUMP = 1
};
```

## <a name="fields"></a>Alanlar
`DUMP_MINIDUMP`\
Küçük, küçük bir döküm belirtir.

`DUMP_FULLDUMP`\
Büyük, eksiksiz bir döküm belirtir.

## <a name="remarks"></a>Açıklamalar
Bağımsız değişken olarak geçirilen [WriteDump](../../../extensibility/debugger/reference/idebugprogram2-writedump.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [WriteDump](../../../extensibility/debugger/reference/idebugprogram2-writedump.md)
