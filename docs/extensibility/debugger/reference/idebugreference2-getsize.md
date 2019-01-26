---
title: IDebugReference2::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugReference2::GetSize
helpviewer_keywords:
- IDebugReference2::GetSize
ms.assetid: a404ddd9-d940-4513-97cd-f52b8ab6a560
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 089e898ed96d5b806a8ab4352b1d8a88316f5dc2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009644"
---
# <a name="idebugreference2getsize"></a>IDebugReference2::GetSize
Başvuru değeri bayt cinsinden boyutunu alır. Daha sonraki kullanımlar için ayrılmıştır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetSize (   
   DWORD* pdwSize  
);  
```  
  
```csharp  
int GetSize (   
   out uint pdwSize  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdwSize`  
 [out] Başvuru değeri bayt cinsinden boyutunu döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Her zaman döndürür `E_NOTIMPL`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)