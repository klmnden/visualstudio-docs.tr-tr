---
title: TASK_STATE_EXECUTED alanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- TASK_STATE_EXECUTED field, Task class [.NET Framework debug engines]
ms.assetid: 75b8f9d0-b908-40d0-b109-70feaed2ab0c
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 290404da17b5e66ab447003db966cdb74a9087f0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66348379"
---
# <a name="taskstateexecuted-field"></a>TASK_STATE_EXECUTED alanı
Görev çalışıyor, ancak henüz tamamlanmadı.

 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)

 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.field static assembly literal int32 TASK_STATE_EXECUTED = int32(0x00020000)
```

## <a name="remarks"></a>Açıklamalar
 Varsa [m_stateFlags](../../extensibility/debugger/m-stateflags-field.md) alan içerir, bu değer <xref:System.Threading.Tasks.Task.Status%2A> özelliği döndürür <xref:System.Threading.Tasks.TaskStatus?displayProperty=fullName>.

## <a name="see-also"></a>Ayrıca bkz.
- [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md)