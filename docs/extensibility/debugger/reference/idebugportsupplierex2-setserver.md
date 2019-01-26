---
title: IDebugPortSupplierEx2::SetServer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugPortSupplierEx2::SetServer
ms.assetid: 0e8ef194-3a4f-4abf-8382-4607ab3005d1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: defc13ea9bc63bc1e2c5bdca229e58ec71fe25dc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54950030"
---
# <a name="idebugportsupplierex2setserver"></a>IDebugPortSupplierEx2::SetServer
Çekirdek sunucusu için bağlantı noktası sağlayıcısı ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetServer(  
   IDebugCoreServer2* pServer  
);  
```  
  
```csharp  
int SetServer(  
   IDebugCoreServer2 pServer  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pServer`  
 Bağlantı noktası sağlayıcısı için ayarlanacak Çekirdek sunucusu.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplierEx2](../../../extensibility/debugger/reference/idebugportsupplierex2.md)