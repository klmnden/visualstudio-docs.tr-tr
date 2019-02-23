---
title: BP_LOCATION_DATA_STRING | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_LOCATION_DATA_STRING
helpviewer_keywords:
- BP_LOCATION_DATA_STRING structure
ms.assetid: 445d6f3f-95b0-47ac-85e2-51b778240687
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 056b7efc01b9536184c3e443156e27e328bdd2b3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689102"
---
# <a name="bplocationdatastring"></a>BP_LOCATION_DATA_STRING
Tümleşik geliştirme ortamından (IDE) kullanıcının girebileceği bir dize temel alan veri kesme noktaları ayarlamak için kullanılır.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_LOCATION_DATA_STRING {
    IDebugThread2* pThread;
    BSTR           bstrContext;
    BSTR           bstrDataExpr;
    DWORD          dwNumElements;
} BP_LOCATION_DATA_STRING;
```

## <a name="members"></a>Üyeler
`pThread` [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) kesme noktası oluştuğu iş parçacığını temsil eden nesne.

`bstrContext` Kod içinde kesme, genellikle bir yöntem veya işlev adı olarak görülen bir çağrı yığınında bağlamı.

`bstrDataExpr` Veri dizesi, kesme noktası ayarlamak için kullanıcı girer.

`dwNumElements` Kesme noktası oluştuğu veri dizedeki öğe sayısı.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) yapısı bir birleşimin parçası olarak.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
