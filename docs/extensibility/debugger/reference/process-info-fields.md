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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 28af715c307ebede5fa264c46cd42b85e8868674
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457954"
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

## <a name="fields"></a>Alanlar
 `PIF_FILE_NAME`\
 Başlat/kullanım `bstrFileName` alanını [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) yapısı.

 `PIF_BASE_NAME`\
 Başlat/kullanım `bstrBaseName` alanını `PROCESS_INFO` yapısı.

 `PIF_TITLE`\
 Başlat/kullanım `bstrTitle` alanını `PROCESS_INFO` yapısı.

 `PIF_PROCESS_ID`\
 Başlat/kullanım `ProcessId` alanını `PROCESS_INFO` yapısı.

 `PIF_SESSION_ID`\
 Başlat/kullanım `dwSessionId` alanını `PROCESS_INFO` yapısı.

 `PIF_ATTACHED_SESSION_NAME`\
 Başlat/kullanım `bstrAttachedSessionName` alanını `PROCESS_INFO` yapısı.

 `PIF_CREATION_TIME`\
 Başlat/kullanım `CreationTime` alanını `PROCESS_INFO` yapısı.

 `PIF_FLAGS`\
 Başlat/kullanım `Flags` alanını `PROCESS_INFO` yapısı.

 `PIF_ALL`\
 Tüm alanları doldurur.

## <a name="remarks"></a>Açıklamalar
 Geçirilen [GetInfo](../../../extensibility/debugger/reference/idebugprocess2-getinfo.md) hangi alanları göstermek için yöntemi [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) yapısı olan başlatılacak.

 Ayrıca kullanılan `Fields` alanını `PROCESS_INFO` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)