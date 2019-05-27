---
title: IDebugProgram2::Step | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::Step
helpviewer_keywords:
- IDebugProgram2::Step
ms.assetid: e4c2ffce-9810-4088-8162-eac9ef04f2a9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 37ff30958d0f8343c5dc77c441087334524d3cd1
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212546"
---
# <a name="idebugprogram2step"></a>IDebugProgram2::Step
Bir adımı gerçekleştirir.

> [!NOTE]
> Bu metot kullanımdan kaldırılmıştır. Kullanım [adım](../../../extensibility/debugger/reference/idebugprocess3-step.md) yöntemi yerine.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Step( 
   IDebugThread2*  pThread,
   STEPKIND        sk,
   STEPUNIT        step
);
```

```csharp
int Step( 
   IDebugThread2  pThread,
   enum_STEPKIND  sk,
   enum_STEPUNIT  step
);
```

## <a name="parameters"></a>Parametreler
`pThread`\
[in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) basamaklı iş parçacığını temsil eden nesne.

`sk`\
[in] Bir değer [STEPKIND](../../../extensibility/debugger/reference/stepkind.md) adım türünü belirten sabit listesi.

`step`\
[in] Bir değer [STEPUNIT](../../../extensibility/debugger/reference/stepunit.md) adım birimini (örneğin, ifade veya yönerge) belirten sabit listesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Belirli bir iş parçacığının adımlanırken durumunda herhangi bir iş parçacığı eşitleme veya iş parçacıkları arasındaki iletişim, programdaki diğer iş parçacıklarını çalıştırmanız gerekir.

> [!WARNING]
> Durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)