---
title: IDebugPortSupplier3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier3
helpviewer_keywords:
- IDebugPortSupplier3 interface
ms.assetid: e458cd02-2370-4435-8953-17d7a60ce152
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b471e0799409e68b5a843e39975f54f2ce3b5bc5
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66314155"
---
# <a name="idebugportsupplier3"></a>IDebugPortSupplier3
Bu arabirim, çağıran bir bağlantı noktası sağlayıcısı ve bağlantı noktaları (bunları diske yazarak) hata ayıklayıcı çağrıları arasında korumak daha sonra korunan Bu bağlantı noktalarının bir listesini alın belirlemek sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortSupplier3 : IDebugPortSupplier2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Özel bağlantı noktası sağlayıcısı kalıcı veya bağlantı noktası bilgilerini diske kaydedilirken desteklemek için bu arabirimi uygular. Bu arabirim aynı nesne üzerinde uygulanması gereken [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde `IDebugPortSupplier2` arabirimi bu arabirim elde edilir.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Devralınan yöntemleri yanı sıra [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) arabirimi bu arabirim, aşağıdakileri destekler:

|Yöntem|Açıklama|
|------------|-----------------|
|[CanPersistPorts](../../../extensibility/debugger/reference/idebugportsupplier3-canpersistports.md)|Bağlantı noktası sağlayıcısı bağlantı noktası (bunları diske yazarak) hata ayıklayıcı çağrıları arasında kalıcı olup olmadığını döndürür.|
|[EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md)|Numaralandırılacak Bu bağlantı noktası sağlayıcısı tarafından diske yazılan tüm bağlantı noktaları üzerinden kullanılabilir bir nesne döndürür.|

## <a name="remarks"></a>Açıklamalar
 Bağlantı noktası sağlayıcısı çağrıları arasında küçük bağlantı noktalarına devam ediyorsa, bu arabirimi uygulamalıdır. Bağlantı noktası, bağlantı noktası sağlayıcısı örneği ve bağlantı noktası sağlayıcısı kaldırıldığında diske yazılan yüklenmelidir.

 Hata ayıklama altyapısı genellikle bağlantı noktası sağlayıcısı ile etkileşime girmez ve bu arabirim için herhangi bir kullanıma sahip olur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)