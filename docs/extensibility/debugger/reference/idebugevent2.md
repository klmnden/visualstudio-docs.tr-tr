---
title: IDebugEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEvent2
helpviewer_keywords:
- IDebugEvent2 interface
ms.assetid: de3d714d-96fb-4e12-b66b-a75391472153
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f87184481c5d01e74d284b175078b67f6f2612d1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66310605"
---
# <a name="idebugevent2"></a>IDebugEvent2
Bu arabirim, bir kesme noktasında durdurma gibi kritik hata ayıklama bilgileri hem hata ayıklama iletisi gibi kritik olmayan bilgileri iletişim kurmak için kullanılır.

## <a name="syntax"></a>Sözdizimi

```
IDebugEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Özel bağlantı noktası sağlayıcısı ve hata ayıklama altyapısı (DE) tüm olay arabirimleri olarak aynı nesne üzerinde bu arabirimi uygulayın.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 ' % S'arabirimi için verilen Kimliğini (IID) bağımsız değişkeni kullanarak [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) veya [olay](../../../extensibility/debugger/reference/idebugportevents2-event.md), oturum hata ayıklama Yöneticisi (SDM) çağırır [QueryInterface](/cpp/atl/queryinterface) üzerinde `IDebugEvent2` almak için arabirimi uygun olay arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugEvent2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetAttributes](../../../extensibility/debugger/reference/idebugevent2-getattributes.md)|Bu hata ayıklama olayı özniteliklerini alır.|

## <a name="remarks"></a>Açıklamalar
 Gibi daha belirli olay arabirimleri [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md), IDebugEvent2 arabirimden türetilmiş değil ancak bunun yerine ayrı bir arabirimi aynı nesne üzerinde uygulanan `IDebugEvent2`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [Event](../../../extensibility/debugger/reference/idebugportevents2-event.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)