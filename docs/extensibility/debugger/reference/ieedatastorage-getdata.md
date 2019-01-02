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
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8ed1788804fea7d10734de339d7b5a91d9cd168b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53936977"
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