---
title: IDebugProgram3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugProgram3 interface
ms.assetid: 4301ba23-c00c-4ce5-8b1e-3f27da312034
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0cfc29f300bc9f28f857424a7a91b4b6bfd3bf82
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66331522"
---
# <a name="idebugprogram3"></a>IDebugProgram3
Bir işlemde çalışan ve genişleten bir program bu arabirimi temsil eder [yürütme](../../../extensibility/debugger/reference/idebugprogram2-execute.md) iş parçacığı bilgileri sağlayarak.

## <a name="syntax"></a>Sözdizimi

```
IDebugProgram3 : IDebugProgram3
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE) ve özel bağlantı noktası sağlayıcısı bir programda bir işlemi temsil etmek için bu arabirimi uygulayın. Oturum hata ayıklama Yöneticisi (SDM) da bilgileri sağlamak için bu arabirimi uygulayan [iliştirme](../../../extensibility/debugger/reference/idebugprogram2-attach.md).

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md) olay için yeni bir program bu arabirimi döndürür. Bu arabirim, birçok birden çok arabirim yöntemleri için parametre olarak da kullanılır.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgram3`.

|Yöntem|Açıklama|
|------------|-----------------|
|[ExecuteOnThread](../../../extensibility/debugger/reference/idebugprogram3-executeonthread.md)|Program yürütür. İş parçacığı üzerinde hangi iş parçacığının kullanıcı yürütülürken görüntüleyen hata ayıklayıcı bilgiler vermemiz döndürülür.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="remarks"></a>Açıklamalar
 Bir program, bir işlem bir veya daha fazla programlarını oluşur ancak belirli bir çalışma zamanı mimaride çalışan iş parçacığı bir kapsayıcıdır.

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [GetProgram](../../../extensibility/debugger/reference/idebugthread2-getprogram.md)
- [Next](../../../extensibility/debugger/reference/ienumdebugprograms2-next.md)
- [Event](../../../extensibility/debugger/reference/idebugportevents2-event.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)
- [DestroyProgram](../../../extensibility/debugger/reference/idebugengine2-destroyprogram.md)
- [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
- [Attach_V7](../../../extensibility/debugger/reference/idebugprogramnode2-attach-v7.md)