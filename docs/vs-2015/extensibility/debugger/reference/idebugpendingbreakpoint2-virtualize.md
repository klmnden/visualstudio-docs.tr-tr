---
title: IDebugPendingBreakpoint2::Virtualize | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPendingBreakpoint2::Virtualize
helpviewer_keywords:
- Virtualize method
- IDebugPendingBreakpoint2::Virtualize method
ms.assetid: 58c8e9a5-4494-47c2-bddb-56f628da6a2d
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: caf4277afc63d403cc3d02c4d79b9e5f2b1b8d26
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799471"
---
# <a name="idebugpendingbreakpoint2virtualize"></a>IDebugPendingBreakpoint2::Virtualize
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu sanallaştırılmış bekleyen kesme noktasının durumunu değiştirir. Bir bekleyen kesme noktasının sanallaştırılmış, hata ayıklama altyapısı, yeni kodu programa yükleyen her zaman bu bağlama dener.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Virtualize(   
   BOOL fVirtualize  
);  
```  
  
```cpp#  
int Virtualize(   
   int fVirtualize  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fVirtualize`  
 [in] İçin sıfır olmayan ayarlayın (`TRUE`) bekleyen kesme noktasının sanallaştırmak için ya da sıfıra (`FALSE`) sanallaştırma açmak için.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_BP_DELETED` kesme noktası silinmiş olması durumunda.  
  
## <a name="remarks"></a>Açıklamalar  
 Kod her yüklendiğinde, sanallaştırılmış bir kesme noktası bağlıdır.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CPendingBreakpoint` gösteren nesne [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) arabirimi.  
  
```cpp#  
HRESULT CPendingBreakpoint::Virtualize(BOOL fVirtualize)    
{    
   HRESULT hr;    
  
   // Verify that the pending breakpoint has not been deleted. If deleted,   
   // then return hr = E_BP_DELETED.    
   if (m_state.state != PBPS_DELETED)    
   {    
      if (fVirtualize)    
      {    
         // Set the PBPSF_VIRTUALIZED flag in the PENDING_BP_STATE_FLAGS   
         // structure.    
         SetFlag(m_state.flags, PBPSF_VIRTUALIZED);    
      }    
      else    
      {    
         // Clear the PBPSF_VIRTUALIZED flag in the PENDING_BP_STATE_FLAGS   
         // structure.    
         ClearFlag(m_state.flags, PBPSF_VIRTUALIZED);    
      }    
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
