---
title: IDebugArrayField::GetNumberOfElements | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugArrayField::GetNumberOfElements
helpviewer_keywords:
- IDebugArrayField::GetNumberOfElements method
ms.assetid: a1961ef3-d69d-4022-b8c9-b9cfb9811345
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 86cd2b227926db38c5bd50fa0457688a023bc7e3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704117"
---
# <a name="idebugarrayfieldgetnumberofelements"></a>IDebugArrayField::GetNumberOfElements
Dizideki öğe sayısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetNumberOfElements( 
   DWORD* pdwNumElements
);
```

```csharp
int GetNumberOfElements(
   out uint pdwNumElements
);
```

#### <a name="parameters"></a>Parametreler
 `pdwNumElements`

 [out] Dizideki öğelerin sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Döndürülen değer, dizideki boyutların sayısı ne olursa olsun öğelerin toplam sayısıdır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugArrayField](../../../extensibility/debugger/reference/idebugarrayfield.md)