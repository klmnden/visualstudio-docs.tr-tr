---
title: IDebugDefaultPort2::GetServer | Microsoft Docs
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
- IDebugDefaultPort2::GetServer
helpviewer_keywords:
- IDebugDefaultPort2::GetServer
ms.assetid: cacb4b74-0f39-471c-af38-54b73f5b2868
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 4c91633a0d478c16e832fec7e73c92d5e7749346
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49892170"
---
# <a name="idebugdefaultport2getserver"></a>IDebugDefaultPort2::GetServer
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, bu bağlantı noktası sunucusuna bir arabirim alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetServer(  
   IDebugCoreServer3** ppServer  
);  
```  
  
```csharp  
int GetServer(  
   out IDebugCoreServer3 ppServer  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppServer`  
 [out] Döndürür bir nesneyi uygulama [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md) arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md) Visual Studio tarafından uygulanır ve bağlantı noktası üzerinde bulunduğu sunucu temsil eder.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)   
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)

