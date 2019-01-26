---
title: IDebugProcess2::GetServer | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess2::GetServer
helpviewer_keywords:
- IDebugProcess2::GetServer
ms.assetid: 8f73c530-cceb-4f1f-8c63-1cc0ccd4a310
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 855f7f4035c8711fabac21d83831b8847f25b44b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54934445"
---
# <a name="idebugprocess2getserver"></a>IDebugProcess2::GetServer
Bu işlem çalıştıran sunucunun alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetServer(   
   IDebugCoreServer2** ppServer  
);  
```  
  
```csharp  
int GetServer(   
   out IDebugCoreServer2 ppServer  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppServer`  
 [out] Döndürür bir [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) bu işlemin çalıştığı sunucu temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Birden fazla sunucu tek bir makinede çalışıyor olabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)