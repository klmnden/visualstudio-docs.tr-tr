---
title: Hata ayıklayıcıyı başlatma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], launching the debugger
- debugger [Debugging SDK], launching
ms.assetid: f24da1a1-f923-48b4-989f-18a22b581d1b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 99b8dcd9647cf9a55bd5cc29d082c8d79e57f302
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353842"
---
# <a name="launch-the-debugger"></a>Hata ayıklayıcıyı başlatma
Hata ayıklayıcıyı başlatma, yöntemlerini ve olaylarını uygun öznitelikleriyle birlikte doğru sırasını gönderilmesi gerekir.

## <a name="sequences-of-methods-and-events"></a>Dizileri yöntemler ve olaylar

1. Oturum hata ayıklama Yöneticisi (SDM) seçerek çağrılır **hata ayıklama** menüsüne ve ardından **Başlat**. Daha fazla bilgi için [bir program Başlat](../../extensibility/debugger/launching-a-program.md).

2. SDM çağrıları [OnAttach](../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) yöntemi.

3. Hata ayıklama altyapısı (DE) işlem modelini temel alan `IDebugProgramNodeAttach2::OnAttach` yöntemi ne olacağını belirler aşağıdaki yöntemlerden birini döndürür.

     Varsa `S_FALSE` hata ayıklama altyapısı (DE), sanal makine aşamasındayız yüklenecek döndürülür.

     -veya-

     Varsa `S_OK` DE, yüklenecek döndürülür işlemdeki SDM biri. SDM sonra aşağıdaki görevleri gerçekleştirir:

    1. Çağrıları [GetEngineInfo](../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md) altyapısı DE almak için.

    2. Birlikte DE oluşturur.

    3. Çağrıları [ekleme](../../extensibility/debugger/reference/idebugengine2-attach.md).

4. DE gönderen bir [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği.

5. DE gönderen bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği.

6. DE gönderen bir [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği.

7. DE gönderen bir [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği.

8. DE gönderen bir [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)
- [Program başlatma](../../extensibility/debugger/launching-a-program.md)