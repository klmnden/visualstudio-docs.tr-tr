---
title: IDebugProcessEx2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcessEx2
helpviewer_keywords:
- IDebugProcessEx2 interface
ms.assetid: 44e309ba-1d6f-499b-aa7e-9b34858a6d57
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 05e4218e18772e581af1651c354c717002fee19d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54996031"
---
# <a name="idebugprocessex2"></a>IDebugProcessEx2
Bu arabirim, hata ayıklama Yöneticisi (SDM) bildirmek için ekleme veya işlemden ayırmak Process işlem oturum sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProcessEx2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı aynı nesne üzerinde bu arabirimi uygulayan [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) için arabirim:  
  
- Oturumlarının bir işleme bağlı destek izleme  
  
- Destek otomatik iliştirme arasında birden çok hata ayıklama altyapısı  
  
  Seçerse bu özel bağlantı noktası sağlayıcısı bu arabirim uygulayabilir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
  
-   SDM çağrıları [QueryInterface](/cpp/atl/queryinterface) üzerinde bir `IDebugProcess2` arabirimi bu arabirim elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProcessEx2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Attach](../../../extensibility/debugger/reference/idebugprocessex2-attach.md)|İşlem, bir oturum işlemi artık hata ayıklıyor bildirir.|  
|[Detach](../../../extensibility/debugger/reference/idebugprocessex2-detach.md)|İşlem, bir oturum işlemi artık hata ayıklıyor bildirir.|  
|[AddImplicitProgramNodes](../../../extensibility/debugger/reference/idebugprocessex2-addimplicitprogramnodes.md)|Program düğümleri için hata ayıklama altyapısının bir listesini ekler.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, işlem SDM arasında özeldir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Portpriv.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)