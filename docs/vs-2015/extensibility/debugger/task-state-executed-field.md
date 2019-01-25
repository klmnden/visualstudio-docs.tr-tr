---
title: TASK_STATE_EXECUTED alanı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- TASK_STATE_EXECUTED field, Task class [.NET Framework debug engines]
ms.assetid: 75b8f9d0-b908-40d0-b109-70feaed2ab0c
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 6dcfb6c7b4b79d1abd2b393e32b9795f613c205a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799254"
---
# <a name="taskstateexecuted-field"></a>TASK_STATE_EXECUTED Alanı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Görev çalışıyor, ancak henüz tamamlanmadı.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)  
  
 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
.field static assembly literal int32 TASK_STATE_EXECUTED = int32(0x00020000)  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa [m_stateFlags](../../extensibility/debugger/m-stateflags-field.md) alan içerir, bu değer <xref:System.Threading.Tasks.Task.Status%2A> özelliği döndürür <xref:System.Threading.Tasks.TaskStatus?displayProperty=fullName>.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Task Sınıfı](../../extensibility/debugger/task-class-internal-members.md)
