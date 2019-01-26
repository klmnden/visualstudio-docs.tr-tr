---
title: IDebugPortSupplier2::GetPortSupplierName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPortSupplier2::GetPortSupplierName
helpviewer_keywords:
- IDebugPortSupplier2::GetPortSupplierName
ms.assetid: e4c368ab-640d-4b5b-9f74-810dc9364d8f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3d092cc049a65ba4f232c9aefd00536a78115b5b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55022410"
---
# <a name="idebugportsupplier2getportsuppliername"></a>IDebugPortSupplier2::GetPortSupplierName
Bağlantı sağlayıcı adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetPortSupplierName(   
   BSTR* pbstrName  
);  
```  
  
```csharp  
int GetPortSupplierName(   
   out string pbstrName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrName`  
 [out] Bağlantı noktası sağlayıcısı adını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)