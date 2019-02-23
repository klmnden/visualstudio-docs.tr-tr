---
title: CONNECTION_PROTOCOL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CONNECTION_PROTOCOL
helpviewer_keywords:
- CONNECTION_PROTOCOL enumeration
ms.assetid: 99df5865-8b36-486d-9f4c-d10ae2bc688a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2a7d8d056fb816a428d78a8e13455cf6ccdd8a90
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56705839"
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

#### <a name="parameters"></a>Parametreler
Bir sunucuya CONNECTION_NONE Hayır bağlantısı yapıldı.

CONNECTION_UNKNOWN bir bağlantı yapıldı, ancak bilinmeyen bir türüdür.

Yerel bir sunucuya CONNECTION_LOCAL bağlantısıdır.

Bir adlandırılmış kanal CONNECTION_PIPE bağlantısıdır.

CONNECTION_TCPIP bağlantı TCP/IP'yi kullanır.

CONNECTION_HTTP bağlantı (bir Web sunucusu üzerinden) HTTP kullanır.

Başka türde bir bağlantı kuruldu CONNECTION_OTHER (Bu değer şu anda kullanılmamaktadır).

## <a name="remarks"></a>Açıklamalar
Bu değerleri döndürülen [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md)
