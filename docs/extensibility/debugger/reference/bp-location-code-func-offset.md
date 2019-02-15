---
title: BP_LOCATION_CODE_FUNC_OFFSET | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_LOCATION_CODE_FUNC_OFFSET
helpviewer_keywords:
- BP_LOCATION_CODE_FUNC_OFFSET structure
ms.assetid: ab38f7ca-fa01-4cf3-a06c-56cbb7207617
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 90f624bf012354dbd438f0fff079e13da756f079
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318038"
---
# <a name="bplocationcodefuncoffset"></a>BP_LOCATION_CODE_FUNC_OFFSET
Kodda bir işlevdeki bir kesme noktası uzaklık konumunu açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_LOCATION_CODE_FUNC_OFFSET {
    BSTR                     bstrContext;
    IDebugFunctionPosition2* pFuncPos;
} BP_LOCATION_CODE_FUNC_OFFSET;
```

## <a name="members"></a>Üyeler
`bstrContext`  
Kesme noktası bağlamında, genellikle de bir yöntem veya işlev adı olarak görülen bir çağrı yığınında.

`pFuncPos`  
[IDebugFunctionPosition2](../../../extensibility/debugger/reference/idebugfunctionposition2.md) işlevi ve işlev göreli konumunu baştan adını tanımlayan nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) yapısı bir birleşimin parçası olarak.

`pFuncPos` Üye nerede işlev kesme noktası ayarlanacağını gösterir.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)  
[IDebugFunctionPosition2](../../../extensibility/debugger/reference/idebugfunctionposition2.md)
