---
title: BP_LOCATION_CODE_CONTEXT | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_LOCATION_CODE_CONTEXT
helpviewer_keywords:
- BP_LOCATION_CODE_CONTEXT structure
ms.assetid: 37412896-021a-4f73-9bb7-4125502c2e18
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c98f1e1e6c516cc2cf2085a3808c5eb08d33be61
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315787"
---
# <a name="bplocationcodecontext"></a>BP_LOCATION_CODE_CONTEXT
Hata ayıklanan programa bir adres için doğrudan bağlı bir kesme noktası konumu açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_LOCATION_CODE_CONTEXT {
    IDebugCodeContext2* pCodeContext;
} BP_LOCATION_CODE_CONTEXT;
```

## <a name="members"></a>Üyeler
pCodeContext  
[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) kod kesme noktası konumunu tanımlayan nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) yapısı bir birleşimin parçası olarak.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)  
[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
