---
title: IEnumDebugCustomAttributes::Next | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumCustomAttributes::Next
helpviewer_keywords:
- IEnumDebugCustomAttributes::Next
ms.assetid: e36f856b-2619-42d1-b73e-4f2390fc22bd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a418fdcb005965a5a972da05ddbc87a598f0ec64
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54927021"
---
# <a name="ienumdebugcustomattributesnext"></a>IEnumDebugCustomAttributes::Next
Özel özniteliklerin bir numaralandırma dizisinde belirtilen bir sayı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Next (   
   ULONG      celt,  
   CODE_PATH* rgelt,  
   ULONG*     pceltFetched  
);  
```  
  
```csharp  
int Next(  
   uint                        celt,   
   out IDebugCustomAttribute[] rgelt,   
   ref uint                    pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `celt`  
 [in] Alınacak öğelerin sayısı. Ayrıca en büyük boyutunu belirtir `rgelt` dizisi.  
  
 `rgelt`  
 [out] Bir dizi [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md) doldurulacak nesne.  
  
 `pceltFetched`  
 [out] Gerçekte döndürülen öğe sayısını döndürür `rgelt`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` istenen öğelerin sayısından daha az döndürülebilen; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)   
 [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)