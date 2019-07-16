---
title: IDebugEngine3 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugEngine3
helpviewer_keywords:
- IDebugEngine3 interface
ms.assetid: 8bdf4bb7-3b5d-4991-8981-772d4f6bb656
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 1e43da0b05062c6c7b1c4d3cfe771ff0b93f83a9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68195789"
---
# <a name="idebugengine3"></a>IDebugEngine3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir veya daha fazla modülü hata ayıklama denetleyen bir tek hata ayıklama altyapısı (DE) temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugEngine3 : IDebugEngine2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 (Simge destekliyorsa) Bu arabirim JustMyCode durumunu etkinleştirmek için özel bir DE tarafından uygulanır. Simgeler ve JustMyCode destekliyorsa, bu arabirim tarafından DE uygulanmalıdır.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim, oturum hata ayıklama Yöneticisi (SDM) sembolleri konumlar için kullanıcı seçeneklerini geçirilecek tarafından çağrılır. Ayrıca, örneği oluşturulduğunda altyapısının GUID ayarlamak için çağrılır (Bu GUID altyapısı kayıt zamanı ölçümleri temel alır). SDM JustMyCode durumunu ayarlamak ve belirli bir duruma hata ayıklayıcı tarafından bilinen tüm özel durumları ayarlamak için bu arabirimi de çağırır.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Devralınan yöntemleri yanı sıra [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md), `IDebugEngine3` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)|Yolu veya yolları DE aramak için hata ayıklama için kullanacağı ayarlar.|  
|[LoadSymbols](../../../extensibility/debugger/reference/idebugengine3-loadsymbols.md)|Semboller yüklendi henüz uygulanmamış tüm modüller için sembolleri yükler.|  
|[SetJustMyCodeState](../../../extensibility/debugger/reference/idebugengine3-setjustmycodestate.md)|JustMyCode bilgilerini DE belirtir.|  
|[SetEngineGuid](../../../extensibility/debugger/reference/idebugengine3-setengineguid.md)|Ölçümleri DE GUID ayarlar.|  
|[SetAllExceptions](../../../extensibility/debugger/reference/idebugengine3-setallexceptions.md)|Belirtilen bir durum şu anda bekleyen tüm özel durumları ayarlayın.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
