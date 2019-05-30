---
title: IEnumDebugAddresses | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugAddresses
helpviewer_keywords:
- IEnumDebugAddresses interface
ms.assetid: 5f6f6751-e6d8-4c5a-8e81-414b6e5d8cc5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0f7871a223695632b5c2118377c9cfeb24d297e4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329917"
---
# <a name="ienumdebugaddresses"></a>IEnumDebugAddresses
Bu arabirimi uygulayan nesnelerin bir koleksiyonunu temsil eder [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugAdresses : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirimi uygulayan nesne kümeleri sağlamak için Sembol sağlayıcısı tarafından uygulanan [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi. Bu varlığı nedeniyle standart bir COM numaralandırma olmadığını unutmayın [GetCount](../../../extensibility/debugger/reference/ienumdebugaddresses-getcount.md) yöntemi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bu arabirim tarafından döndürülen [GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md) ve [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Bu arabirim, aşağıdaki yöntemleri uygular.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugaddresses-next.md)|Sonraki alır [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) nesnelerden sabit listesi.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugaddresses-skip.md)|Belirtilen bir girdi sayısı atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugaddresses-reset.md)|Numaralandırma ilk girişe sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugaddresses-clone.md)|Geçerli sabit bir kopyasını alır.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugaddresses-getcount.md)|Sabit listesi içerisindeki giriş sayısını alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, genellikle için ifade değerlendirici vermek için uygun adresi belirlemeye yardımcı olması için hata ayıklama altyapısı tarafından kullanılır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: sh.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sembol Sağlayıcısı Arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
- [GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md)
- [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)