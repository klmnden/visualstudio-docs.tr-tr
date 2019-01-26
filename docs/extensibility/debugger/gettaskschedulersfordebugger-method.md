---
title: GetTaskSchedulersForDebugger metodu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- GetTaskSchedulersForDebugger method, TaskScheduler class [.NET Framework debug engines]
ms.assetid: 58aa236a-5ab8-4695-b303-89dffdbcd946
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 76229d86c973c9ef512ecf5039ae420085129160
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55029251"
---
# <a name="gettaskschedulersfordebugger-method"></a>GetTaskSchedulersForDebugger Metodu
Tüm alır <xref:System.Threading.Tasks.TaskScheduler> şu anda etkin olan nesneler.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)  
  
 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp  
.method assembly hidebysig static class System.Threading.Tasks.TaskScheduler[] GetTaskSchedulersForDebugger() cil managed  
```  
  
## <a name="return-value"></a>Dönüş değeri  
 Tüm dizi <xref:System.Threading.Tasks.TaskScheduler> bu şu anda etkin olan nesneler <xref:System.AppDomain>.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem iş parçacığı güvenli değildir ve diğer örnekleri aynı anda kullanmamalısınız <xref:System.Threading.Tasks.TaskScheduler>. Bu yöntem bir hata ayıklayıcı'dan aramanızı yalnızca hata ayıklayıcı, diğer tüm iş parçacıkları askıya aldı.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [TaskScheduler sınıfı](../../extensibility/debugger/taskscheduler-class-internal-members.md)