---
title: IDebugProgram2::Execute | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::Execute
helpviewer_keywords:
- IDebugProgram2::Execute
ms.assetid: f7205ce8-0ac6-4fcd-b6ec-b720b4fcaccf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 29839e2f2adb4a0e560b5b58d4226fd61596128c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412853"
---
# <a name="idebugprogram2execute"></a>IDebugProgram2::Execute
Bu program bir durdurulmuş çalışmaya devam eder. Herhangi bir önceki yürütme durumu (örneğin, bir adım) seçili, ve programı yeniden yürütme.

> [!NOTE]
> Bu metot kullanımdan kaldırılmıştır. Kullanım [yürütme](../../../extensibility/debugger/reference/idebugprocess3-execute.md) yöntemi yerine.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Execute(
   void
);
```

```csharp
int Execute();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Yürütme kullanıcı bazı diğer programın iş parçacığının durdurulmuş bir duruma başlatılır, bu programın üzerinde bu yöntem çağrılır. Bu yöntem aynı zamanda Kullanıcı seçtiğinde çağrılır **Başlat** komutunu **hata ayıklama** IDE'de menü. Bu yöntemin uygulanmasını çağırmak kadar basit [sürdürme](../../../extensibility/debugger/reference/idebugthread2-resume.md) programı geçerli işlem parçacığında yöntemi.

> [!WARNING]
> Durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
- [Resume](../../../extensibility/debugger/reference/idebugthread2-resume.md)