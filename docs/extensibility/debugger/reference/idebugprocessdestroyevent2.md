---
title: IDebugProcessDestroyEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcessDestroyEvent2
helpviewer_keywords:
- IDebugProcessDestroyEvent2
ms.assetid: 1b8e0528-95bc-48fa-9653-2cea66c8dc3a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2fd96396f73b5f33a2a8944e56fb5c8c5fece54a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687555"
---
# <a name="idebugprocessdestroyevent2"></a>IDebugProcessDestroyEvent2
Bu arabirim, bir işlem sonlandırılır, beklenmedik şekilde çıkar veya öğesinden ayrıldı gönderilir.

## <a name="syntax"></a>Sözdizimi

```
IDebugProcessDestroyEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) veya özel bağlantı noktası sağlayıcısı, bir işlem sonlandırıldı bildirmek için bu arabirimi uygulayın. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 DE veya özel bağlantı noktası sağlayıcısı oluşturur ve bu olay bir işlemin sonlandırılması rapor nesnesine gönderir. Kullanarak DE bu olay gönderen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi. Özel bağlantı noktası sağlayıcısı kullanarak bu olay gönderir [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md) arabirimi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
- [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md)