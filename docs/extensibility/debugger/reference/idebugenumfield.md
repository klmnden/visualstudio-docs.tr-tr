---
title: IDebugEnumField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField
helpviewer_keywords:
- IDebugEnumField interface
ms.assetid: 42f685bf-0f39-47f4-98b0-6022efe2bf97
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4e2bcb8f8562b5b20231879d46c64eb73af027f0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680002"
---
# <a name="idebugenumfield"></a>IDebugEnumField
Bu arabirim, bir numaralandırma türü temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugEnumField : IDebugContainerField
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı, bir numaralandırma temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden edinme [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) , arabirim [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) döndürür `FIELD_TYPE_ENUM`.

## <a name="methods-in-vtable-order"></a>VTable sırayla yöntemleri
 Yöntemlere ek olarak `IDebugField` ve `IDebugContainerField` arabirimleri, bu arabirimi aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetUnderlyingSymbol](../../../extensibility/debugger/reference/idebugenumfield-getunderlyingsymbol.md)|Döndürür bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) açıklayan bu numaralandırma türü adı.|
|[GetStringFromValue](../../../extensibility/debugger/reference/idebugenumfield-getstringfromvalue.md)|Verilen değer ile ilişkili numaralandırma sabiti adını döndürür.|
|[GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)|Belirtilen numaralandırma sabit adla ilişkilendirilmiş değeri döndürür|
|[GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)|Belirtilen numaralandırma sabit adı ancak göz ardı çalışması ile ilişkili değeri döndürür.|

## <a name="remarks"></a>Açıklamalar
 Aslında bir konumla ilişkili temel alınan simgenin olup [bağlama](../../../extensibility/debugger/reference/idebugbinder-bind.md).

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md)