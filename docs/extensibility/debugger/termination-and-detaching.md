---
title: Sonlandırma ve ayırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- programs, termination events
- debug engines, detaching from programs
ms.assetid: 268c1e51-6363-45d1-964c-1ab99bdfa4f9
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8aafb94e0a07462d93cc77a34f7199f61f944d0f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66333721"
---
# <a name="termination-and-detaching"></a>Sonlandırma ve ayırma
Aşağıdaki bölümde, normal sonlandırması açıklanmaktadır.

## <a name="discussion"></a>Tartışma
 Sonra [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) veya [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) arabirimi devam eder, hiçbir kesme noktaları, özel durumlar, çalışma zamanı hataları veya uygulamada hata ayıklaması için sonsuz döngüler varsa hata ayıklanan programa tamamlanana kadar çalışacaktır. Normal sonlandırması işlemidir.

 Göndermeniz gerekir bir [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) normal sonlandırması uygulamak için. Normal sonlandırması gerektiren çalışan [IDebugProgramDestroyEvent2::GetExitCode](../../extensibility/debugger/reference/idebugprogramdestroyevent2-getexitcode.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [Bir özel hata ayıklama altyapısı oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)