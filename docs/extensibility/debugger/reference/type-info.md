---
title: TYPE_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- TYPE_INFO
helpviewer_keywords:
- TYPE_INFO structure
ms.assetid: d725cb68-a565-49d1-a16f-ff0445c587a0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 86212a5ef6f417dae2ae345b1367e041c3cf9095
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66316123"
---
# <a name="typeinfo"></a>TYPE_INFO
Bu yapı, çeşitli türlerdeki bir alan türü hakkında bilgi belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
struct _tagTYPE_INFO_UNION {
   dwTYPE_KIND dwKind;
   union {
      METADATA_TYPE typeMeta;
      PDB_TYPE      typePdb;
      BUILT_TYPE    typeBuilt;
      DWORD         unused;
   } type;
} TYPE_INFO;
```

```csharp
public struct TYPE_INFO {
   public uint   dwKind;
   public IntPtr unionmember;
};
```

## <a name="members"></a>Üyeler
 `dwKind`\
 Bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) birleşim yorumlama belirleyen sabit listesi.

 `type.typeMeta`\
 [C++ yalnızca] İçeren bir [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md) , yapı `dwKind` olduğu `TYPE_KIND_METADATA`.

 `type.typePdb`\
 [C++ yalnızca] İçeren bir [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md) , yapı `dwKind` olduğu `TYPE_KIND_PDB`.

 `type.typeBuilt`\
 [C++ yalnızca] İçeren bir [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md) , yapı `dwKind` olduğu `TYPE_KIND_BUILT`.

 `type.unused`\
 Kullanılmayan doldurma.

 `type`\
 Union adıdır.

 `unionmember`\
 [C# yalnızca] Bu uygun yapı türüne göre sıralama `dwKind`.

## <a name="remarks"></a>Açıklamalar
 Bu yapı geçirilir [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md) yöntemi burada da doldurulur. Yapı içeriğini yorumlanma şeklini dayanır `dwKind` alan.

> [!NOTE]
> [C++ yalnızca] Varsa `dwKind` eşittir `TYPE_KIND_BUILT`, arka plandaki serbest bırakmak gerekli ise [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne yok etme `TYPE_INFO` yapısı. Bu çağrılarak gerçekleştirilir `typeInfo.type.typeBuilt.pUnderlyingField->Release()`.

 [C# yalnızca] Aşağıdaki tablo nasıl yorumlanacağını gösterir `unionmember` türü her tür için üye. Bu örnek, türü bir tür için nasıl yapıldığını gösterir.

|`dwKind`|`unionmember` yorumlanan|
|--------------|----------------------------------|
|`TYPE_KIND_METADATA`|[METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)|
|`TYPE_KIND_PDB`|[PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)|
|`TYPE_KIND_BUILT`|[BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)|

## <a name="example"></a>Örnek
 Bu örnek nasıl yorumlanacağını gösterir `unionmember` üyesi `TYPE_INFO` C# yapısı. Bu örnek, yalnızca bir tür yorumlama gösterir (`TYPE_KIND_METADATA`), ancak diğerleri tam olarak aynı şekilde yorumlanır.

```csharp
using System;
using System.Runtime.Interop.Services;
using Microsoft.VisualStudio.Debugger.Interop;

namespace MyPackage
{
    public class MyClass
    {
        public void Interpret(TYPE_INFO ti)
        {
            if (ti.dwKind == (uint)enum_dwTypeKind.TYPE_KIND_METADATA)
            {
                 METADATA_TYPE dataType = (METADATA_TYPE)Marshal.PtrToStructure(ti.unionmember,
                                               typeof(METADATA_TYPE));
            }
        }
    }
}
```

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)
- [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)
- [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)
- [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)
- [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)