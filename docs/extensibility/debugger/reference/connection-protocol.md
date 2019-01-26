---
title: CONNECTION_PROTOCOL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: 6d09d751dd51306810f4d0cbb56d701859e2b183
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55036478"
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
 CONNECTION_NONE  
 Bir sunucuya bağlantı yapıldı.  
  
 CONNECTION_UNKNOWN  
 Bir bağlantı yapıldı, ancak bilinmeyen bir türüdür.  
  
 CONNECTION_LOCAL  
 Yerel bir sunucuya bağlantısıdır.  
  
 CONNECTION_PIPE  
 Bir adlandırılmış kanal bağlantıdır.  
  
 CONNECTION_TCPIP  
 Bağlantı, TCP/IP'yi kullanır.  
  
 CONNECTION_HTTP  
 Bağlantı HTTP (bir Web sunucusu üzerinden) kullanır.  
  
 CONNECTION_OTHER  
 Başka türde bir bağlantı kuruldu (Bu değer şu anda kullanılmamaktadır).  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerleri döndürülen [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetConnectionProtocol](../../../extensibility/debugger/reference/idebugcoreserver3-getconnectionprotocol.md)