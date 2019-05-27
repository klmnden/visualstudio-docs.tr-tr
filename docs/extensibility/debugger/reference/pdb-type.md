---
title: PDB_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PDB_TYPE
helpviewer_keywords:
- PDB_TYPE structure
ms.assetid: 1c1bb772-77d6-4870-90b2-fd9247d0004e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b122231099641b38fc6106698dba5fbff433b4de
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212742"
---
# <a name="pdbtype"></a>PDB_TYPE

Bu yapı, PDB sembol harcanan alan türü hakkında bilgileri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagTYPE_PDB {
    ULONG32 ulAppDomainID;
    GUID    guidModule;
    DWORD   symid;
} PDB_TYPE;
```

```csharp
public struct PDB_TYPE {
    public uint ulAppDomainID;
    public Guid guidModule;
    public uint symid;
};
```

## <a name="members"></a>Üyeler

`ulAppDomainID`\
Simgenin içinden gelen uygulama kimliği. Bu, uygulamanın bir örneğini benzersiz şekilde tanımlamak için kullanılır.

`guidModule`\
Bu alan içeren modül GUID.

`symid`\
Bu alana karşılık gelen simgesinin kimliği.

## <a name="remarks"></a>Açıklamalar

Bu yapı birleşimde bir parçası olarak görünür [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) ne zaman yapısı `dwKind` alanını `TYPE_INFO` yapısı ayarlandığında `TYPE_KIND_PDB` (arasında bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) sabit listesi).

## <a name="requirements"></a>Gereksinimler

Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.

- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)
- [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)
