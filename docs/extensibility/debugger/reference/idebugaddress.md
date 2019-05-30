---
title: IDebugAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugAddress
helpviewer_keywords:
- IDebugAddress interface
ms.assetid: bc709ff7-4966-4f36-9af2-690efe2cea1d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 653d2424d21a18e7053f66e0a74214ecc25d97da
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317915"
---
# <a name="idebugaddress"></a>IDebugAddress
Bu arabirim, bir öğenin adresi temsil eder. Bu sembol işleyici tarafından döndürülür.

## <a name="syntax"></a>Sözdizimi

```
IDebugAddress : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Sembol sağlayıcısı, bir nesnenin bir adresi temsil etmek için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Birçok yöntemlerde pek çok arabirimi bu arabirim döndürür.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Bu arabirim, aşağıdaki yöntemi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetAddress](../../../extensibility/debugger/reference/idebugaddress-getaddress.md)|Alır bir [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) yapısı, konumu ve bir nesne tanımlayan.|

## <a name="remarks"></a>Açıklamalar
 Sembol sağlayıcısı, bir nesne ve konumuna (örneğin, işlev, yöntemi veya sınıf) belirli bir kapsam içinde temsil etmek için bu arabirimi döndürür. Bu arabirim döndürüldüğü ve sembol sağlayıcısı ve ifade çeşitli yöntemlere geçirilen değerlendiricisi. Normalde, sembol sağlayıcısı bu arabirimi içeriğini yorumlamak için gereken tek varlıktır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)