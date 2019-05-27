---
title: IDebugProcess3::Continue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess3::Continue
helpviewer_keywords:
- IDebugProcess3::Continue
ms.assetid: 57506242-5763-4c08-adb9-8a78ce02cebb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: efd05ffb3d8b6d14f7e1e7732426b1ae453d2f49
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66202468"
---
# <a name="idebugprocess3continue"></a>IDebugProcess3::Continue
Bu işlem durdurulmuş bir duruma çalışmaya devam eder. Herhangi bir önceki yürütme durumu (örneğin, bir adım) korunur, ve işlemi yeniden yürütmeden başlatır.

> [!NOTE]
> Bu yöntem yerine kullanılması gereken [devam](../../../extensibility/debugger/reference/idebugprogram2-continue.md).

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

## <a name="parameters"></a>Parametreler
`pThread`\
[in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) devam etmesi gereken iş parçacığını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, kaç işlemleri ayıklanan veya hangi işlem durdurma olay oluşturulan bağımsız olarak bu işlem çağrılır. Uygulama, önceki yürütme durumu (örneğin, bir adım) korumak ve hiçbir zaman önceki yürütme tamamlamadan önce durmuş gibi sorgulamanıza yürütmeye devam et. Diğer bir deyişle, bir iş parçacığında bu işlem bir üzerinden Adımlama ile işlemi yapmakta olduğu ve başka bir işlem durdurulduğundan durduruldu ve ardından `Continue` çağrıldı, belirtilen iş parçacığı özgün üzerinden Adımlama ile işlemi tamamlamanız gerekir.

 **Uyarı** durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)