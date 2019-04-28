---
title: PROCESS_INFO_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PROCESS_INFO_FLAGS
helpviewer_keywords:
- PROCESS_INFO_FLAGS enumeration
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 42a596eb8d720a273d89586427232dcf833f8595
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62864988"
---
# <a name="processinfoflags"></a>PROCESS_INFO_FLAGS

Açıklayan veya bir işlem özelliklerini belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_PROCESS_INFO_FLAGS { 
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,
   PIFLAG_PROCESS_STOPPED   = 0x00000004,
   PIFLAG_PROCESS_RUNNING   = 0x00000008,
};
typedef DWORD PROCESS_INFO_FLAGS;
```

```csharp
enum enum_PROCESS_INFO_FLAGS { 
   PIFLAG_SYSTEM_PROCESS    = 0x00000001,
   PIFLAG_DEBUGGER_ATTACHED = 0x00000002,
   PIFLAG_PROCESS_STOPPED   = 0x00000004,
   PIFLAG_PROCESS_RUNNING   = 0x00000008,
};
```

## <a name="members"></a>Üyeler

PIFLAG_SYSTEM_PROCESS işlem bir sistem işlemi olduğunu gösterir.

İşlem bir hata ayıklayıcı tarafından ayıklanmakta olan PIFLAG_DEBUGGER_ATTACHED gösterir. Olabilir bir [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] hata ayıklayıcı veya bazı diğer hata ayıklayıcı, örneğin, WinDbg olabilir.

İşlem durdurulur PIFLAG_PROCESS_STOPPED gösterir. Yalnızca şu durumlarda geçerli `PIFLAG_DEBUGGER_ATTACHED` ayrıca belirtilir. Visual Studio 2005 ve sonraki sürümlerinde kullanılabilir.

İşlem çalışıyor PIFLAG_PROCESS_RUNNING gösterir. Yalnızca şu durumlarda geçerli `PIFLAG_DEBUGGER_ATTACHED` ayrıca belirtilir. Visual Studio 2005 ve sonraki sürümlerinde kullanılabilir.

## <a name="remarks"></a>Açıklamalar

İçin kullanılan `Flags` üyesi [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md) yapısı.

Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler

Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.

- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)