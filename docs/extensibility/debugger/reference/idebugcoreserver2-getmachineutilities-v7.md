---
title: IDebugCoreServer2::GetMachineUtilities_V7 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCoreServer2::GetMachineUtilities_V7
helpviewer_keywords:
- IDebugCoreServer2::GetMachineUtilities_V7
ms.assetid: 64c1f08f-853b-4498-9810-29791581ef2f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 977c7157ade60afe57b3564934319a34d140d81c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55027665"
---
# <a name="idebugcoreserver2getmachineutilitiesv7"></a>IDebugCoreServer2::GetMachineUtilities_V7
Bu yöntem, bir sunucu için makine yardımcı programları alır.  
  
> [!NOTE]
>  Bu yöntem artık kullanılmıyor: kullanmayın ([!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] her zaman döndürür `E_NOTIMPL` bu yöntemi çağrılırsa). Bu, geçmiş nedenlerle korunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetMachineUtilities_V7(  
   IDebugMDMUtil2_V7** ppUtil  
);  
```  
  
```csharp  
int GetMachineUtilities_V7(  
   out IDebugMDMUtil2_V7 ppUtil  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppUtil`  
 [out] Döndürür bir `IDebugMDMUtil2_V7` makine yardımcı programları bilgilerini temsil eden arabirim.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Her zaman döndürür `E_NOTIMPL`, belirten yöntem uygulanmadı.  
  
## <a name="remarks"></a>Açıklamalar  
 [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] her zaman döndürür `E_NOTIMPL` varsa, bu yöntem çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)