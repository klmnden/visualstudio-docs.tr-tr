---
title: m_stateFlags alanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- m_stateFlags field, Task class [.NET Framework debug engines]
ms.assetid: 82b20efc-08f2-4cd2-91f6-4e01e3da906b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8dee91fa96e16cdc2cd1cd75083c381422a99092
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66330847"
---
# <a name="mstateflags-field"></a>m_stateFlags field
Geçerli durumuyla ilgili bilgileri depolayan <xref:System.Threading.Tasks.Task> nesne.

 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)

 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.field assembly int32 modreq(System.Runtime.CompilerServices.IsVolatile) m_stateFlags
```

## <a name="remarks"></a>Açıklamalar
 Tipik olarak kullandığınız <xref:System.Threading.Tasks.Task.Status%2A?displayProperty=fullName> bu değere erişmek için özelliği.

 Bu üye, aşağıdaki değerlerden herhangi bir birleşimi olabilir:

- [TASK_STATE_EXECUTED](../../extensibility/debugger/task-state-executed-field.md)

- [TASK_STATE_FAULTED](../../extensibility/debugger/task-state-faulted-field.md)

- [TASK_STATE_CANCELED](../../extensibility/debugger/task-state-canceled-field.md)

- [TASK_STATE_WAITING_ON_CHILDREN](../../extensibility/debugger/task-state-waiting-on-children-field.md)

- [TASK_STATE_RAN_TO_COMPLETION](../../extensibility/debugger/task-state-ran-to-completion-field.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md)