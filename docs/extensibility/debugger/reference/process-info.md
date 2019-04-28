---
title: PROCESS_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PROCESS_INFO
helpviewer_keywords:
- PROCESS_INFO structure
ms.assetid: 260c33cc-a05e-4645-84b6-536d0b3b0537
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a18d9a158e69fd18319f187274a2db7d00e24546
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62913484"
---
# <a name="processinfo"></a>PROCESS_INFO
Bir işlem hakkında bilgi içerir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagPROCESS_INFO { 
   PROCESS_INFO_FIELDS Fields;
   BSTR                bstrFileName;
   BSTR                bstrBaseName;
   BSTR                bstrTitle;
   AD_PROCESS_ID       ProcessId;
   DWORD               dwSessionId;
   BSTR                bstrAttachedSessionName;
   FILETIME            CreationTime;
   PROCESS_INFO_FLAGS  Flags;
} PROCESS_INFO;
```

```csharp
public struct PROCESS_INFO { 
   public uint          Fields;
   public string        bstrFileName;
   public string        bstrBaseName;
   public string        bstrTitle;
   public AD_PROCESS_ID ProcessId;
   public uint          dwSessionId;
   public string        bstrAttachedSessionName;
   public FILETIME      CreationTime;
   public uint          Flags;
};
```

## <a name="members"></a>Üyeler
 Bayraklarının bir birleşimi alanları [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md) hangi alanların doldurulmuş belirten sabit listesi.

 bstrFileName işleminin tam yol adı. Arama eşdeğer [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md) yöntemi parametresi ile `GN_FILENAME`.

 bstrBaseName dosya adı ve uzantısı işleminin. Arama eşdeğer `IDebugProcess2::Getname` yöntemi parametresi ile `GN_BASENAME`.

 bstrTitle varsa işlemin başlığı. Arama eşdeğer `IDebugProcess2::Getname` yöntemi parametresi ile `GN_TITLE`.

 ProcessID [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) işlemi tanımlayan yapısı. Arama eşdeğer [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md) yöntemi.

 Bu işlem çalışan hata ayıklama oturumu tanımlayıcısı dwSessionId.

 bstrAttachedSessionName ekli oturum adı. Arama eşdeğer [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md) yöntemi.

 CreationTime işlem oluşturulduğu zaman.

 Bayraklarının bir birleşimi bayrakları [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md) işlem özelliklerini belirten sabit listesi.

## <a name="remarks"></a>Açıklamalar
 Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) yöntemi burada da doldurulur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md)
- [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md)
- [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md)
- [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)
- [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md)