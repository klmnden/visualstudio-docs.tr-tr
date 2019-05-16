---
title: IDebugSymbolSearchEvent2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugSymbolSearchEvent2
helpviewer_keywords:
- IDebugSymbolSearchEvent2
ms.assetid: 9b946d55-ff85-44eb-b40a-efbf8282eafd
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: fe6eda784ddfa393ee123a7aab1498fc2e5a15b5
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694619"
---
# <a name="idebugsymbolsearchevent2"></a>IDebugSymbolSearchEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, hata ayıklama gerçekleştirilen modül için hata ayıklama sembolleri yüklendiğini göstermek için hata ayıklama altyapısı (DE) tarafından gönderilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugSymbolSearchEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE bir modülün sembolleri yüklenmiş olan bildirmek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde. SDM kullanan [QueryInterface](https://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) erişimi `IDebugEvent2` arabirimi.  
  
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
