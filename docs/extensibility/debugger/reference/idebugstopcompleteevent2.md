---
title: IDebugStopCompleteEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugStopCompleteEvent2 interface
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d080b3073ffc13b90870b40a16a353634f4aa0cf
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66352020"
---
# <a name="idebugstopcompleteevent2"></a>IDebugStopCompleteEvent2

Bir program durduğunda, hata ayıklama altyapısı (DE) oturum hata ayıklama Yöneticisi (SDM) Bu isteğe bağlı bir olay gönderebilirsiniz.

## <a name="syntax"></a>Sözdizimi

```
IDebugStopCompleteEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar

Bu arabirim, Visual Studio 2005 ile kullanılmaya başlandı. Önceki sürümlerde, zaman uyumsuz durdurma desteklememektedir.

- [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md) SDM senaryolarda, çok işlemli veya çok programı tarafından çağrılır. Bir program için SDM durdurma olay gönderdiğinde SDM çok durdurmak için diğer programları ister.

Durdurma, zaman uyumsuz olarak bir program durduktan SDM bildirmek için kullanılır. SDM bir yorumlayıcı hata ayıklama altyapısı için yararlıdır bildiren, bazen kod hata ayıklaması içinde çalıştığı programı, bunu [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md) zaman uyumlu olarak tamamlanamadı. Hata ayıklama altyapısı bu zaman uyumsuz bildirim görevlendirmek isteyip istemediği, döndürmesi gereken `S_ASYNC_STOP` gelen [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md).

## <a name="requirements"></a>Gereksinimler

Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll