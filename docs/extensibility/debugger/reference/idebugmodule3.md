---
title: IDebugModule3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugModule3
helpviewer_keywords:
- IDebugModule3 interface
ms.assetid: 44f8e96e-9c59-4ffc-9a08-9c908a0e4de7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bb40c3b0d6d08e3b4b995d2f39440775df292f9f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55013762"
---
# <a name="idebugmodule3"></a>IDebugModule3
Bu arabirim, simgeler ve JustMyCode durumları alternatif konumlar destekleyen bir modülü temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugModule3 : IDebugModule2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE) simgeleri alternatif konumlar desteklemek ve JustMyCode durumları ile çalışmak için bu arabirimi uygular (bkz [Visual Studio hata ayıklayıcısı sözlüğü](../../../extensibility/debugger/reference/visual-studio-debugger-glossary.md) "JustMyCode" açıklaması için).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı [Getsymbolsearchınfo](../../../extensibility/debugger/reference/idebugsymbolsearchevent2-getsymbolsearchinfo.md) bu arabirimi döndürür. DE gönderir [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md) arabirimini kullanarak oturum hata ayıklama Yöneticisi için (SDM) [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) yöntemi. Ayrıca, bir çağrı [QueryInterface](/cpp/atl/queryinterface) üzerinde bir [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) arabirimi bu arabirim döndürür.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)|Simgeleri ve her yolu arama sonuçları için arama yolları listesi döndürür.|  
|[LoadSymbols](../../../extensibility/debugger/reference/idebugmodule3-loadsymbols.md)|Yükler ve geçerli bir modüle ilişkin simgeleri başlatır.|  
|[IsUserCode](../../../extensibility/debugger/reference/idebugmodule3-isusercode.md)|Modül kullanıcı kodu temsil edip etmediğini belirten döndürür bayrak.|  
|[SetJustMyCodeState](../../../extensibility/debugger/reference/idebugmodule3-setjustmycodestate.md)|Modül kullanıcı kodu veya değerlendirilip değerlendirilmeyeceğini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Visual Studio, bu arabirimin tipik tüketicisidir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)   
 [IDebugSymbolSearchEvent2](../../../extensibility/debugger/reference/idebugsymbolsearchevent2.md)   
 [GetSymbolSearchInfo](../../../extensibility/debugger/reference/idebugsymbolsearchevent2-getsymbolsearchinfo.md)