---
title: IDebugPortSupplier2::GetPort | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPortSupplier2::GetPort
helpviewer_keywords:
- IDebugPortSupplier2::GetPort
ms.assetid: d55d5055-7386-4037-bf22-4c3e434a99ca
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 9672ead8b774761d5655acc86878103664f8662f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53841466"
---
# <a name="idebugportsupplier2getport"></a>IDebugPortSupplier2::GetPort
Bir bağlantı noktasına bağlantı noktası sağlayıcısı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetPort(   
   REFGUID       guidPort,  
   IDebugPort2** ppPort  
);  
```  
  
```csharp  
int GetPort(   
   ref Guid        guidPort,  
   out IDebugPort2 ppPort  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidPort`  
 [in] Bağlantı noktasının genel benzersiz tanıtıcısı (GUID).  
  
 `ppPort`  
 [out] Döndürür bir [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) bağlantı noktasını temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_PORTSUPPLIER_NO_PORT` verilen tanıtıcı ile hiçbir bağlantı noktası zaten varsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)