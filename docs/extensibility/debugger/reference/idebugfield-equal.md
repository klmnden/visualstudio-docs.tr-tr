---
title: IDebugField::Equal | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugField::Equal
helpviewer_keywords:
- IDebugField::Equal method
ms.assetid: 75369fe6-ddd3-497d-80d1-2488e6100e9f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7fdfc2abd407c586c949ade4e8085e282fb465a8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54984359"
---
# <a name="idebugfieldequal"></a>IDebugField::Equal
Bu yöntem, bu alan için eşitlik belirtilen alan ile karşılaştırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Equal(   
   IDebugField* pField  
);  
```  
  
```csharp  
int Equal(  
   IDebugField pField  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pField`  
 [in] Buna karşılaştırmak için alan.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Alanları aynıysa döndürür `S_OK`. Alanları farklı ise döndürür `S_FALSE.` Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)