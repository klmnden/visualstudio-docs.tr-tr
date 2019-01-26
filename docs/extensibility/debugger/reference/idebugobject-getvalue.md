---
title: IDebugObject::GetValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugObject::GetValue
helpviewer_keywords:
- IDebugObject::GetValue method
ms.assetid: eec6051e-8ecb-49fa-bdd4-dd786f211692
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0e2c41cc81a27e46e74298d78ff9836ef74a8bff
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54941911"
---
# <a name="idebugobjectgetvalue"></a>IDebugObject::GetValue
Nesnenin değerini ardışık bir bayt dizisi olarak alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetValue(   
   BYTE* pValue,  
   UINT  nSize  
);  
```  
  
```csharp  
int GetValue(  
   ref byte[] pValue,   
   uint nSize  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pValue`  
 [out içinde] Nesnenin değerini temsil eden bir bayt serisi art arda oturum doldurulmuş bir dizi.  
  
 `nSize`  
 [in] Getirilecek bayt sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Toplam çağrı getirilen değeri bayt sayısını almak [GetSize](../../../extensibility/debugger/reference/idebugobject-getsize.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)