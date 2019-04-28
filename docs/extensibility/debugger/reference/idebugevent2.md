---
title: IDebugEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEvent2
helpviewer_keywords:
- IDebugEvent2 interface
ms.assetid: de3d714d-96fb-4e12-b66b-a75391472153
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7e70767bab6453f3c3d96b58c8be049a832dc6ad
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62920203"
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

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [Event](../../../extensibility/debugger/reference/idebugportevents2-event.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)