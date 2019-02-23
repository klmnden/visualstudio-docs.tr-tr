---
title: SetNotificationForWaitCompletion metodu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- SetNotificationForWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: da149c9a-20f4-4543-a29e-429c8c1d2e19
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 468850a441cfd0bc87155fd746d8578c6b763e66
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56714393"
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
- [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md)