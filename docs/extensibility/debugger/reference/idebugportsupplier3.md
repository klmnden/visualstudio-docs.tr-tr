---
title: IDebugPortSupplier3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortSupplier3
helpviewer_keywords:
- IDebugPortSupplier3 interface
ms.assetid: e458cd02-2370-4435-8953-17d7a60ce152
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ca7113a1b108713b5dd7cf0f17511cec39a1b8b6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62918003"
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

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)