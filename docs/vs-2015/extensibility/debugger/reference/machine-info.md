---
title: MACHINE_INFO | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- MACHINE_INFO
helpviewer_keywords:
- MACHINE_INFO structure
ms.assetid: e7564ff2-00b5-4750-8fd5-dc1029a16912
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ac571a1e1c7a9d6cff1caaca40f1c6568f99adf1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546794"
---
# <a name="machineinfo"></a>MACHINE_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belirli bir makine açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef struct tagMACHINE_INFO {   
   MACHINE_INFO_FIELDS Fields;  
   BSTR                bstrName;  
   MACHINE_INFO_FLAGS  Flags;  
} MACHINE_INFO;  
```  
  
```csharp  
public struct MACHINE_INFO {   
   public uint   Fields;  
   public string bstrName;  
   public uint   Flags;  
};  
```  
  
## <a name="members"></a>Üyeler  
 `Fields`  
 Bayraklarının bir birleşimi [MACHINE_INFO_FIELDS](../../../extensibility/debugger/reference/machine-info-fields.md) yapının hangi alanların başlatılır belirten sabit listesi.  
  
 `bstrName`  
 Makine adı. Arama eşdeğer [GetMachineName](../../../extensibility/debugger/reference/idebugcoreserver2-getmachinename.md).  
  
 `Flags`  
 Bayraklarının bir birleşimi [MACHINE_INFO_FLAGS](../../../extensibility/debugger/reference/machine-info-flags.md) makine özniteliklerini açıklayan sabit listesi.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı için bir çağrı tarafından döndürülen [GetMachineInfo](../../../extensibility/debugger/reference/idebugcoreserver2-getmachineinfo.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [MACHINE_INFO_FIELDS](../../../extensibility/debugger/reference/machine-info-fields.md)   
 [GetMachineInfo](../../../extensibility/debugger/reference/idebugcoreserver2-getmachineinfo.md)
