---
title: IDebugPortEvents2::Event | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortEvents2::Event
helpviewer_keywords:
- IDebugPortEvents2::Event
ms.assetid: 5cc813f7-04a1-4462-9ea7-fbddcf0e0143
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 6ede9055f97a796e4e007914f68e370d4ff81420
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66326754"
---
# <a name="idebugportevents2event"></a>IDebugPortEvents2::Event
Bu yöntem, oluşturma ve yok etme süreçleri ve bağlantı noktası programlar geldiğiniz olayları gönderir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Event(
   IDebugCoreServer2* pServer,
   IDebugPort2*       pPort,
   IDebugProcess2*    pProcess,
   IDebugProgram2*    pProgram,
   IDebugEvent2*      pEvent,
   REFIID             riidEvent
);
```

```csharp
int Event(
   IDebugCoreServer2 pServer,
   IDebugPort2       pPort,
   IDebugProcess2    pProcess,
   IDebugProgram2    pProgram,
   IDebugEvent2      pEvent,
   ref Guid          riidEvent
);
```

## <a name="parameters"></a>Parametreler
`pMachine`\
[in] Bir [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) hata ayıklama sunucusu temsil eden nesne (bir, her örneği için [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]) olayın gerçekleştiği içinde.

`pPort`\
[in] Bir [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) olayın gerçekleştiği bağlantı noktasını temsil eden nesne.

`pProcess`\
[in] Bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) olayın gerçekleştiği işlemini temsil eden nesne.

`pProgram`\
[in] Bir [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) olayın gerçekleştiği program temsil eden nesne.

`pEvent`\
[in] Bir [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) olay tanımlayan nesne. Olası olayları aşağıdaki gibidir:

- [IDebugProcessCreateEvent2](../../../extensibility/debugger/reference/idebugprocesscreateevent2.md)

- [IDebugProcessDestroyEvent2](../../../extensibility/debugger/reference/idebugprocessdestroyevent2.md)

- [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md)

- [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md)

`riidEvent`\
[in] Olayın GUID. Olay türüne dönüştürülür çünkü [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) bu yöntemi çağırmadan önce bu tanımlayıcı, hangi olay gönderilen belirlemek kolaylaştırır.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md)
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)