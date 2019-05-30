---
title: IEnumDebugBoundBreakpoints2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugBoundBreakpoints2
helpviewer_keywords:
- IEnumDebugBoundBreakpoints2
ms.assetid: ea03e7e1-28d6-40b7-8097-bbb61d3b7caa
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5d81d97cfed8f02973b062367a50d7864f7ed3a8
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322758"
---
# <a name="ienumdebugboundbreakpoints2"></a>IEnumDebugBoundBreakpoints2
Bu arabirim bir bekleyen kesme noktası ile ilişkili bağlı kesme noktaları numaralandırır veya olay Kesme noktasının bağlı.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugBoundBreakpoints2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Hata ayıklama altyapısı (DE), kesme noktaları desteğini bir parçası olarak bu arabirimi uygular. Bu arabirim, kesme noktaları destekleniyorsa uygulanmalıdır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Visual Studio çağırır:

- [EnumBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointevent2-enumbreakpoints.md) bu arabirim tarafından tetiklenen tüm kesme noktalarını listesini temsil eden elde edilir.

- [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointboundevent2-enumboundbreakpoints.md) bağlı olan tüm kesme noktalarını listesini temsil eden bu arabirimi elde edilir.

- [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md) bu arabirim, bekleyen kesme noktasına bağlı tüm kesme noktalarını listesini temsil eden elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugBoundBreakpoints2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-next.md)|Belirtilen bir numaralandırma sıralı bağlı kesme noktaları sayısını alır.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-skip.md)|Bir numaralandırma sıralı bağlı kesme noktaları, belirtilen sayıda atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2-getcount.md)|Bağlı kesme noktaları sayısını bir numaralandırıcı alır.|

## <a name="remarks"></a>Açıklamalar
 Visual Studio IDE'de kesme noktaları görüntüsünü güncelleştirmek için bu arabirim tarafından temsil edilen bağlı kesme noktaları kullanır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointboundevent2-enumboundbreakpoints.md)
- [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)
- [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)