---
title: IDebugPortEx2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortEx2
helpviewer_keywords:
- IDebugPortEx2 interface
ms.assetid: 144724d0-38ee-4c9b-87ca-8a504371182b
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: bb866c5cb968a4f03c718f04193026ac5308f7d4
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65681130"
---
# <a name="idebugportex2"></a>IDebugPortEx2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, programlar ve bağlantı noktasında çalışan işlemler yöneticisi (SDM) denetiminde hata ayıklama oturumu sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortEx2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 SDM çağrıları [QueryInterface](https://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) üzerinde `IDebugPort2` arabirimi bu arabirim elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortEx2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[LaunchSuspended](../../../extensibility/debugger/reference/idebugportex2-launchsuspended.md)|Bir yürütülebilir dosya başlatır.|  
|[ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)|Bir işlemin yürütülmesi devam eder.|  
|[CanTerminateProcess](../../../extensibility/debugger/reference/idebugportex2-canterminateprocess.md)|Bir işlem sonlandırılabilir olup olmadığını belirler.|  
|[TerminateProcess](../../../extensibility/debugger/reference/idebugportex2-terminateprocess.md)|Bir işlemi sonlandırır.|  
|[GetPortProcessId](../../../extensibility/debugger/reference/idebugportex2-getportprocessid.md)|Bağlantı işlem Kimliğini alır.|  
|[GetProgram](../../../extensibility/debugger/reference/idebugportex2-getprogram.md)|Bir program düğümle ilişkili bir program alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, SDM ve özel bağlantı noktası sağlayıcısı arasında normalde özeldir.  
  
 İsterseniz, hata ayıklama altyapısı (DE) Bu arabirim için bakabilirsiniz [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) arabirimi geçirilen [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md) ve [LaunchSuspended](../../../extensibility/debugger/reference/idebugportex2-launchsuspended.md) programını başlatmak için. Ancak, bu bir gereklilik olmadığı ve ne olursa olsun, istek programını başlatmak için yapması gereken bir DE yapabilirsiniz.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: portpriv.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
