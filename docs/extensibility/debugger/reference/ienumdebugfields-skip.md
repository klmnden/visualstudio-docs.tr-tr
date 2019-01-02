---
title: IEnumDebugFields::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugFields::Skip
helpviewer_keywords:
- IEnumDebugFields::Skip method
ms.assetid: b3bc51c4-21ae-4913-800c-c2ca9dc18443
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 0e5704f741883a3d676b0428b358e14debfa7599
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53917062"
---
# <a name="ienumdebugfieldsskip"></a>IEnumDebugFields::Skip
Bu yöntem, belirtilen sayıda öğeyi atlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Skip(  
   ULONG celt  
);  
```  
  
```csharp  
int Skip(  
   uint celt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Geçilecek öğelerin sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa `celt` kalan öğeleri sayısından büyüktür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa `celt` numarasından daha büyük bir değer belirtir, kalan öğeleri numaralandırma sonuna ayarlanır ve `S_FALSE` döndürülür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)