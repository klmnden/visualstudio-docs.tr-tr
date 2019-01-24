---
title: SetNotificationForWaitCompletion metodu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- SetNotificationForWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: da149c9a-20f4-4543-a29e-429c8c1d2e19
caps.latest.revision: 6
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 874e31c331f16e760e030f337dda715473b77af8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753653"
---
# <a name="setnotificationforwaitcompletion-method"></a>SetNotificationForWaitCompletion Metodu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Ayarlar veya TASK_STATE_WAIT_COMPLETION_NOTIFICATION durumu bit temizler.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)  
  
## <a name="syntax"></a>Sözdizimi  
  
```vb  
internal void SetNotificationForWaitCompletion(bool enabled)  
```  
  
#### <a name="parameters"></a>Parametreler  
 `enabled`  
  
 `true` bit ayarlamak için; `false` çok unset bit.  
  
## <a name="exceptions"></a>Özel Durumlar  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklayıcı adım bir zaman uyumsuz yöntem gövdesinin dışında yardımcı olmak için bu bit ayarlar. Varsa `enabled` olduğu `true`, yalnızca henüz tamamlanmamış bir görev üzerinde bu yöntem çağrılmalıdır. Varsa `enabled` olduğu `false`, tamamlanan görevler üzerinde bu yöntem çağrılabilir. Ya da bir olay, yalnızca promise stili görevler için kullanılmalıdır.  
  
## <a name="requirements"></a>Gereksinimler  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Task Sınıfı](../../extensibility/debugger/task-class-internal-members.md)
