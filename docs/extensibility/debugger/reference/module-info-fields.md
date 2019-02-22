---
title: MODULE_INFO_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MODULE_INFO_FIELDS
helpviewer_keywords:
- MODULE_INFO_FIELDS enumeration
ms.assetid: 8bed85f4-235f-4192-b58f-5fad7a4d7a78
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f4302a911e58a23bdcd58bb054c1fc90c389fed6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708397"
---
# <a name="moduleinfofields"></a>MODULE_INFO_FIELDS
Hata ayıklama modülü bilgi bayrakları belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_MODULE_INFO_FIELDS { 
   MIF_NONE              = 0x0000,
   MIF_NAME              = 0x0001,
   MIF_URL               = 0x0002,
   MIF_VERSION           = 0x0004,
   MIF_DEBUGMESSAGE      = 0x0008,
   MIF_LOADADDRESS       = 0x0010,
   MIF_PREFFEREDADDRESS  = 0x0020,
   MIF_SIZE              = 0x0040,
   MIF_LOADORDER         = 0x0080,
   MIF_TIMESTAMP         = 0x0100,
   MIF_URLSYMBOLLOCATION = 0x0200,
   MIF_FLAGS             = 0x0400,
   MIF_ALLFIELDS         = 0x07ff
};
typedef DWORD MODULE_INFO_FIELDS;
```

```csharp
public enum enum_MODULE_INFO_FIELDS { 
   MIF_NONE              = 0x0000,
   MIF_NAME              = 0x0001,
   MIF_URL               = 0x0002,
   MIF_VERSION           = 0x0004,
   MIF_DEBUGMESSAGE      = 0x0008,
   MIF_LOADADDRESS       = 0x0010,
   MIF_PREFFEREDADDRESS  = 0x0020,
   MIF_SIZE              = 0x0040,
   MIF_LOADORDER         = 0x0080,
   MIF_TIMESTAMP         = 0x0100,
   MIF_URLSYMBOLLOCATION = 0x0200,
   MIF_FLAGS             = 0x0400,
   MIF_ALLFIELDS         = 0x07ff
};
```

## <a name="members"></a>Üyeler
 MIF_NONE başlatma/kullanım alanları yapısında hiçbiri.

 MIF_NAME başlatma/kullanım `m_bstrName` alanındaki [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) yapısı.

 MIF_URL başlatma/kullanım `m_bstrUrl` alanındaki `MODULE_INFO` yapısı.

 MIF_VERSION başlatma/kullanım `m_bstrVersion` alanındaki `MODULE_INFO` yapısı.

 MIF_DEBUGMESSAGE başlatma/kullanım `m_bstrDebugMessage` alanındaki `MODULE_INFO` yapısı.

 MIF_LOADADDRESS başlatma/kullanım `m_addrLoadAddress` alanındaki `MODULE_INFO` yapısı.

 MIF_PREFFEREDADDRESS başlatma/kullanım `m_addrPreferredLoadAddress` alanındaki `MODULE_INFO` yapısı.

 MIF_SIZE başlatma/kullanım `m_dwSize` alanındaki `MODULE_INFO` yapısı.

 MIF_LOADORDER başlatma/kullanım `m_dwLoadOrder` alanındaki `MODULE_INFO` yapısı.

 MIF_TIMESTAMP başlatma/kullanım `m_TimeStamp` alanındaki `MODULE_INFO` yapısı.

 MIF_URLSYMBOLLOCATION başlatma/kullanım `m_bstrUrlSymbolLocation` alanındaki `MODULE_INFO` yapısı.

 MIF_FLAGS başlatma/kullanım `m_dwModuleFlags` alanındaki `MODULE_INFO` yapısı.

 MIF_ALLFIELDS başlatma/kullanım tüm alanlarda `MODULE_INFO` yapısı.

## <a name="remarks"></a>Açıklamalar
 Bu değerleri bir bağımsız değişken olarak geçirilen [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md) hangi alanları göstermek için yöntemi [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) yapısı olan başlatılacak.

 Bu değerleri de kullanılan `MODULE_INFO` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)