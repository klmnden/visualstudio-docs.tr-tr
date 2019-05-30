---
title: IDebugFunctionObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugFunctionObject
helpviewer_keywords:
- IDebugFunctionObject interface
ms.assetid: 8d94e97c-a9d1-400c-8a98-a44b5385b33a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5fb0d969268e7765abe5c3ebdc9fc000a10a3aa0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66313444"
---
# <a name="idebugfunctionobject"></a>IDebugFunctionObject
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 Bu arabirim, bir işlevi temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugFunctionObject : IDebugObject
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 İfade değerlendiricisi, bir işlevi temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu bir arabirimdir özelleştirmesi [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) arabirim ve kullanılarak elde edilen [QueryInterface](/cpp/atl/queryinterface) üzerinde `IDebugObject` arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md), `IDebugFunctionObject` arabirimi aşağıdaki yöntemleri sunar.

|Yöntem|Açıklama|
|------------|-----------------|
|[CreatePrimitiveObject](../../../extensibility/debugger/reference/idebugfunctionobject-createprimitiveobject.md)|Temel veri nesnesi oluşturur.|
|[CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)|Bir oluşturucu kullanılarak bir nesne oluşturur.|
|[CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)|Bir nesne ile hiçbir oluşturucu oluşturur.|
|[CreateArrayObject](../../../extensibility/debugger/reference/idebugfunctionobject-createarrayobject.md)|Bir dizi nesnesi oluşturur.|
|[CreateStringObject](../../../extensibility/debugger/reference/idebugfunctionobject-createstringobject.md)|Bir dize nesnesi oluşturur.|
|[Evaluate](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md)|İşlevini çağırır ve bir nesne olarak elde edilen değeri döndürür.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, ayrıştırma ağacı işlevlerini temsil etmek ifade değerlendirici sağlar. `Create` Bu arabirimdeki yöntemleri yönteme giriş parametrelerini temsil eden nesneler oluşturmak için kullanılır. İşlev çağrı yaparak sonra yürütülebilen [değerlendir](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md) yöntemi işlevinin dönüş değerini temsil eden bir nesne döndürür.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [İfade Değerlendirme Arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)