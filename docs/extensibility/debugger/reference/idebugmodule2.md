---
title: IDebugModule2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugModule2
helpviewer_keywords:
- IDebugModule2 interface
ms.assetid: 24c2a126-f4ab-4891-8509-8ef99b994c08
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b621ae3b1408bc4af371243a1c34909117d40576
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66323929"
---
# <a name="idebugmodule2"></a>IDebugModule2
Bu arabirim bir modülü temsil eder — diğer bir deyişle, bir yürütülebilir bir program ölçü — bir DLL gibi.

## <a name="syntax"></a>Sözdizimi

```
IDebugModule2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) bir modülü temsil eder ve bu modülle ilgili bilgileri erişim sağlamak için bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [GetModule](../../../extensibility/debugger/reference/idebugmoduleloadevent2-getmodule.md) bu arabirimi döndürür. DE gönderir [IDebugModuleLoadEvent2](../../../extensibility/debugger/reference/idebugmoduleloadevent2.md) arabirimini kullanarak oturum hata ayıklama Yöneticisi için (SDM) [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) yöntemi.

 Bu arabirim, ayrıca döndürülebilir bir [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md) yapısı (bir çağrı tarafından döndürülen [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2-enumframeinfo.md)).

- [Sonraki](../../../extensibility/debugger/reference/ienumdebugmodules2-next.md) Ayrıca bu arabirim döndürür ([EnumModules](../../../extensibility/debugger/reference/idebugprogram2-enummodules.md) döndürür [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md) arabirimi).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugModule2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)|Alır [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) , bu modül açıklar.|
|[ReloadSymbols_Deprecated](../../../extensibility/debugger/reference/idebugmodule2-reloadsymbols-deprecated.md)|ARTIK KULLANILMIYOR. KULLANMAYIN. Bu modüle ilişkin simgeleri yeniden yükler.|

## <a name="remarks"></a>Açıklamalar
 Modül bilgilerini görüntülenebilir **modülleri** IDE bir pencerenin.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)
- [GetModule](../../../extensibility/debugger/reference/idebugmoduleloadevent2-getmodule.md)
- [FRAMEINFO](../../../extensibility/debugger/reference/frameinfo.md)
- [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)