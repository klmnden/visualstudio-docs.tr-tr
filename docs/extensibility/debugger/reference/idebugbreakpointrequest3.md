---
title: IDebugBreakpointRequest3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBreakpointRequest3
helpviewer_keywords:
- IDebugBreakpointRequest3
ms.assetid: 8a042beb-b319-48e3-b3c8-9c8336ab371b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c45b1bae11710063d089aeca61a9d20fb6e907a4
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691104"
---
# <a name="idebugbreakpointrequest3"></a>IDebugBreakpointRequest3
Bu arabirim, oluşturma ve herhangi bir türde kesme noktası bağlama için gereken bilgileri temsil eder. Bir uzantısıdır [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md).

## <a name="syntax"></a>Sözdizimi

```
IDebugBreakpointRequest3 : IDebugBreakpointRequest2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Oturum hata ayıklama Yöneticisi (SDM), genellikle bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Hata ayıklama altyapısı (DE) Bu arabirim çağırarak erişen [QueryInterface](/cpp/atl/queryinterface) çağrıda alınan IDebugBreakpointRequest2 arabirimde [CreatePendingBreakpoint](../../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md), `IDebugBreakpointRequest3` arabirimi aşağıdaki yöntemi kullanıma sunar.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetRequestInfo2](../../../extensibility/debugger/reference/idebugbreakpointrequest3-getrequestinfo2.md)|Bu kesme noktası istek tanımlayan kesme noktası isteği bilgilerini alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim DE ek bilgi sağlamak için kullanılan [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapısı. Bu ek bilgiler DE'ın satıcı kimliği (GUID biçiminde), bir izleme noktası adını ve bir kesme noktası kısıtlama adını içerir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)