---
title: IEnumDebugModules2::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugModules2::Skip
helpviewer_keywords:
- IEnumDebugModules2::Skip
ms.assetid: 61dc42f4-8544-45bb-8da0-fb22cccec7da
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ed27ec339ecc2e0118d784d62c2aec3c41140938
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54989841"
---
# <a name="ienumdebugmodules2skip"></a>IEnumDebugModules2::Skip
Belirtilen sayıda öğeyi üzerinden atlar.  
  
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
 [IEnumDebugModules2](../../../extensibility/debugger/reference/ienumdebugmodules2.md)