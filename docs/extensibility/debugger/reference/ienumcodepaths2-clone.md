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
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b8fd1422b787fc8322e66e362b629092a1bb2cca
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006802"
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