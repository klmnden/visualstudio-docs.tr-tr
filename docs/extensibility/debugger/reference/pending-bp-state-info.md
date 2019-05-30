---
title: PENDING_BP_STATE_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PENDING_BP_STATE_INFO
helpviewer_keywords:
- PENDING_BP_STATE_INFO structure
ms.assetid: 4d73ceff-43f9-4e95-8dba-88e1fab2def3
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 306f3f6ac5f12d2a26da958d50fae87c6e174355
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66349884"
---
# <a name="pendingbpstateinfo"></a>PENDING_BP_STATE_INFO
Bir kod konuma bağlamak hazır bir kesme noktası durumu hakkında bilgi içerir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagPENDING_BP_STATE_INFO { 
   PENDING_BP_STATE       state;
   PENDING_BP_STATE_FLAGS flags;
} PENDING_BP_STATE_INFO;
```

```csharp
public struct PENDING_BP_STATE_INFO { 
   public uint state;
   public uint flags;
};
```

## <a name="members"></a>Üyeler
 `state`\
 Bir değer [PENDING_BP_STATE](../../../extensibility/debugger/reference/pending-bp-state.md) bekleyen kesme noktasının durumunu belirten sabit listesi.

 `flags`\
 Bayraklarının bir birleşimi [PENDING_BP_STATE_FLAGS](../../../extensibility/debugger/reference/pending-bp-state-flags.md) kesme noktası sanallaştırılmış olup olmadığını belirten sabit listesi.

## <a name="remarks"></a>Açıklamalar
 Bu yapı geçirilir [GetState](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getstate.md) yöntemi burada da doldurulur.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetState](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-getstate.md)
- [PENDING_BP_STATE](../../../extensibility/debugger/reference/pending-bp-state.md)
- [PENDING_BP_STATE_FLAGS](../../../extensibility/debugger/reference/pending-bp-state-flags.md)