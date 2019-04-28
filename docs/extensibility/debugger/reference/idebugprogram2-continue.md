---
title: IDebugProgram2::Continue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::Continue
helpviewer_keywords:
- IDebugProgram2::Continue
ms.assetid: e5a6e02a-d21b-4a03-a034-e8de1f71ce2e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fd13d67917a395eb33e26a53e0db1fed7340c9c6
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412857"
---
# <a name="idebugprogram2continue"></a>IDebugProgram2::Continue
Bu program bir durdurulmuş çalışmaya devam eder. Herhangi bir önceki yürütme durumu (örneğin, bir adım) korunur, ve programı yeniden yürütme.

> [!NOTE]
> Bu metot kullanımdan kaldırılmıştır. Kullanım [devam](../../../extensibility/debugger/reference/idebugprocess3-continue.md) yöntemi yerine.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Continue( 
   IDebugThread2* pThread
);
```

```csharp
int Continue( 
   IDebugThread2 pThread
);
```

#### <a name="parameters"></a>Parametreler
 `pThread`

 [in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) iş parçacığını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, kaç programlar ayıklanan veya hangi program durdurma olayı oluşturan bağımsız olarak bu programı üzerinde çağrılır. Uygulama, önceki yürütme durumu (örneğin, bir adım) korumak ve hiçbir zaman önceki yürütme tamamlamadan önce durmuş gibi sorgulamanıza yürütmeye devam et. Diğer bir deyişle, bir iş parçacığı bu programda bir üzerinden Adımlama ile işlemi yapmakta olduğu ve başka bir programı durduruldu ve ardından bu yöntemi çağrıldı nedeniyle durduruldu, program özgün adımlamayla işlemi tamamlamanız gerekir.

> [!WARNING]
> Durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)