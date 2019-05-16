---
title: IDebugBreakEvent2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugBreakEvent2
helpviewer_keywords:
- IDebugBreakEvent2 interface
ms.assetid: 57dfdbc2-4e68-4dbf-9579-006cd6fb1c62
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 98e8c1b1669b3fdd1f442c6987e4e9d2b9fc4835
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65675375"
---
# <a name="idebugbreakevent2"></a>IDebugBreakEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, oturum hata ayıklama Yöneticisi (SDM) zaman uyumsuz bir sonu başarıyla tamamlandığını bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugBreakEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 DE kullanıcı sonu bir programda desteklemek için bu arabirimi uygular. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde (SDM kullanan [QueryInterface](https://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) erişimi `IDebugEvent2` arabirimi).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 SDM çağrıları [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md) zaman kullanıcı istedi Duraklatılacak ayıklanan programa. Program başarıyla duraklatıldı DE gönderir `IDebugBreakEvent2` olay. Bu olay ile gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bir kullanıcının seçim yapabileceği **tümünü Kes** komutunu **hata ayıklama** sonsuz bir döngüye çalışan bir programı ayırmak için menü. SDM çağırarak durdurmak için program söyler [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md). DE gönderir `IDebugBreakEvent2` program son ne zaman durdurur.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
