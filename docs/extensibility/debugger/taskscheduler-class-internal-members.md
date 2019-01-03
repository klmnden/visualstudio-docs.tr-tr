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
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c86b71e836c49d12c0ec0aceb3a20bf0b38e367a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53853885"
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
 <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName>   
 [.NET Framework için paralel uzantı dahili bileşenleri](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)