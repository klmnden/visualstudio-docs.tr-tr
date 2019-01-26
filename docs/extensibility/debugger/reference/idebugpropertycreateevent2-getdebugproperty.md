---
title: IDebugPropertyCreateEvent2::GetDebugProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPropertyCreateEvent2::GetDebugProperty
helpviewer_keywords:
- IDebugPropertyCreateEvent2::GetDebugProperty
ms.assetid: d7e43183-444c-4417-af19-82e28229f83a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c38ccf4adcef59454e6d65730034099777a2c549
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999411"
---
# <a name="idebugpropertycreateevent2getdebugproperty"></a>IDebugPropertyCreateEvent2::GetDebugProperty
Yeni özelliği alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetDebugProperty (   
   IDebugProperty2** ppProperty  
);  
```  
  
```csharp  
int GetDebugProperty (   
   out IDebugProperty2 ppProperty  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppProperty`  
 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) yeni özellik temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPropertyCreateEvent2](../../../extensibility/debugger/reference/idebugpropertycreateevent2.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)