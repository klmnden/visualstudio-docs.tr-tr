---
title: BP_LOCATION_CODE_STRING | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_LOCATION_CODE_STRING
helpviewer_keywords:
- BP_LOCATION_CODE_STRING structure
ms.assetid: a4cd71c6-5052-45fe-907b-ebc6ca1df2e4
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0650c7b3c2961531b64539887a1c4c68ac2bc819
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56316216"
---
# <a name="bplocationcodestring"></a>BP_LOCATION_CODE_STRING
Tümleşik geliştirme ortamından (IDE) kullanıcının girebileceği bir dizesini kod kesme noktaları ayarlamak için kullanılır.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_LOCATION_CODE_STRING {
    BSTR bstrContext;
    BSTR bstrCodeExpr;
} BP_LOCATION_CODE_STRING;
```

## <a name="members"></a>Üyeler
`bstrContext`  
Kod içinde kesme, genellikle bir yöntem veya işlev adı olarak görülen bir çağrı yığınında bağlamı.

`bstrCodeExpr`  
Kodu kesme noktası tanımlamak için kullanıcının yazdığı bir dize.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md) yapısı bir birleşimin parçası olarak.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)
