---
title: IEEDataStorage::GetData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEEDataStorage::GetData
helpviewer_keywords:
- IEEDataStorage::GetData
ms.assetid: 4d384039-73d4-40b4-ace6-a2474c546397
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 26a77547ba16c6cfafde0d1629a4fef570aaef9c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54959583"
---
# <a name="ieedatastoragegetdata"></a>IEEDataStorage::GetData
Nesneden belirtilen bayt sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetData(  
   ULONG  dataSize,  
   ULONG* sizeGotten,  
   BYTE*  data  
);  
```  
  
```csharp  
int GetData(  
   uint     dataSize,  
   out uint sizeGotten,  
   byte[]   data  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dataSize`  
 [in] Alınacak bayt sayısı ( `data` dizi gerekir tutmak en az bu bayt sayısı).  
  
 `sizeGotten`  
 [out] Gerçekte alınan bayt sayısını döndürür.  
  
 `data`  
 [out içinde] İstenen veriler ile doldurulacak dizisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Önerilen bu yöntemin bayt alma işleminde atlamayı mümkün olduğundan tüm veri baytı yerel bir diziye almak için kullanılır. Bu durumda, parametre `dataSize` değeri olarak döndürülmelidir [GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)