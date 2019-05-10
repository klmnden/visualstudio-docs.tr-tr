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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 3a3418aaa9c2e14454d71d26c0e364ae04244127
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457964"
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
 `Fields`\
 Bayraklarının bir birleşimi [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md) hangi alanların doldurulmuş belirten sabit listesi.

 `bstrFileName`\
 İşlemi tam yol adı. Arama eşdeğer [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md) yöntemi parametresi ile `GN_FILENAME`.

 `bstrBaseName`\
 Uzantı işleminin ve dosya adı. Arama eşdeğer `IDebugProcess2::Getname` yöntemi parametresi ile `GN_BASENAME`.

 `bstrTitle`\
 Varsa işlemin başlığı. Arama eşdeğer `IDebugProcess2::Getname` yöntemi parametresi ile `GN_TITLE`.

 `ProcessId`\
 [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) işlemi tanımlayan yapısı. Arama eşdeğer [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md) yöntemi.

 `dwSessionId`\
 Bu işlem çalışan hata ayıklama oturumu tanımlayıcısı.

 `bstrAttachedSessionName`\
 Ekli oturumun adı. Arama eşdeğer [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md) yöntemi.

 `CreationTime`\
 İşlem oluşturulduğu zaman.

 `Flags`\
 Bayraklarının bir birleşimi [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md) işlem özelliklerini belirten sabit listesi.

## <a name="remarks"></a>Açıklamalar
 Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) yöntemi burada da doldurulur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [PROCESS_INFO_FIELDS](../../../extensibility/debugger/reference/process-info-fields.md)
- [PROCESS_INFO_FLAGS](../../../extensibility/debugger/reference/process-info-flags.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md)
- [GetName](../../../extensibility/debugger/reference/idebugprocess2-getname.md)
- [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)
- [GetAttachedSessionName](../../../extensibility/debugger/reference/idebugprocess2-getattachedsessionname.md)