---
title: AD_PROCESS_ID | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- AD_PROCESS_ID
helpviewer_keywords:
- AD_PROCESS_ID union
ms.assetid: 4cb40d12-2e92-4f09-83f4-689928bd65b3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e03b51081b082c1180091e823eead47a21a7b3d2
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315436"
---
# <a name="adprocessid"></a>AD_PROCESS_ID
Sistem kimliği veya bir GUID olabilir işlem Kimliğini belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _AD_PROCESS_ID {
    AD_PROCESS_ID_TYPE ProcessIdType;
    union {
        DWORD dwProcessId; 
        GUID  guidProcessId; 
        DWORD dwUnused; 
    } ProcessId;
} AD_PROCESS_ID;
```

```csharp
public struct AD_PROCESS_ID {
    AD_PROCESS_ID_TYPE ProcessIdType;
    DWORD              dwProcessId; 
    GUID               guidProcessId; 
    DWORD              dwUnused; 
};
```

## <a name="members"></a>Üyeler
`ProcessIdType`  
Bir değer [AD_PROCESS_ID_TYPE](../../../extensibility/debugger/reference/ad-process-id-type.md) yorumlama belirten sabit listesi `ProcessId` birleşim (ya da yönetilen kod için erişmek için üye yapısı).

dwProcessId  
Sistem arasında bir değer olarak işlem kimliği.

guidProcessId  
İşlem kimliği bir GUID olarak.

dwUnused  
Doldurma.

## <a name="remarks"></a>Açıklamalar
Bu yapı için aşağıdaki yöntemlerden geçirilir:

- [GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md)

- [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md)

- [GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)

- [GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md)

Ve aşağıdaki yöntemlerden döndürülen:

- [GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)

- [GetHostId](../../../extensibility/debugger/reference/idebugprogramhost2-gethostid.md)

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md)  
[PROCESS_INFO](../../../extensibility/debugger/reference/process-info.md)  
[AD_PROCESS_ID_TYPE](../../../extensibility/debugger/reference/ad-process-id-type.md)  
[GetPhysicalProcessId](../../../extensibility/debugger/reference/idebugprocess2-getphysicalprocessid.md)  
[GetHostId](../../../extensibility/debugger/reference/idebugprogramhost2-gethostid.md)  
[GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md)  
[WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md)  
[GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)
