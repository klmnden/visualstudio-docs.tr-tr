---
title: IDebugDefaultPort2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDefaultPort2
helpviewer_keywords:
- IDebugDefaultPort2 interface
ms.assetid: 7b3452af-9a96-4c4c-9946-4339b72d3d7b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7e646a248e4b7da03a9dbad9bcea2470d9d0f450
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718865"
---
# <a name="idebugdefaultport2"></a>IDebugDefaultPort2
Bu arabirim bir bağlantı noktasının sunucusu ve bildirim olanakları erişmek için çeşitli yöntemler sunar.

## <a name="syntax"></a>Sözdizimi

```
IDebugDefaultPort2 : IDebugPort2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio erişim programları için hata ayıklama bağlantı temsil etmek için bu arabirimi uygular. Uzaktan hata ayıklama işliyorsa özel bağlantı noktası sağlayıcısı Ayrıca bu arabirim uygulayabilir.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Bağımsız değişken üzerinde yöntemleri [IDebugProgramProvider2](../../../extensibility/debugger/reference/idebugprogramprovider2.md) arabirimi bu arabirim sağlar. Çağırma [QueryInterface](/cpp/atl/queryinterface) üzerinde bir [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) arabirimi bu arabirim de edinebilirsiniz.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 İçinde tanımlanan yöntemleri yanı sıra [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md), aşağıdaki yöntemlerden bu arabirimi uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetPortNotify](../../../extensibility/debugger/reference/idebugdefaultport2-getportnotify.md)|Bağlantı noktası bildirim arabirimi Bu bağlantı noktasından alır.|
|[GetServer](../../../extensibility/debugger/reference/idebugdefaultport2-getserver.md)|Bu bağlantı noktasını barındıran sunucuya arabirimini alır.|
|[QueryIsLocal](../../../extensibility/debugger/reference/idebugdefaultport2-queryislocal.md)|Bu bağlantı noktasını yerel makinede çalışıp çalışmadığını belirler.|

## <a name="remarks"></a>Açıklamalar
 Adı "`IDebugDefaultPort2`" varsayılan bağlantı noktası göstermiyor biraz bir misnomer aynıdır. "IDebugPort3." çağrılabilir

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugProgramProvider2](../../../extensibility/debugger/reference/idebugprogramprovider2.md)