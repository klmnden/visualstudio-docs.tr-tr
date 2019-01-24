---
title: IDebugCoreServer2::GetMachineUtilities_V7 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugCoreServer2::GetMachineUtilities_V7
helpviewer_keywords:
- IDebugCoreServer2::GetMachineUtilities_V7
ms.assetid: 64c1f08f-853b-4498-9810-29791581ef2f
caps.latest.revision: 18
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c6d615a24e9c6608713699904724a62d14569ee4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753609"
---
# <a name="idebugcoreserver2getmachineutilitiesv7"></a>IDebugCoreServer2::GetMachineUtilities_V7
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, bir sunucu için makine yardımcı programları alır.  
  
> [!NOTE]
>  Bu yöntem artık kullanılmıyor: kullanmayın ([!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] her zaman döndürür `E_NOTIMPL` bu yöntemi çağrılırsa). Bu, geçmiş nedenlerle korunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
 [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] her zaman döndürür `E_NOTIMPL` varsa, bu yöntem çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
