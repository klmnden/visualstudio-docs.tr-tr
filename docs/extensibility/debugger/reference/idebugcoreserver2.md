---
title: IDebugCoreServer2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer2
helpviewer_keywords:
- IDebugCoreServer2 interface
ms.assetid: 9c47d0a6-9eb1-464e-bd44-fa2b552d4d36
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3d3f0ea4a9c9cef92feba511afe84f44e06f1f8c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317773"
---
# <a name="idebugcoreserver2"></a>IDebugCoreServer2
Bu arabirim, temsil ve ağ üzerindeki bir makinede bir sunucudan bilgi almak için kullanılır.

## <a name="syntax"></a>Sözdizimi

```
IDebugCoreServer2 : IUknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio, bir sunucu temsil etmek için bu arabirimi uygular. Visual Studio'nun her örneği, bu arabirim bir örneğini oluşturur.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Özel bağlantı noktası sağlayıcısı bir çağrıda bu arabirimin aldığı [olay](../../../extensibility/debugger/reference/idebugportevents2-event.md).

 Bu arabirim için bir çağrı aracılığıyla dolaylı olarak bir hata ayıklama altyapısı elde edebilirsiniz [GetServer](../../../extensibility/debugger/reference/idebugdefaultport2-getserver.md) (döndüren [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md), türetilmiş bir arabirim `IDebugCoreServer2`).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugCoreServer2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[GetMachineInfo](../../../extensibility/debugger/reference/idebugcoreserver2-getmachineinfo.md)|Bir makine özniteliklerini ve adını alır.|
|[GetMachineName](../../../extensibility/debugger/reference/idebugcoreserver2-getmachinename.md)|Bir makine adını alır.|
|[GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)|Bir makinede var olan bağlantı noktası sağlayıcısı alır.|
|[GetPort](../../../extensibility/debugger/reference/idebugcoreserver2-getport.md)|Bir makinede zaten bir bağlantı noktasını alır.|
|[EnumPorts](../../../extensibility/debugger/reference/idebugcoreserver2-enumports.md)|Tüm bağlantı noktaları için bir numaralandırıcı bir makinede oluşturur.|
|[EnumPortSuppliers](../../../extensibility/debugger/reference/idebugcoreserver2-enumportsuppliers.md)|Tüm bağlantı noktası sağlayıcıları için bir numaralandırıcı bir makinede oluşturur.|
|[GetMachineUtilities_V7](../../../extensibility/debugger/reference/idebugcoreserver2-getmachineutilities-v7.md)|Makine yardımcı programlar bir makine için alır.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, ağdaki makineler üzerinde çalışan işlemler göz atmak için Visual Studio tarafından da kullanılır.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [Event](../../../extensibility/debugger/reference/idebugportevents2-event.md)
- [GetServer](../../../extensibility/debugger/reference/idebugdefaultport2-getserver.md)
- [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)