---
title: IDebugCoreServer3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCoreServer3
helpviewer_keywords:
- IDebugCoreServer3 interface
ms.assetid: 51f5f41b-a5a4-4df0-a703-41f3d1811d7f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7f9a8e6e16aa9279bb7324f5d08f0da3035f2b85
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66343989"
---
# <a name="idebugcoreserver3"></a>IDebugCoreServer3
Bu arabirim işlemini çalıştıran sunucu ile ilgili bilgilere erişmenizi sağlar.

## <a name="syntax"></a>Sözdizimi

```
IDebugCoreServer3 : IDebugCoreServer2
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
 Visual Studio bu arabirimi uygular.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden almak için bir [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) arabirimi. Bir çağrı [GetServer](../../../extensibility/debugger/reference/idebugdefaultport2-getserver.md) Ayrıca bu arabirimi döndürebilir. Bu arabirim, bir sunucuda (yerel veya uzak) programları'nı başlatmak için özel bağlantı noktası sağlayıcısı tarafından en sık kullanılır.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Yöntemlere ek olarak [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:

|Yöntem|Açıklama|
|------------|-----------------|
|[GetServerName](../../../extensibility/debugger/reference/idebugcoreserver3-getservername.md)|Sunucu adını alır.|
|[GetServerFriendlyName](../../../extensibility/debugger/reference/idebugcoreserver3-getserverfriendlyname.md)|Sunucu adı kullanıcı dostu bir sürümü alır.|
|[EnableAutoAttach](../../../extensibility/debugger/reference/idebugcoreserver3-enableautoattach.md)|Bu işlemleri başlattığınızda işlemleri otomatik olarak eklemek üzere belirli hata ayıklama motorlarını söyler.|
|[DiagnoseWebDebuggingError](../../../extensibility/debugger/reference/idebugcoreserver3-diagnosewebdebuggingerror.md)|Otomatik başarısız eklediğinizde, belirli bir hata kodunu alır.|
|[CreateInstanceInServer](../../../extensibility/debugger/reference/idebugcoreserver3-createinstanceinserver.md)|Sunucuda bir hata ayıklama altyapısı örneğini oluşturur.|
|[QueryIsLocal](../../../extensibility/debugger/reference/idebugcoreserver3-queryislocal.md)|Sunucu çağıran ile aynı makinede olup olmadığını belirten bir bayrak alır.|
|[GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md)|Sunucu ile iletişim kurmak için kullanılan protokol belirten bir değer alır.|
|[DisableAutoAttach](../../../extensibility/debugger/reference/idebugcoreserver3-disableautoattach.md)|Tüm devre dışı bırakır otomatik-bu sunucu bildiği tüm hata ayıklama altyapısı ayarları ekleyin.|

## <a name="remarks"></a>Açıklamalar
 Özel bağlantı noktası sağlayıcısı alır [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) çağırması arabirimi [olay](../../../extensibility/debugger/reference/idebugportevents2-event.md). `IDebugCoreServer3` Arabirimi arabirimden elde edilebilir.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
- [GetServer](../../../extensibility/debugger/reference/idebugdefaultport2-getserver.md)