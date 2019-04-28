---
title: IDebugPortNotify2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortNotify2
helpviewer_keywords:
- IDebugPortNotify2 interface
ms.assetid: 43278b79-bf16-4c08-bcf1-6f7f7a17feab
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2427bfbc70c992cfcd41217aec56aa94d825faae
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62918175"
---
# <a name="idebugportnotify2"></a>IDebugPortNotify2
Bu arabirim kaydeder veya üzerinde çalıştığı bağlantı noktası ile ayıklanabilir bir program kaydını siler.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortNotify2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Özel bağlantı noktası sağlayıcısı ekleme ve kaldırma bağlantı noktasından desteklemek için bu arabirimi uygular. Genellikle uygulayan aynı nesne üzerinde uygulanan [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) arabirimi.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bir çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde `IDebugPort2` arabirimi bu arabirim döndürür. Ayrıca, bir çağrı [GetPortNotify](../../../extensibility/debugger/reference/idebugdefaultport2-getportnotify.md) bu arabirimi döndürür. Hata ayıklama altyapısı, bir parametre olarak bu arabirimi görebilirsiniz [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md).

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortNotify2`.

|Yöntem|Açıklama|
|------------|-----------------|
|[AddProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)|Hata ayıklaması yapılabilir bir program çalıştığı bağlantı noktası ile kaydeder.|
|[RemoveProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md)|Bir program çalıştığı bağlantı noktasından ayıklanabilir kaydını siler.|

## <a name="remarks"></a>Açıklamalar
 Özel bağlantı noktası sağlayıcısı, hata ayıklama bağlantı programlar zaman yüklü veya kaldırılmış bilmenin bir yolu olmadığı sürece, bu arabirimini uygulaması gerekir. Belirli bir bağlantı noktası üzerinden hata ayıklama için yüklenen tüm programlar bu arabirimi kullanılarak izlenir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)