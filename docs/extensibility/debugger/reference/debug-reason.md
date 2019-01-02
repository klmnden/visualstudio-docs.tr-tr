---
title: DEBUG_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DEBUG_REASON
helpviewer_keywords:
- DEBUG_REASON enumeration
ms.assetid: ad2ee898-8648-4671-9078-d32873862346
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 5842b79e6dd38ed99a7a255b4164762b1dd1b68b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53867356"
---
# <a name="debugreason"></a>DEBUG_REASON
Hata ayıklama için işlem neden başlatıldı belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
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