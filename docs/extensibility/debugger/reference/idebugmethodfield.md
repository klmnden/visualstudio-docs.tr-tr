---
title: IDebugMethodField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField
helpviewer_keywords:
- IDebugMethodField interface
ms.assetid: a7dc9030-fc98-4cf1-b943-37a4003300b6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8a4b8557226ad010968772562aa787472f159900
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66324100"
---
# <a name="idebugmethodfield"></a>IDebugMethodField
Bu arabirim yöntemi açıklanmaktadır.

## <a name="syntax"></a>Sözdizimi

```
IDebugMethodField : IDebugContainerField
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) arabirimi. Bir yöntem sunan bir özelleştirmesi arabirimidir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden edinme [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) , arabirim [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) döndürür `FIELD_TYPE_METHOD`. Ayrıca, yöntemleri [GetPropertyGetter](../../../extensibility/debugger/reference/idebugpropertyfield-getpropertygetter.md), [GetPropertySetter](../../../extensibility/debugger/reference/idebugpropertyfield-getpropertysetter.md), ve [EnumConstructors](../../../extensibility/debugger/reference/idebugclassfield-enumconstructors.md), tüm dönüş `IDebugMethodField` arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemlere ek olarak [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) ve [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) arabirimleri, bu arabirimi aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumParameters](../../../extensibility/debugger/reference/idebugmethodfield-enumparameters.md)|Yöntem parametreleri için bir numaralandırıcı oluşturur.|
|[GetThis](../../../extensibility/debugger/reference/idebugmethodfield-getthis.md)|"Bu" işaretçisinin yöntemi içeren nesneyi alır.|
|[EnumAllLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumalllocals.md)|Tüm yerel değişkenlerin yöntemi için bir numaralandırıcı oluşturur.|
|[EnumLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumlocals.md)|Yöntemin seçili yerel değişkenler için bir numaralandırıcı oluşturur.|
|[IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugmethodfield-iscustomattributedefined.md)|Belirli bir özel öznitelik tanımlı olup olmadığını belirler.|
|[EnumStaticLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumstaticlocals.md)|Yöntem statik yerel değişkenler için bir numaralandırıcı oluşturur.|
|[GetGlobalContainer](../../../extensibility/debugger/reference/idebugmethodfield-getglobalcontainer.md)|Yöntem genel kapsayıcısını alır.|
|[EnumArguments](../../../extensibility/debugger/reference/idebugmethodfield-enumarguments.md)|Yöntemini çağırmak için gereken her bağımsız değişken türü için bir numaralandırıcı oluşturur.|

## <a name="remarks"></a>Açıklamalar
 Bir yöntem parametreleri ve bunun yanı sıra yerel değişkenleri içerebilir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)