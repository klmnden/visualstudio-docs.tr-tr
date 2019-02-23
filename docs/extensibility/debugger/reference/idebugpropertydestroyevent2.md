---
title: IDebugPropertyDestroyEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPropertyDestroyEvent2
helpviewer_keywords:
- IDebugPropertyDestroyEvent2 interface
ms.assetid: 301b7a75-ecfa-46f1-9131-66cf3e4be147
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6c2ab0bd3a0a4afcabb5ea04a6bea6ba20ff5c70
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706177"
---
# <a name="idebugpropertydestroyevent2"></a>IDebugPropertyDestroyEvent2
Bu arabirim, belirli bir belge ile ilişkili olan bir özellik edilmek üzereyken hata ayıklama altyapısı (DE) oturum hata ayıklama Yöneticisi (SDM) gönderilir.

## <a name="syntax"></a>Sözdizimi

```
IDebugPropertyDestroyEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 DE bir özellik yok edildi bildirmek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi. Bu arabirim, daha önce bir komut dosyasıyla ilişkili bir özelliği DE oluşturduysa uygulanır; özellik yok etme ilişkili betik IDE'den kaldırır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 DE oluşturur ve bu olay nesneyi bir özelliği yok edilmiş raporu gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugPropertyDestroyEvent2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetDebugProperty](../../../extensibility/debugger/reference/idebugpropertydestroyevent2-getdebugproperty.md)|Yok edilecek özelliği alır.|

## <a name="remarks"></a>Açıklamalar
 Açıklamalar için bkz. [IDebugPropertyCreateEvent2](../../../extensibility/debugger/reference/idebugpropertycreateevent2.md) neden hakkında ayrıntılı bilgi için bu olaylar kullanılır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugPropertyCreateEvent2](../../../extensibility/debugger/reference/idebugpropertycreateevent2.md)