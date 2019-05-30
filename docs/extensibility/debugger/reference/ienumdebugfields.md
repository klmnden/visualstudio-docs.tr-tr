---
title: IEnumDebugFields | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugFields
helpviewer_keywords:
- IEnumDebugFields interface
ms.assetid: 403c2a51-3ba5-431f-a1dd-2f3b2046c00c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 50d80242ca516c5fa7f3ad297250e25c782664d0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350375"
---
# <a name="ienumdebugfields"></a>IEnumDebugFields
Bu arabirimi uygulayan nesnelerin bir koleksiyonunu temsil eder [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugFields : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirimi uygulayan nesne kümeleri sağlamak için Sembol sağlayıcısı tarafından uygulanan [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi. Bu varlığı nedeniyle standart bir COM numaralandırma olmadığını unutmayın [GetCount](../../../extensibility/debugger/reference/ienumdebugfields-getcount.md) yöntemi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim tarafından döndürülen [GetMethodFieldsByName](../../../extensibility/debugger/reference/idebugsymbolprovider-getmethodfieldsbyname.md) ve [GetNamespacesUsedAtAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getnamespacesusedataddress.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Bu arabirim, aşağıdaki yöntemleri uygular.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugfields-next.md)|Sonraki alır [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesnelerden sabit listesi.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugfields-skip.md)|Belirtilen bir girdi sayısı atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugfields-reset.md)|Numaralandırma ilk girişe sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugfields-clone.md)|Geçerli sabit bir kopyasını alır.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugfields-getcount.md)|Sabit listesi içerisindeki giriş sayısını alır.|

## <a name="remarks"></a>Açıklamalar

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [GetMethodFieldsByName](../../../extensibility/debugger/reference/idebugsymbolprovider-getmethodfieldsbyname.md)
- [GetNamespacesUsedAtAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getnamespacesusedataddress.md)