---
title: GetScheduledTasksForDebugger metodu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- GetScheduledTasksForDebugger method, TaskScheduler class [.NET Framework debug engines]
ms.assetid: 7c9b4cde-6e4a-4cef-929f-7d02b1da5762
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 49a63462eece9bef09579c7284f72790a3914bc2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353725"
---
# <a name="getscheduledtasksfordebugger-method"></a>GetScheduledTasksForDebugger Metodu
Tüm zamanlanmış görevlerin dizisini alır.

 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)

 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.method assembly hidebysig instance class System.Threading.Tasks.Task[] GetScheduledTasksForDebugger() cil managed
```

## <a name="return-value"></a>Dönüş Değeri
 Tüm zamanlanmış görevlerin dizisi. Her görev, yürütülmekte olan veya yürütülmesi tamamlandı.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem iş parçacığı güvenli değildir ve diğer örnekleri aynı anda kullanmamalısınız <xref:System.Threading.Tasks.TaskScheduler>. Bu yöntem bir hata ayıklayıcı'dan aramanızı yalnızca hata ayıklayıcı, diğer tüm iş parçacıkları askıya aldı.

## <a name="see-also"></a>Ayrıca bkz.
- [TaskScheduler sınıfı](../../extensibility/debugger/taskscheduler-class-internal-members.md)