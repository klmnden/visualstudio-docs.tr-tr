---
title: GetTaskSchedulersForDebugger metodu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- GetTaskSchedulersForDebugger method, TaskScheduler class [.NET Framework debug engines]
ms.assetid: 58aa236a-5ab8-4695-b303-89dffdbcd946
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c763499a053119340ca6827d3190aa4163af4fe0
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49229963"
---
# <a name="gettaskschedulersfordebugger-method"></a>GetTaskSchedulersForDebugger Metodu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Tüm alır <xref:System.Threading.Tasks.TaskScheduler> şu anda etkin olan nesneler.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)  
  
 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
.method assembly hidebysig static class System.Threading.Tasks.TaskScheduler[] GetTaskSchedulersForDebugger() cil managed  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Tüm dizi <xref:System.Threading.Tasks.TaskScheduler> bu şu anda etkin olan nesneler <xref:System.AppDomain>.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem iş parçacığı güvenli değildir ve diğer örnekleri aynı anda kullanılmamalıdır <xref:System.Threading.Tasks.TaskScheduler>. Yalnızca hata ayıklayıcı, diğer tüm iş parçacıkları askıya olduğunda bir hata ayıklayıcı'dan çağrılmalıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [TaskScheduler Sınıfı](../../extensibility/debugger/taskscheduler-class-internal-members.md)

