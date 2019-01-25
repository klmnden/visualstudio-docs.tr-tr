---
title: DEBUG_REASON | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- DEBUG_REASON
helpviewer_keywords:
- DEBUG_REASON enumeration
ms.assetid: ad2ee898-8648-4671-9078-d32873862346
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 95a537c703d4afd68bb291205e0c7da8d9b8fc59
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799865"
---
# <a name="debugreason"></a>DEBUG_REASON
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama için işlem neden başlatıldı belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_DEBUG_REASON {  
   DEBUG_REASON_ERROR         = 0,  
   DEBUG_REASON_USER_LAUNCHED = 1,  
   DEBUG_REASON_USER_ATTACHED = 2,  
   DEBUG_REASON_AUTO_ATTACHED = 3,  
   DEBUG_REASON_CAUSALITY     = 4  
};  
typedef DWORD DEBUG_REASON;  
```  
  
```csharp  
public enum enum_DEBUG_REASON {  
   DEBUG_REASON_ERROR         = 0,  
   DEBUG_REASON_USER_LAUNCHED = 1,  
   DEBUG_REASON_USER_ATTACHED = 2,  
   DEBUG_REASON_AUTO_ATTACHED = 3,  
   DEBUG_REASON_CAUSALITY     = 4  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 DEBUG_REASON_ERROR  
 Belirli olmayan bir hata oluştu (yok, diğer uygun neden olduğunda bu bir varsayılan koşul olarak kullanılır).  
  
 DEBUG_REASON_USER_LAUNCHED  
 İşlem, kullanıcının isteğiyle başlatıldı.  
  
 DEBUG_REASON_USER_ATTACHED  
 Zaten çalışan işlemi kullanıcı tarafından eklendi.  
  
 DEBUG_REASON_AUTO_ATTACHED  
 Başlatıldığında işlemi otomatik olarak depolamaya bağlanmıştır.  
  
 DEBUG_REASON_CAUSALITY  
 İşlem şu nedenle başlatıldı bir *Just-ın-Time* (JIT) hata ayıklama olay.  
  
## <a name="remarks"></a>Açıklamalar  
 Öğesinden döndürülen [GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md)
