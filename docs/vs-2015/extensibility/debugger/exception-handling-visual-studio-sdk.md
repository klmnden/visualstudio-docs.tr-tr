---
title: Özel durum işleme (Visual Studio SDK) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], exception handling
ms.assetid: 7279dc16-db14-482c-86b8-7b3da5a581d2
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 38e646f032a12de48bbfb55b089462c7f8a4dd26
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094846"
---
# <a name="exception-handling-visual-studio-sdk"></a>Özel Durum İşleme (Visual Studio SDK)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Aşağıdaki özel durumlar oluşturulduğunda oluşan işlemini açıklar.  
  
## <a name="exception-handling-process"></a>Özel durum işleme işlemi  
  
1. Öncelikle bir özel durum oluşturulur, ancak hata ayıklanan programa içinde özel durum işleyici tarafından işlenen önce hata ayıklama altyapısı (DE) gönderir. bir [IDebugExceptionEvent2](../../extensibility/debugger/reference/idebugexceptionevent2.md) durdurma olay olarak oturum hata ayıklama Yöneticisi (SDM). `IDebugExceptionEvent2` Kullanıcı üzerinde ilk fırsat özel durum bildirimleri durdurmak istiyor (hata ayıklama paketi özel durumlar iletişim kutusunda belirtilen) özel durum ayarlarını belirtin. yalnızca gönderilir.  
  
2. SDM çağrıları [IDebugExceptionEvent2::GetException](../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) özel durum özelliği alınamıyor.  
  
3. Hata ayıklama paketi çağrıları [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) kullanıcının seçeneklerini belirlemek için.  
  
4. Hata ayıklama paketi ilk fırsat özel durum iletişim kutusunu açarak özel durumu işlemek nasıl kullanıcıya sorar.  
  
5. SDM kullanıcı devam etmek seçerse, çağıran [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md).  
  
    - Yöntem S_OK döndürür, çağıran [IDebugExceptionEvent2::PassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-passtodebuggee.md).  
  
         -veya-  
  
         Yöntem S_FALSE, program döndürüyorsa ayıklanan özel durumu işlemek için ikinci bir şans verilir.  
  
6. Hata ayıklanan programa için ikinci şans özel durum işleyici yok ise DE gönderir. bir `IDebugExceptionEvent2` SDM için **EVENT_SYNC_STOP**.  
  
7. Hata ayıklama paketi ilk fırsat özel durum iletişim kutusunu açarak özel durumu işlemek nasıl kullanıcıya sorar.  
  
8. Hata ayıklama paketi çağrıları [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) kullanıcının seçeneklerini belirlemek için.  
  
9. Hata ayıklama paketi ikinci şans özel durum iletişim kutusunu açarak özel durumu işlemek nasıl kullanıcıya sorar.  
  
10. Yöntem S_OK döndürür, çağıran `IDebugExceptionEvent2::PassToDebuggee`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)
