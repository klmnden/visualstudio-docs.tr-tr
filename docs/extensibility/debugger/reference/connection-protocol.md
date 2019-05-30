---
title: CONNECTION_PROTOCOL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CONNECTION_PROTOCOL
helpviewer_keywords:
- CONNECTION_PROTOCOL enumeration
ms.assetid: 99df5865-8b36-486d-9f4c-d10ae2bc688a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 3f52ef7e723b583d593f6f0d4fc18f5f6909b131
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66346534"
---
# <a name="connectionprotocol"></a>CONNECTION_PROTOCOL
Hata ayıklama paketi (DE) ve hata ayıklama sunucusu arasında iletişim kurmak için kullanılan protokolü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef enum tagCONNECTION_PROTOCOL {
    CONNECTION_NONE    = 0,
    CONNECTION_UNKNOWN = 1,
    CONNECTION_LOCAL   = 2,
    CONNECTION_PIPE    = 3,
    CONNECTION_TCPIP   = 4,
    CONNECTION_HTTP    = 5,
    CONNECTION_OTHER   = 6
} CONNECTION_PROTOCOL;
```

```csharp
public enum CONNECTION_PROTOCOL {
    CONNECTION_NONE    = 0,
    CONNECTION_UNKNOWN = 1,
    CONNECTION_LOCAL   = 2,
    CONNECTION_PIPE    = 3,
    CONNECTION_TCPIP   = 4,
    CONNECTION_HTTP    = 5,
    CONNECTION_OTHER   = 6
};
```

## <a name="fields"></a>Alanlar
`CONNECTION_NONE`\
Bir sunucuya bağlantı yapıldı.

`CONNECTION_UNKNOWN`\
Bir bağlantı yapıldı, ancak bilinmeyen bir türüdür.

`CONNECTION_LOCAL`\
Yerel bir sunucuya bağlantısıdır.

`CONNECTION_PIPE`\
Bir adlandırılmış kanal bağlantıdır.

`CONNECTION_TCPIP`\
Bağlantı, TCP/IP'yi kullanır.

`CONNECTION_HTTP`\
Bağlantı HTTP (bir Web sunucusu üzerinden) kullanır.

`CONNECTION_OTHER`\
Başka türde bir bağlantı kuruldu (Bu değer şu anda kullanılmamaktadır).

## <a name="remarks"></a>Açıklamalar
Bu değerleri döndürülen [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md)
