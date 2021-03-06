---
title: IDebugProgramNode2::Attach_V7 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramNode2::Attach
helpviewer_keywords:
- IDebugProgramNode2::Attach_V7
- IDebugProgramNode2::Attach
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a90b162476872700ee0ec69a3bb9e6e575e7862a
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351178"
---
# <a name="idebugprogramnode2attachv7"></a>IDebugProgramNode2::Attach_V7

> [!Note]
> KULLANIM DIŞI. KULLANMAYIN.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Attach_V7 (
   IDebugProgram2*       pMDMProgram,
   IDebugEventCallback2* pCallback,
   DWORD                 dwReason
);
```

```csharp
int Attach_V7 (
   IDebugProgram2       pMDMProgram,
   IDebugEventCallback2 pCallback,
   uint                 dwReason
);
```

## <a name="parameters"></a>Parametreler

`pMDMProgram`\
[in] [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) eklemek için program temsil eden arabirim.

`pCallback`\
[in] [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) SDM için hata ayıklama olayları göndermek için kullanılan arabirim.

`dwReason`\
[in] Bir değer [ATTACH_REASON](../../../extensibility/debugger/reference/attach-reason.md) ekleme nedenini belirten sabit listesi.

## <a name="return-value"></a>Dönüş Değeri

Bir uygulama her zaman döndürmelidir `E_NOTIMPL`.

## <a name="remarks"></a>Açıklamalar

> [!WARNING]
> Visual Studio 2005 ' ten itibaren bu yöntem artık kullanılmamaktadır ve her zaman döndürmelidir `E_NOTIMPL`. Bkz: [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md) program düğümü, iliştirilemez için göstermek gerekiyorsa veya program düğümü yalnızca program ayarlıyorsanız alternatif bir yaklaşım için arabirim `GUID`. Aksi takdirde uygulama [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi.

## <a name="prior-to-visual-studio-2005"></a>Visual Studio 2005'ten önce

Bu yöntem yalnızca DE ayıklanan programa Adres alanında çalıştırıyorsa uygulanması gerekiyor. Aksi takdirde, bu yöntem döndürmelidir `S_FALSE`.

Bu yöntem çağrıldığında DE göndermelisiniz [IDebugEngineCreateEvent2](../../../extensibility/debugger/reference/idebugenginecreateevent2.md) olay nesne, zaten bu örneği için gönderilmedi, [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) arabirimi yanı sıra [ IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md) ve [IDebugLoadCompleteEvent2](../../../extensibility/debugger/reference/idebugloadcompleteevent2.md) olay nesneleri. [IDebugEntryPointEvent2](../../../extensibility/debugger/reference/idebugentrypointevent2.md) olay nesnesi, ardından gönderilen `dwReason` parametresi `ATTACH_REASON_LAUNCH`.

DE çağırmalı [GetProgramId](../../../extensibility/debugger/reference/idebugprogram2-getprogramid.md) metodunda [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) tarafından sağlanan nesne [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md) olay nesne ve bu programın GUID depolamanız gerekir Örnek verileri `IDebugProgram2` DE tarafından uygulanan bir nesne.

## <a name="see-also"></a>Ayrıca bkz.

- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
- [IDebugProgramNodeAttach2](../../../extensibility/debugger/reference/idebugprogramnodeattach2.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
- [IDebugEngineCreateEvent2](../../../extensibility/debugger/reference/idebugenginecreateevent2.md)
- [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md)
- [IDebugLoadCompleteEvent2](../../../extensibility/debugger/reference/idebugloadcompleteevent2.md)
- [IDebugEntryPointEvent2](../../../extensibility/debugger/reference/idebugentrypointevent2.md)
- [ATTACH_REASON](../../../extensibility/debugger/reference/attach-reason.md)