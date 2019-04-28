---
title: MODULE_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MODULE_INFO
helpviewer_keywords:
- MODULE_INFO structure
ms.assetid: f2e06180-1ab3-4eb5-a428-7994cceb61b6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0e3a11e368b6260d00f3f6ed0b19d94aa26bd31a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62865472"
---
# <a name="moduleinfo"></a>MODULE_INFO
Belirli bir modülün (DLL, EXE veya derleme) açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagMODULE_INFO { 
   MODULE_INFO_FIELDS dwValidFields;
   BSTR               m_bstrName;
   BSTR               m_bstrUrl;
   BSTR               m_bstrVersion;
   BSTR               m_bstrDebugMessage;
   UINT64             m_addrLoadAddress;
   UINT64             m_addrPreferredLoadAddress;
   DWORD              m_dwSize;
   DWORD              m_dwLoadOrder;
   FILETIME           m_TimeStamp;
   BSTR               m_bstrUrlSymbolLocation;
   MODULE_FLAGS       m_dwModuleFlags;
} MODULE_INFO;
```

```csharp
public struct MODULE_INFO { 
   public uint     dwValidFields;
   public string   m_bstrName;
   public string   m_bstrUrl;
   public string   m_bstrVersion;
   public string   m_bstrDebugMessage;
   public ulong    m_addrLoadAddress;
   public ulong    m_addrPreferredLoadAddress;
   public uint     m_dwSize;
   public uint     m_dwLoadOrder;
   public FILETIME m_TimeStamp;
   public string   m_bstrUrlSymbolLocation;
   public uint     m_dwModuleFlags;
};
```

## <a name="members"></a>Üyeler
 bayrakları birleşimi dwValidFields A [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md) hangi alanların doldurulmuş belirten sabit listesi.

 m_bstrName modül adı.

 m_bstrUrl modülü URL.

 m_bstrVersion Modül sürümü.

 m_bstrDebugMessage isteğe bağlı bir ileti modülü hakkında Örneğin, "sembolleri yüklenemiyor."

 Adres m_addrLoadAddress modülünü yükleyin.

 m_addrPreferredLoadAddress modülünün tercih edilen yük adresi.

 m_dwSize modül boyutu.

 Modül yükleme sırasında m_dwLoadOrder.

 Sembol dosyası en son değiştirildiği zamanı m_TimeStamp.

 m_bstrUrlSymbolLocation sembol dosyasının konumunu (örneğin, ".\\") modülü belirtilmiş. Bir modül için semboller bulmak için bir başlangıç konumu olarak kullanılır.

 bayrakları birleşimi m_dwModuleFlags A [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md) modülü açıklayan sabit listesi.

## <a name="remarks"></a>Açıklamalar
 Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md) yöntemi burada da doldurulur.

 Bu yapı, listelenen her bir modülü karşılık gelen **modülleri** penceresi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md)
- [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)