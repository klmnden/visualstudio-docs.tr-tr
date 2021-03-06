---
title: IDebugCustomAttributeQuery2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCustomAttributeQuery2
helpviewer_keywords:
- IDebugCustomAttributeQuery interface
- IDebugCustomAttributeQuery2 interface
ms.assetid: 7cfa23e4-a05a-47a3-af6c-bd40c655014b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 00220574ac9c16bdab9abd64adde1877ee0fd9f2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66335800"
---
# <a name="idebugcustomattributequery2"></a>IDebugCustomAttributeQuery2
Bu alan için özel bir öznitelik var olup olmadığını belirler ve varsa, öznitelik bilgileri döndürür.

## <a name="syntax"></a>Sözdizimi

```
IDebugCustomAttributeQuery2 : IDebugCustomAttributeQuery
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) özel öznitelikler desteklemek için.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden edinme [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir **IDebugCustomAttributeQuery** arabirimi.

|Yöntem|Açıklama|
|------------|-----------------|
|[IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugcustomattributequery2-iscustomattributedefined.md)|Özel bir öznitelik ada göre var olup olmadığını belirler.|
|[GetCustomAttributeByName](../../../extensibility/debugger/reference/idebugcustomattributequery2-getcustomattributebyname.md)|Belirtilen özel özniteliğin öznitelik bilgileri alır.|

 Ek olarak **IDebugCustomAttributeQuery** yöntemleri `IDebugCustomAttributeQuery2` aşağıdaki yöntemi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md)|Bu alana ekli tüm özel öznitelikleri için bir numaralandırıcı alır.|

## <a name="remarks"></a>Açıklamalar
 [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md) yöntem bu alan için tanımlanan tüm özel öznitelikleri için bir numaralandırıcı döndürür.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)