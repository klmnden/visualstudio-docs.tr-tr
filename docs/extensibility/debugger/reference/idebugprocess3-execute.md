---
title: IDebugProcess3::Execute | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess3::Execute
helpviewer_keywords:
- IDebugProcess3::Execute
ms.assetid: d831cd81-d7bf-4172-8517-aa699867791f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 4b2870a50f4ab8bb0358e2e38529e996b143b7ae
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66202390"
---
# <a name="idebugprocess3execute"></a>IDebugProcess3::Execute
Bu işlem durdurulmuş bir duruma çalışmaya devam eder. Herhangi bir önceki yürütme durumu (örneğin, bir adım) temizlenir ve yeniden yürütme işlemini başlatır.

> [!NOTE]
> Bu yöntem yerine kullanılması gereken [yürütme](../../../extensibility/debugger/reference/idebugprogram2-execute.md).

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Execute(
   IDebugThread2* pThread
);
```

```csharp
int Execute(
   IDebugThread2 pThread
);
```

## <a name="parameters"></a>Parametreler
`pThread`\
[in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) yürütülecek iş parçacığını temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Yürütme kullanıcı bazı diğer işlemin iş parçacığında durdurulmuş bir duruma başlatılır, bu işlemi bu yöntem çağrılır. Bu yöntem aynı zamanda Kullanıcı seçtiğinde çağrılır **Başlat** komutunu **hata ayıklama** IDE'de menü. Bu yöntemin uygulanmasını çağırmak kadar basit [sürdürme](../../../extensibility/debugger/reference/idebugthread2-resume.md) işlemdeki geçerli işlem parçacığında yöntemi.

> [!WARNING]
> Durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [Resume](../../../extensibility/debugger/reference/idebugthread2-resume.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)