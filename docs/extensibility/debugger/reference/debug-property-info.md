---
title: DEBUG_PROPERTY_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DEBUG_PROPERTY_INFO
helpviewer_keywords:
- DEBUG_PROPERTY_INFO structure
ms.assetid: 5a085d18-62c6-4740-b9e9-3f5db6bfdf7f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7804cfad48d5029e16619b5ae524fa6e761f11b4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66346176"
---
# <a name="debugpropertyinfo"></a>DEBUG_PROPERTY_INFO
Hata ayıklama özelliği hakkında bilgiler içerir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagDEBUG_PROPERTY_INFO {
    DEBUGPROP_INFO_FLAGS dwValidFields;
    BSTR                 bstrFullName;
    BSTR                 bstrName;
    BSTR                 bstrType;
    BSTR                 bstrValue;
    IDebugProperty2*     pProperty;
    DBG_ATTRIB_FLAGS     dwAttrib;
} DEBUG_PROPERTY_INFO;
```

```csharp
public struct DEBUG_PROPERTY_INFO {
    public uint            dwValidFields;
    public string          bstrFullName;
    public string          bstrName;
    public string          bstrType;
    public string          bstrValue;
    public IDebugProperty2 pProperty;
    public ulong           dwAttrib;
};
```

## <a name="members"></a>Üyeler
`dwValidFields`\
Bayraklarının bir birleşimi [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md) hangi alanların doldurulur belirten sabit listesi.

`bstrFullName`\
Özelliğin tam adı.

`bstrName`\
Bir bağlam içinde özellik adı.

`bstrType`\
Özellik türü olarak biçimlendirilmiş bir dize.

`bstrValue`\
Özellik değeri olarak biçimlendirilmiş bir dize.

`pProperty`\
[IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) bu yapı tarafından açıklanan bir nesne.

`dwAttrib`\
Bayraklarının bir birleşimi [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md) bu özelliğin özniteliklerini açıklayan sabit listesi.

## <a name="remarks"></a>Açıklamalar
Bir özellik adı, türü ve değeri içeren hiyerarşik bir yapısı nesnesidir. Örneğin, bir özellik, yerel değişkenler, parametreleri, izleme değişkenleri ve ifadeleri ve kayıtları açıklayabilirsiniz.

Bu yapı geçirilir [GetPropertyInfo](../../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md) yöntemi burada da doldurulur. Bu yapı ayrıca bir liste bu yapının bir parçası olarak döndürülen [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md) hangi sırayla çağrısından döndürülen arabirimi [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) ve [ EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md) yöntemleri.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md)
- [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [GetPropertyInfo](../../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md)
- [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md)
- [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md)
- [EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md)
