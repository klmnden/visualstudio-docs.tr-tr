---
title: IDebugErrorBreakpointResolution2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugErrorBreakpointResolution2
helpviewer_keywords:
- IDebugErrorBreakpointResolution2
ms.assetid: b1234216-0ac8-461d-b2a7-54f60f8f3262
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 093b3ae1bd58113941d1031559dadd55cb704475
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66327754"
---
# <a name="idebugerrorbreakpointresolution2"></a>IDebugErrorBreakpointResolution2
Bu arabirim, bir kesme noktası hatası çözünürlüğünü temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugErrorBreakpointResolution2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı, kesme noktaları desteğini bir parçası olarak bu arabirimi uygular. Bu arabirim, bağlamak bir kesme noktası başarısız olduğu bildirmek için kullanılır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [GetBreakpointResolution](../../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md) bağlamak kesme noktası başarısız olduğu hakkında bilgi sağlamak için bu arabirimi döndürür. [GetErrorBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md) yöntemi alır [IDebugErrorBreakpoint2](../../../extensibility/debugger/reference/idebugerrorbreakpoint2.md) arabirimi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugErrorBreakpointResolution2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetBreakpointType](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2-getbreakpointtype.md)|Kesme noktası türünü alır.|
|[GetResolutionInfo](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2-getresolutioninfo.md)|Kesme noktası çözümleme bilgilerini alır.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugErrorBreakpoint2](../../../extensibility/debugger/reference/idebugerrorbreakpoint2.md)
- [GetBreakpointResolution](../../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md)
- [GetErrorBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md)