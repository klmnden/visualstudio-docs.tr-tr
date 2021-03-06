---
title: IDebugEngineProgram2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngineProgram2
helpviewer_keywords:
- IDebugEngineProgram2 interface
ms.assetid: 151003a9-2e4d-4acf-9f4d-365dfa6b9596
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 221ab8fd00bc7d98745fdd5cc03dd72b9919b4b2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345131"
---
# <a name="idebugengineprogram2"></a>IDebugEngineProgram2
Bu arabirim, çok iş parçacıklı hata ayıklama desteği sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugEngineProgram2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısını aynı anda birden çok iş parçacığı hata ayıklamayı desteklemek için bu arabirimi uygular. Bu arabirimi uygulayan aynı nesne üzerinde uygulanan [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden almak için bir `IDebugProgram2` arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugEngineProgram2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Stop](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md)|Bu programa tüm iş parçacıkları durdurur.|
|[WatchForThreadStep](../../../extensibility/debugger/reference/idebugengineprogram2-watchforthreadstep.md)|İzleyen yürütme (veya yürütme için İzlemeyi Durdur) için verilen iş parçacığı üzerinde gerçekleşmesi için.|
|[WatchForExpressionEvaluationOnThread](../../../extensibility/debugger/reference/idebugengineprogram2-watchforexpressionevaluationonthread.md)|İfade değerlendirme programı durdurulmuş olsa bile verilen iş parçacığı üzerinde gerçekleşmesi için izin verir (veya izin vermiyor).|

## <a name="remarks"></a>Açıklamalar
 Visual Studio yanıt olarak bu arabirimi çağıran bir [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md) olay ve programın "İş parçacığı adım İzle" ve "İzleme için ifade değerlendirme üzerinde iş parçacığı" durumlarını ayarlama. [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md) zaman çağrılır program durdurulacak; bu yöntem program tüm iş parçacıklarını sonlandırma olanağı verir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)