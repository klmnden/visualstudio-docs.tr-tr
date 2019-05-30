---
title: IDebugPortSupplierEx2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugPortSupplierEx2 interface
ms.assetid: dae0050a-a50a-4f35-bfbd-e538f537b20f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3bebf232e17df54d4dae2392a40f2ccbc3fc711c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353313"
---
# <a name="idebugportsupplierex2"></a>IDebugPortSupplierEx2
Seçin ve bir çekirdek sunucusu ile etkileşim kurmak bağlantı noktası sağlayıcısı için destek sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortSupplierEx2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Çekirdek sunucusunu kullanacak şekilde seçebilmeniz için özel bağlantı noktası sağlayıcısı bu arabirimi uygular.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir **IDebugPortSupplierEx2**.

|Yöntem|Açıklama|
|------------|-----------------|
|[SetServer](../../../extensibility/debugger/reference/idebugportsupplierex2-setserver.md)|Çekirdek sunucusu için bağlantı noktası sağlayıcısı ayarlar.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Portpriv.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
- [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)