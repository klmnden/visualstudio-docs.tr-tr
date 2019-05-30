---
title: NotifyDebuggerOfWaitCompletion metodu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- NotifyDebuggerOfWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: 841c5908-4f3f-400b-a7b0-96a95f362817
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9a3280a24ad7f9d4045c9a1bff6ca2b44c724325
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350630"
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
- [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md)