---
title: IDebugMemoryContext2::Subtract | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugMemoryContext2::Subtract
helpviewer_keywords:
- Subtract method
- IDebugMemoryContext2::Subtract method
ms.assetid: 63df14c7-8d7e-47c1-afa7-5a1ab5d8eaba
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 53f919cb0c70d93c9888eb979846bc9b228c2e18
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55035360"
---
# <a name="idebugmemorycontext2subtract"></a>IDebugMemoryContext2::Subtract
Belirtilen değer geçerli bağlamdan çıkarır ve yeni bir bağlam döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Subtract(   
   UINT64                 dwCount,  
   IDebugMemoryContext2** ppMemCxt  
);  
```  
  
```csharp  
int Subtract(  
   ulong                    dwCount,   
   out IDebugMemoryContext2 ppMemCxt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwCount`  
 [in] Düşürmek için bellek bayt sayısı.  
  
 `ppMemCxt`  
 [out] Yeni bir [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir bellek bağlamı bir adresi olduğundan bir değeri bir adresinden çıkararak yeni bir bağlam arabirimi gerektiren yeni bir adres üretir.  
  
 Bu bağlamla ilişkilendirilen bellek alanını elde edilen adresi dışında olsa bile, bu yöntem her zaman yeni bir bağlam üretmesi gerekir. Yeni bağlam için ayrılan bellek yok ise veya tek özel durumu olan `ppMemCxt` (Bu bir hatadır) null bir değerdir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)