---
title: NotifyDebuggerOfWaitCompletion metodu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- NotifyDebuggerOfWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: 841c5908-4f3f-400b-a7b0-96a95f362817
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 29657a85b72fa57f37a3932465b5aeb874e9a672
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55012397"
---
# <a name="notifydebuggerofwaitcompletion-method"></a>NotifyDebuggerOfWaitCompletion metodu
Hata ayıklayıcı tarafından bir kesme noktası hedefi olarak kullanılan yer tutucu yöntemi. Bu yöntem, satır içine alınmış veya iyileştirilmiş olmamalıdır.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)  
  
## <a name="syntax"></a>Sözdizimi  
  
```vb  
private void NotifyDebuggerOfWaitCompletion()  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Görevle ilgili tüm birleştirme işlemleri, kendi hata ayıklayıcı bildirim biti ayarlanmışsa bu yöntemi çağırmanız gerekir.  
  
## <a name="requirements"></a>Gereksinimler  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md)