---
title: IDebugReturnValueEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReturnValueEvent2
helpviewer_keywords:
- IDebugReturnValueEvent2
ms.assetid: 2daded43-e427-4fbb-a19e-f3834e3723af
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a2ce15c905ee12e1c3f45db5e5044b171db3527d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62916379"
---
# <a name="idebugreturnvalueevent2"></a>IDebugReturnValueEvent2
Bu arabirim dışı veya bir işlevin üzerinden geçildikten sonra oturum hata ayıklama Yöneticisi (SDM) hata ayıklama altyapısı (DE) tarafından gönderilir.

## <a name="syntax"></a>Sözdizimi

```
IDebugReturnValueEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 DE dışı veya üzerinden basamaklı bir işlevden dönüş değeri bildirmek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 KODU oluşturur ve bir işlevin dönüş değeri bildirmek için bu olay nesneyi gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugReturnValueEvent2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetReturnValue](../../../extensibility/debugger/reference/idebugreturnvalueevent2-getreturnvalue.md)|Bir işlev dışına Adımlama üzerinde döndürülen değer alır.|

## <a name="remarks"></a>Açıklamalar
 İşlev tarafından döndürülen değer çağrılarak alınabilir [GetReturnValue](../../../extensibility/debugger/reference/idebugreturnvalueevent2-getreturnvalue.md). Döndürülen değer görünür **Otolar** penceresi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)