---
title: IDebugArrayObject::GetCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugArrayObject::GetCount
helpviewer_keywords:
- IDebugArrayObject::GetCount method
ms.assetid: 7931f3f7-033c-4bf8-8abd-95183952ebb0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ac21ac30e1f4511efa1ec8a7fe27129bf2ddb3a1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66321657"
---
# <a name="idebugarrayobjectgetcount"></a>IDebugArrayObject::GetCount
Dizideki öğe sayısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetCount( 
   DWORD* pdwElements
);
```

```csharp
int GetCount(
   out uint pdwElements
);
```

## <a name="parameters"></a>Parametreler
`pdwElements`\
[out] Sayımını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Çok boyutlu dizi nesnesi olsa bile, bu yöntem, bir dizi nesnesinin tüm öğeleri tek boyutlu dizi görür. Örneğin, bir dizi verilen `myarray[3][2][6]`, bu yöntem, 36 döndürecekti `pdwElements` parametresi. Kullanım [GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md) aynı anda tek tek tek öğeleri almak için yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)