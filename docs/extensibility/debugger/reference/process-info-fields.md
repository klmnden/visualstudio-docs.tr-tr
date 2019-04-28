---
title: PROCESS_INFO_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PROCESS_INFO_FIELDS
helpviewer_keywords:
- PROCESS_INFO_FIELDS enumeration
ms.assetid: 0d9cc345-3d3a-44d8-ae15-a67acb97a828
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 835509048e888e13b91c53d9e35bd03d7aebdfed
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62913507"
---
# <a name="processinfofields"></a>PROCESS_INFO_FIELDS
Hangi tür bilgiler almak için bir işlem için belirtilen.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_PROCESS_INFO_FIELDS { 
   PIF_FILE_NAME             = 0x00000001,
   PIF_BASE_NAME             = 0x00000002,
   PIF_TITLE                 = 0x00000004,
   PIF_PROCESS_ID            = 0x00000008,
   PIF_SESSION_ID            = 0x00000010,
   PIF_ATTACHED_SESSION_NAME = 0x00000020,
   PIF_CREATION_TIME         = 0x00000040,
   PIF_FLAGS                 = 0x00000080,
   PIF_ALL                   = 0x000000ff
};
typedef DWORD PROCESS_INFO_FIELDS;
```

```csharp
public enum enum_PROCESS_INFO_FIELDS { 
   PIF_FILE_NAME             = 0x00000001,
   PIF_BASE_NAME             = 0x00000002,
   PIF_TITLE                 = 0x00000004,
   PIF_PROCESS_ID            = 0x00000008,
   PIF_SESSION_ID            = 0x00000010,
   PIF_ATTACHED_SESSION_NAME = 0x00000020,
   PIF_CREATION_TIME         = 0x00000040,
   PIF_FLAGS                 = 0x00000080,
   PIF_ALL                   = 0x000000ff
};
```

## <a name="members"></a>Üyeler
 PIF_FILE_NAME başlatma/kullanım `bstrFileName` alanını [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) yapısı.

 PIF_BASE_NAME başlatma/kullanım `bstrBaseName` alanını `PROCESS_INFO` yapısı.

 PIF_TITLE başlatma/kullanım `bstrTitle` alanını `PROCESS_INFO` yapısı.

 PIF_PROCESS_ID başlatma/kullanım `ProcessId` alanını `PROCESS_INFO` yapısı.

 PIF_SESSION_ID başlatma/kullanım `dwSessionId` alanını `PROCESS_INFO` yapısı.

 PIF_ATTACHED_SESSION_NAME başlatma/kullanım `bstrAttachedSessionName` alanını `PROCESS_INFO` yapısı.

 PIF_CREATION_TIME başlatma/kullanım `CreationTime` alanını `PROCESS_INFO` yapısı.

 PIF_FLAGS başlatma/kullanım `Flags` alanını `PROCESS_INFO` yapısı.

 PIF_ALL tüm alanları doldurur.

## <a name="remarks"></a>Açıklamalar
 Geçirilen [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) hangi alanları göstermek için yöntemi [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) yapısı olan başlatılacak.

 Ayrıca kullanılan `Fields` alanını `PROCESS_INFO` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)