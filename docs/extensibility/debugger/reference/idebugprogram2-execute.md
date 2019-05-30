---
title: IDebugProgram2::Execute | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::Execute
helpviewer_keywords:
- IDebugProgram2::Execute
ms.assetid: f7205ce8-0ac6-4fcd-b6ec-b720b4fcaccf
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 27730528b552e4a545725a7a7463475be6038bba
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329804"
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

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
- [Resume](../../../extensibility/debugger/reference/idebugthread2-resume.md)