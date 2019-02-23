---
title: IDebugPortSupplierLocale2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugPortSupplierLocale2 interface
ms.assetid: 910e7220-da2a-4339-9fff-9fb1bad3c28c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 252c1e39af112b305b66a92fcfc3f329b743eae0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694016"
---
# <a name="idebugportsupplierlocale2"></a>IDebugPortSupplierLocale2
Bağlantı noktası sağlayıcısı için yerel destek sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugPortSupplierLocale2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Özel bağlantı noktası sağlayıcısı, yerel ayar için bu arabirimi uygular.

## <a name="methods"></a>Yöntemler
 Aşağıdaki tabloda yöntemlerini gösterilmektedir **IDebugPortSupplierLocale2**.

|Yöntem|Açıklama|
|------------|-----------------|
|[SetLocale](../../../extensibility/debugger/reference/idebugportsupplierlocale2-setlocale.md)|Yerel ayarı için bağlantı noktası sağlayıcısı ayarlar.|

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: Portpriv.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
- [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)