---
title: IDebugErrorBreakpoint2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugErrorBreakpoint2
helpviewer_keywords:
- IDebugErrorBreakpoint2 interface
ms.assetid: 1f2a4b94-3713-46e9-8272-3917187792bd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2f25187b2aa88153fcfd712b9dd4b0f651ba8860
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66327795"
---
# <a name="idebugerrorbreakpoint2"></a>IDebugErrorBreakpoint2
Bu arabirim, bir hata veya geçersiz bir konum, geçersiz bir ifade veya neden bekleyen kesme noktasının (kod yüklenmedi henüz, vb.) bağlı değil nedenleri gibi uyarı kesme noktası temsil eder.

## <a name="syntax"></a>Sözdizimi

```
IDebugErrorBreakpoint2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı, kesme noktaları desteğini bir parçası olarak bu arabirimi uygular. Bu arabirim, bir kesme noktası bağlama sorunlarını bildirmek için kullanılır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [GetErrorBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md) bu arabirim alır. Bu arabirim da döndürülebilir (tarafından temsil edilen bir listenin bir parçası olarak bir [IEnumDebugErrorBreakpoints2](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2.md) arabirimi) yapılan bir çağrıyla [CanBind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md) veya [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugErrorBreakpoint2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md)|Hataya neden bekleyen kesme noktasının alır.|
|[GetBreakpointResolution](../../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md)|Hatayı açıklayan bir kesme noktası hata çözünürlüğü alır.|

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugBreakpointErrorEvent2](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md)
- [GetErrorBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md)
- [IEnumDebugErrorBreakpoints2](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2.md)
- [Next](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2-next.md)
- [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)
- [IDebugErrorBreakpointResolution2](../../../extensibility/debugger/reference/idebugerrorbreakpointresolution2.md)