---
title: IDebugProperty2::GetParent | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProperty2::GetParent
helpviewer_keywords:
- IDebugProperty2::GetParent
ms.assetid: 58780469-fe25-4d84-9187-67940ca0767f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1db6acb0f60dac726717ebaccae0837e620dd9ce
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54991469"
---
# <a name="idebugproperty2getparent"></a>IDebugProperty2::GetParent
Bir özelliğin üst özelliği alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetParent (   
   IDebugProperty2** ppParent  
);  
```  
  
```csharp  
int GetParent (   
   out IDebugProperty2 ppParent  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppParent`  
 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) özelliğinin üst temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür. Döndürür `S_GETPARENT_NO_PARENT` üst öğe varsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)