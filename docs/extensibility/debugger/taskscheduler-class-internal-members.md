---
title: TaskScheduler sınıfı - dahili üyeler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- TaskScheduler class [.NET Framework debug engines]
- debug engines, TaskScheduler class [.NET Framework]
ms.assetid: 87f1c969-0217-4464-8907-7609c1bf61d3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cf7b693c058cd69ab2dcb79be787cf5a16d8f8a0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62864029"
---
# <a name="taskscheduler-class---internal-members"></a>TaskScheduler sınıfı - dahili üyeler
Bu makalede iç üyelerine <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName> yardımcı sınıf, bir özel hata ayıklayıcı uygulama. Bu sınıf hakkında genel bilgi için bkz: <xref:System.Threading.Tasks.TaskScheduler> başvurusu makalesinde.

 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)

 Bu iç üyeleri .NET Framework'ten erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.class public abstract auto ansi beforefieldinit System.Threading.Tasks.TaskScheduler
       extends System.Object
```

## <a name="members"></a>Üyeler

### <a name="methods"></a>Yöntemler

|Ad|Açıklama|
|----------|-----------------|
|[GetScheduledTasksForDebugger](../../extensibility/debugger/getscheduledtasksfordebugger-method.md)|Tüm zamanlanmış görevlerin dizisini alır.|
|[GetTaskSchedulersForDebugger](../../extensibility/debugger/gettaskschedulersfordebugger-method.md)|Tüm alır <xref:System.Threading.Tasks.TaskScheduler> şu anda etkin olan nesneler.|

## <a name="remarks"></a>Açıklamalar

## <a name="see-also"></a>Ayrıca bkz.
- <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName>
- [.NET Framework için paralel uzantı dahili bileşenleri](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)