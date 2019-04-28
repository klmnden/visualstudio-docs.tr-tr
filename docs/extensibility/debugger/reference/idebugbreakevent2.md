---
title: IDebugBreakEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBreakEvent2
helpviewer_keywords:
- IDebugBreakEvent2 interface
ms.assetid: 57dfdbc2-4e68-4dbf-9579-006cd6fb1c62
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fdefbfa71ed220eed6e3f32ee95c02197f58a85d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62923433"
---
# <a name="idebugbreakevent2"></a>IDebugBreakEvent2
Bu arabirim, oturum hata ayıklama Yöneticisi (SDM) zaman uyumsuz bir sonu başarıyla tamamlandığını bildirir.

## <a name="syntax"></a>Sözdizimi

```
IDebugBreakEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 DE kullanıcı sonu bir programda desteklemek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde (SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi).

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 SDM çağrıları [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md) zaman kullanıcı istedi Duraklatılacak ayıklanan programa. Program başarıyla duraklatıldı DE gönderir `IDebugBreakEvent2` olay. Bu olay ile gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.

## <a name="remarks"></a>Açıklamalar
 Örneğin, bir kullanıcının seçim yapabileceği **tümünü Kes** komutunu **hata ayıklama** sonsuz bir döngüye çalışan bir programı ayırmak için menü. SDM çağırarak durdurmak için program söyler [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md). DE gönderir `IDebugBreakEvent2` program son ne zaman durdurur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)