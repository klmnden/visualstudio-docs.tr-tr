---
title: IDebugPendingBreakpoint2::Enable | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPendingBreakpoint2::Enable
helpviewer_keywords:
- IDebugPendingBreakpoint2::Enable method
- Enable method
ms.assetid: 09e32d05-464b-40a6-a41d-76f2759cf2cd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2f4da6362f195efe55ba38e3de02f644d40596c4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971955"
---
# <a name="idebugpendingbreakpoint2enable"></a>IDebugPendingBreakpoint2::Enable
Bekleyen kesme noktasının etkinleştirilen durumunu değiştirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Enable(   
   BOOL fEnable  
);  
```  
  
```csharp  
int Enable(   
   int fEnable  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fEnable`  
 [in] İçin sıfır olmayan ayarlayın (`TRUE`) bir bekleyen kesme noktasını etkinleştir veya sıfır (`FALSE`) devre dışı bırakmak için.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_BP_DELETED` kesme noktası silinmiş olması durumunda.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir bekleyen kesme noktasının etkin veya devre dışı bırakıldıysa bağlı tüm kesme noktalarını aynı duruma ayarlanır.  
  
 Kesme noktası zaten etkin veya devre dışı olsa bile bu yöntem, gerekli sayıda çağrılabilir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CPendingBreakpoint` gösteren nesne [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) arabirimi.  
  
```cpp  
HRESULT CPendingBreakpoint::Enable(BOOL fEnable)    
{    
   HRESULT hr;    
  
   // Verify that the pending breakpoint has not been deleted. If deleted,   
   // then return hr = E_BP_DELETED.    
   if (m_state.state != PBPS_DELETED)    
   {    
      // If the bound breakpoint member variable is valid, then enable or   
      // disable the bound breakpoint.    
      if (m_pBoundBP)    
      {    
         m_pBoundBP->Enable(fEnable);    
      }    
      // Set the PENDING_BP_STATE in the PENDING_BP_STATE_INFO structure   
      // to enabled or disabled depending on the passed BOOL condition.    
      m_state.state = fEnable ? PBPS_ENABLED : PBPS_DISABLED;    
      hr = S_OK;    
  
   }    
   else    
   {    
      hr = E_BP_DELETED;    
   }    
  
   return hr;    
}    
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)