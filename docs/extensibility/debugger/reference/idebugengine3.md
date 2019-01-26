---
title: IDebugEngine3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEngine3
helpviewer_keywords:
- IDebugEngine3 interface
ms.assetid: 8bdf4bb7-3b5d-4991-8981-772d4f6bb656
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0f89452582677334f75c330ff00af58b95e928c2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992353"
---
# <a name="idebugengine3"></a>IDebugEngine3
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