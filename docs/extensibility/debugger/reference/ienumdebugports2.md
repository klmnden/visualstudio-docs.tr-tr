---
title: IEnumDebugPorts2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugPorts2
helpviewer_keywords:
- IEnumDebugPorts2
ms.assetid: 1754eef3-cf62-42e0-b218-1911acba77d4
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c24edcd5ef47408cd4c11b3d0548ad34516702a1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66326512"
---
# <a name="ienumdebugports2"></a>IEnumDebugPorts2
Bu arabirim, makine veya bağlantı noktası tedarikçi bağlantı noktalarını numaralandırır.

## <a name="syntax"></a>Sözdizimi

```
IEnumDebugPorts2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Özel bağlantı noktası sağlayıcısı sağlayıcı tarafından oluşturulan bağlantı noktalarının bir listesini göstermek için bu arabirimi uygular. Visual Studio, kendi bağlantı noktası sağlayıcısı desteklemek üzere bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md) bağlantı noktası sağlayıcısı tarafından oluşturulan bağlantı noktalarının bir listesini temsil eden bu arabirimi elde edilir. Çağrı [EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md) kaydedildi bağlantı noktalarının bir listesini temsil eden bu arabirimi almak için diske.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugPorts2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[Next](../../../extensibility/debugger/reference/ienumdebugports2-next.md)|Belirtilen bir sabit listesi sırası rastgele bağlantı sayısını alır.|
|[Skip](../../../extensibility/debugger/reference/ienumdebugports2-skip.md)|Bir sabit listesi sırası rastgele bağlantı belirtilen sayıda atlar.|
|[Reset](../../../extensibility/debugger/reference/ienumdebugports2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|
|[Clone](../../../extensibility/debugger/reference/ienumdebugports2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugports2-getcount.md)|Bağlantı noktası sayısını bir numaralandırıcı alır.|

## <a name="remarks"></a>Açıklamalar
 Visual Studio işlemlere ekleme için kullanılan bağlantı noktaları listesini doldurmak için bu arabirimi kullanır.

 Hata ayıklama altyapısı, genellikle bu arabirimi kullanmaz.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [EnumPorts](../../../extensibility/debugger/reference/idebugcoreserver2-enumports.md)
- [EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md)