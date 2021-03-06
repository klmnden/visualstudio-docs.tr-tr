---
title: IDebugExceptionEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExceptionEvent2
helpviewer_keywords:
- IDebugExceptionEvent2 interface
ms.assetid: 53d32e59-a84b-4710-833e-c5ab08100516
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3fd2a449c71b69c654cd19846990f7b722f706de
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66325987"
---
# <a name="idebugexceptionevent2"></a>IDebugExceptionEvent2
Programın şu anda yürütülmekte olan bir özel durum oluştuğunda hata ayıklama altyapısı (DE) Bu arabirim oturum hata ayıklama Yöneticisi (SDM) gönderir.

## <a name="syntax"></a>Sözdizimi

```
IDebugExceptionEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Bu arabirim için bir özel durum hata ayıklaması yapılan programa oluştu rapor DE uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 KODU oluşturur ve bu olay bir özel durum rapor nesnesine gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugExceptionEvent2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)|Bu olay harekete geçirilen özel durum hakkında ayrıntılı bilgiler alır.|
|[GetExceptionDescription](../../../extensibility/debugger/reference/idebugexceptionevent2-getexceptiondescription.md)|Bu olay harekete geçirilen özel durum için okunabilir bir açıklamasını alır.|
|[CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)|Hata ayıklama altyapısı (DE) yürütme devam ettiğinde ayıklanan programa bu özel durum geçirme seçeneğiniz destekleyip desteklemediğini belirler.|
|[PassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-passtodebuggee.md)|Özel durum yürütme devam ettiğinde ayıklanan programa geçirilmelidir olup olmadığını ya da özel durum atılmalı belirtir.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="remarks"></a>Açıklamalar
 Bu özel durum olayı bir ilk şans veya ikinci şans özel durum için bir çağrı tarafından belirlendiyse, görmek için DE denetler olay göndermeden önce [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md). İlk fırsat özel durum olarak belirlendiyse `IDebugExceptionEvent2` olay SDM için gönderilir. Değilse DE uygulamaya özel durumu işlemek üzere bir fırsat sunar. Hiçbir özel durum işleyicisi sağlanır ve özel durum ikinci şans özel durum belirlendiyse `IDebugExceptionEvent2` olay SDM için gönderilir. Aksi takdirde DE programın yürütülmesini sürdürür ve işletim sistemi ya da çalışma zamanı özel durumu işler.

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)