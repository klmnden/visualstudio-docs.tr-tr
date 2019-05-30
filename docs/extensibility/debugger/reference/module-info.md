---
title: MODULE_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MODULE_INFO
helpviewer_keywords:
- MODULE_INFO structure
ms.assetid: f2e06180-1ab3-4eb5-a428-7994cceb61b6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: db67710fd7ee71cddf1e7dbee030cb208a1de86c
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66339117"
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
 `dwValidFields`\
 Bayraklarının bir birleşimi [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md) hangi alanların doldurulmuş belirten sabit listesi.

 `m_bstrName`\
 Modül adı.

 `m_bstrUrl`\
 Modül URL'si.

 `m_bstrVersion`\
 Modül sürümü.

 `m_bstrDebugMessage`\
 İsteğe bağlı bir ileti modülü hakkında Örneğin, "sembolleri yüklenemiyor."

 `m_addrLoadAddress`\
 Modül yükleme adresi.

 `m_addrPreferredLoadAddress`\
 Modül tercih edilen yükleme adresi.

 `m_dwSize`\
 Modül boyutu.

 `m_dwLoadOrder`\
 Modül yükleme sırası.

 `m_TimeStamp`\
 Sembol dosyası en son değiştirildiği zamanı.

 `m_bstrUrlSymbolLocation`\
 Sembol dosyası konumu (örneğin, ".\\") modülü belirtilmiş. Bir modül için semboller bulmak için bir başlangıç konumu olarak kullanılır.

 `m_dwModuleFlags`\
 Bayraklarının bir birleşimi [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md) modülü açıklayan sabit listesi.

## <a name="remarks"></a>Açıklamalar
 Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md) yöntemi burada da doldurulur.

 Bu yapı, listelenen her bir modülü karşılık gelen **modülleri** penceresi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [MODULE_INFO_FIELDS](../../../extensibility/debugger/reference/module-info-fields.md)
- [MODULE_FLAGS](../../../extensibility/debugger/reference/module-flags.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)
