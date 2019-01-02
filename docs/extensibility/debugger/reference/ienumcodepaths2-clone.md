---
title: IEnumCodePaths2::Clone | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumCodePaths2::Clone
helpviewer_keywords:
- IEnumCodePaths2::Clone
ms.assetid: 9d5c6bc6-7e72-4f1b-801c-7192458f3ba8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f8dd02f49b7865bf92cce2f6cd5e48fdf8992b27
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53863754"
---
# <a name="ienumcodepaths2clone"></a>IEnumCodePaths2::Clone
Bir kopyasını ayrı bir nesne olarak geçerli bir sabit listesi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Clone(  
   IEnumCodePaths2** ppEnum  
);  
```  
  
```csharp  
int Clone(  
   out IEnumCodePaths2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Bu numaralandırma ayrı bir nesne gibi bir kopyasını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Numaralandırma kopyasını bu yöntemin çağrıldığı zaman orijinal ile aynı duruma sahiptir. Ancak, kopyanın ve orijinalin durumları ayrıdır ve ayrı ayrı değiştirilebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md)