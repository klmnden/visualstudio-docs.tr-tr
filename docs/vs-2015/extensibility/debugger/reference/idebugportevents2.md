---
title: IDebugPortEvents2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortEvents2
helpviewer_keywords:
- IDebugPortEvents2 interface
ms.assetid: 2c017094-3ba2-4067-83f9-147df1d96bce
caps.latest.revision: 19
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5e0f6455e6df8db88b1aae1a7b7f6965c0ee524b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784951"
---
# <a name="idebugportevents2"></a>IDebugPortEvents2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, işlem ve program oluşturma ve yok etme belirli bir bağlantı noktası üzerinde dinleyici (genellikle oturum hata ayıklama Yöneticisi [SDM] veya hata ayıklama altyapısı) bildirir. Bu bilgiler bağlantı noktası üzerinde çalışan programları ve işlemleri gerçek zamanlı bir görünümünü sunmak için kullanılabilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortEvents2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Visual Studio, genellikle program oluşturma ve yok etme hakkında bildirim almak için bu arabirimi uygular. Hata ayıklama altyapısı ayrıca bağlantı noktası gibi olayları dinlemek için bu arabirimi uygulayabilir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Tüm [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) arabirimleri için sorgulanabilir bir <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> arabirimi. Ardından <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer.FindConnectionPoint%2A> yöntemi `IDebugPortEvents2` çağrılma yeri <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> arabirimi almak için bir <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> arabirimi. Son olarak, <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint.Advise%2A> yönteminde <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> arabirimi aracılığıyla olayları göndermek için çağırılır [olay](../../../extensibility/debugger/reference/idebugportevents2-event.md) yöntemi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemini aşağıdaki tabloda gösterilmektedir `IDebugPortEvents2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Event](../../../extensibility/debugger/reference/idebugportevents2-event.md)|Oluşturma ve yok etme süreçleri ve bağlantı noktası programları açıklayan olaylar gönderir.|  
  
## <a name="remarks"></a>Açıklamalar  
 `IDebugPortEvents2` SDM tarafından ayıklanmakta olan bir işlem içinde çalıştırmak programlarda hata ayıklama için de kullanılır.  
  
 Bağlantı noktası olayları için SDM bu arabirim tarafından geçirilir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
