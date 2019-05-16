---
title: IDebugProcessEx2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProcessEx2
helpviewer_keywords:
- IDebugProcessEx2 interface
ms.assetid: 44e309ba-1d6f-499b-aa7e-9b34858a6d57
caps.latest.revision: 22
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d2b036bd68aca126675f26b9823d2c786a0ae652
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65675325"
---
# <a name="idebugprocessex2"></a>IDebugProcessEx2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

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
  
- SDM çağrıları [QueryInterface](https://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) üzerinde bir `IDebugProcess2` arabirimi bu arabirim elde edilir.  
  
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
