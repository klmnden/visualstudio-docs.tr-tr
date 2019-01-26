---
title: IDebugSymbolSearchEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugSymbolSearchEvent2
helpviewer_keywords:
- IDebugSymbolSearchEvent2
ms.assetid: 9b946d55-ff85-44eb-b40a-efbf8282eafd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7af963afab74149da0c1c0bd6394e7de9df6cd36
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54931147"
---
# <a name="idebugsymbolsearchevent2"></a>IDebugSymbolSearchEvent2
Bu arabirim, hata ayıklama gerçekleştirilen modül için hata ayıklama sembolleri yüklendiğini göstermek için hata ayıklama altyapısı (DE) tarafından gönderilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugSymbolSearchEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE bir modülün sembolleri yüklenmiş olan bildirmek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](/cpp/atl/queryinterface) erişimi `IDebugEvent2` arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 KODU oluşturur ve bu olay bir modülün sembolleri yüklenmiş olan rapor nesnesine gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 `IDebugSymbolSearchEvent2` Arabirimi aşağıdaki yöntemi kullanıma sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetSymbolSearchInfo](../../../extensibility/debugger/reference/idebugsymbolsearchevent2-getsymbolsearchinfo.md)|Sembol Arama sonuçlarıyla ilgili bilgileri alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Semboller yüklenemedi olsa bile, bu olay gönderilir. Çağırma `IDebugSymbolSearchEvent2::GetSymbolSearchInfo` modülü gerçekten simgeleri olup olmadığını belirlemek için bu olay işleyicisi sağlar.  
  
 Visual Studio genellikle kullanır bu olay semboller yüklendi durumunu güncelleştirmek için **modülleri** penceresi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)