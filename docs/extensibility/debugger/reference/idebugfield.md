---
title: IDebugField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField
helpviewer_keywords:
- IDebugField interface
ms.assetid: adecdd1c-b1b9-4027-92da-74cbe910636f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 80def3f9c3d270ebd6f2217f6ce39f07ef27b119
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66337516"
---
# <a name="idebugfield"></a>IDebugField
Bu arabirim, bir alan, diğer bir deyişle, bir simge veya türü bir açıklamasını temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugField : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı, tüm alanlar için temel sınıf olarak bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim, tüm alanlar için temel sınıftır. Dönüş değerini temel alarak [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md), bu arabirim daha özel arabirimler kullanarak döndürebilir [QueryInterface](/cpp/atl/queryinterface). Ayrıca, pek çok arabirimi dönüş `IDebugField` çeşitli yöntemler nesneleri.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugField`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)|Simge veya türü görüntülenebilir bilgilerini alır.|
|[GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md)|Alan türünü alır.|
|[GetType](../../../extensibility/debugger/reference/idebugfield-gettype.md)|Alan türünü alır.|
|[GetContainer](../../../extensibility/debugger/reference/idebugfield-getcontainer.md)|Alan kapsayıcısını alır.|
|[GetAddress](../../../extensibility/debugger/reference/idebugfield-getaddress.md)|Adres alanının alır.|
|[GetSize](../../../extensibility/debugger/reference/idebugfield-getsize.md)|Bir alanın bayt cinsinden boyutunu alır.|
|[GetExtendedInfo](../../../extensibility/debugger/reference/idebugfield-getextendedinfo.md)|Genişletilmiş bir alanla ilgili bilgiler.|
|[Equal](../../../extensibility/debugger/reference/idebugfield-equal.md)|İki alan karşılaştırır.|
|[GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)|Tür bağımsız türü ve sembol bilgilerini alır.|

## <a name="remarks"></a>Açıklamalar
 Bir tür için bir C dili eşdeğerdir `typedef`.

 Aşağıdaki örnekte C++ dili, `weather` bir sınıf türüdür ve `sunny` ve `stormy` simgeler şunlardır:

```cpp
class weather;
weather sunny;
weather stormy;
```

 Bir alan temsil eden bir simge ya da türü çağırarak belirlenebilir [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) inceleyerek [FIELD_KIND](../../../extensibility/debugger/reference/field-kind.md) sonucu. Varsa `FIELD_KIND_TYPE` bitinin ayarlanmasıdır, alanın bir tür olduğunda ve `FIELD_KIND_SYMBOL` bit ayarlandığında, bir semboldür.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)