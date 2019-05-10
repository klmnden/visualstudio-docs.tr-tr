---
title: MACHINE_INFO_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MACHINE_INFO_FIELDS
helpviewer_keywords:
- MACHINE_INFO_FIELDS enumeration
ms.assetid: 2d61d206-7d40-4df1-8c88-1b3c9c78821e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 00f1e8ea5487a4eecb6dc9fa1f2b16d18ec3fa07
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65458062"
---
# <a name="machineinfofields"></a>MACHINE_INFO_FIELDS
Hangi tür bilgiler almak için belirli bir makine için belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_MACHINE_INFO_FIELDS { 
   MCIF_NAME  = 0x00000001,
   MCIF_FLAGS = 0x00000002,
   MCIF_ALL   = 0x00000003
};
typedef DWORD MACHINE_INFO_FIELDS;
```

```csharp
public enum enum_MACHINE_INFO_FIELDS { 
   MCIF_NAME  = 0x00000001,
   MCIF_FLAGS = 0x00000002,
   MCIF_ALL   = 0x00000003
};
```

## <a name="fields"></a>Alanlar
 `MCIF_NAME`\
 Başlat/kullanım `bstrName` yapısında alan.

 `MCIF_FLAGS`\
 Başlat/kullanım `Flags` yapısında alan.

 `MIF_ALL`\
 Tüm alanları yapısında başlatma/kullanın.

## <a name="remarks"></a>Açıklamalar
 Bu değerler geçirilecek [GetMachineInfo](../../../extensibility/debugger/reference/idebugcoreserver2-getmachineinfo.md) hangi üyelerinin belirtmek üzere yöntem [MACHINE_INFO](../../../extensibility/debugger/reference/machine-info.md) yapısı olan başlatılacak.

 Ayrıca kullanılan `Fields` üyesi `MACHINE_INFO` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.

 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [MACHINE_INFO](../../../extensibility/debugger/reference/machine-info.md)
- [GetMachineInfo](../../../extensibility/debugger/reference/idebugcoreserver2-getmachineinfo.md)