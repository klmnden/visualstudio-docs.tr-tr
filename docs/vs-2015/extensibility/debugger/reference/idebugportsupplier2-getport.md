---
title: IDebugPortSupplier2::GetPort | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugPortSupplier2::GetPort
helpviewer_keywords:
- IDebugPortSupplier2::GetPort
ms.assetid: d55d5055-7386-4037-bf22-4c3e434a99ca
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0346707f87d6cf7847b42f76ab4ba2b9704f36a9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49951190"
---
# <a name="idebugportsupplier2getport"></a>IDebugPortSupplier2::GetPort
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir bağlantı noktasına bağlantı noktası sağlayıcısı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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

