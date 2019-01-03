---
title: SetNotificationForWaitCompletion metodu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- SetNotificationForWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: da149c9a-20f4-4543-a29e-429c8c1d2e19
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4b488bcfb37696f4e18c8f32741e8f3ef861aed8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53986121"
---
# <a name="setnotificationforwaitcompletion-method"></a>SetNotificationForWaitCompletion Metodu
Ayarlar veya TASK_STATE_WAIT_COMPLETION_NOTIFICATION durumu bit temizler.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)  
  
## <a name="syntax"></a>Sözdizimi  
  
```vb  
internal void SetNotificationForWaitCompletion(bool enabled)  
```  
  
### <a name="parameters"></a>Parametreler  
 `enabled`  
  
 `true` bit ayarlamak için; `false` çok unset bit.  
  
## <a name="exceptions"></a>Özel Durumlar  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklayıcı adım bir zaman uyumsuz yöntem gövdesinin dışında yardımcı olmak için bu bit ayarlar. Varsa `enabled` olduğu `true`, yalnızca henüz tamamlanmamış bir görev üzerinde bu yöntem çağrılmalıdır. Zaman `enabled` olduğu `false`, tamamlanan görevler üzerinde bu yöntem çağrılabilir. Ya da bir olay, yalnızca promise stili görevler için kullanılmalıdır.  
  
## <a name="requirements"></a>Gereksinimler  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md)