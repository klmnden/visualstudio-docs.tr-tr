---
title: C çalışma zamanı kitaplığını kullanmadan çalışma zamanı kullanarak denetler | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.runtime
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- run-time errors, error checks
- CRT, run-time checks
- debugger, native run-time checks
- run-time errors, run-time checks
- run-time checks, /RTC option
- debugging [Visual Studio], run-time routines
ms.assetid: 30ed90f3-9323-4784-80a4-937449eb54f6
caps.latest.revision: 20
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 7f5d9c56cfde6e87c0f9bd92289597e77bfea875
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754147"
---
# <a name="using-run-time-checks-without-the-c-run-time-library"></a>C Çalışma Zamanı Kitaplığını Kullanmadan Çalışma Zamanı Denetimlerini Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Programınızın C çalışma zamanı kitaplığı olmadan kullanıyorsa **/nodefaultlıb**ve çalışma zamanı denetimlerini kullanmak istiyorsanız, RunTmChk.lib ile bağlanmanız gerekir.  
  
 `_RTC_Initialize` programınızın çalışma zamanı denetimleri başlatır. C çalışma zamanı kitaplığı ile bağlamazsanız, programınızın çalışma zamanı hata denetimleri çağırmadan önce ile derlenmiş olup olmadığını görmek için denetlemelisiniz `_RTC_Initialize`gibi:  
  
```  
#ifdef __MSVC_RUNTIME_CHECKS  
    _RTC_Initialize();  
#endif  
```  
  
 C çalışma zamanı kitaplığı ile bağlamazsanız, çağrılan işlev ayrıca tanımlamalısınız `_CRT_RTC_INITW`. `_CRT_RTC_INITW` Kullanıcı tanımlı işlevinizi varsayılan hata raporlama işlevi, şu şekilde yükler:  
  
```  
// C version:  
_RTC_error_fnW __cdecl _CRT_RTC_INITW(  
        void *res0, void **res1, int res2, int res3, int res4)  
{  
    // set the error handler.  
    return &MyErrorFunc;   
}  
  
// C++ version:  
extern "C" _RTC_error_fnW __cdecl _CRT_RTC_INITW(  
       void *res0, void **res1, int res2, int res3, int res4)  
{  
    // set the error handler:  
    return &MyErrorFunc;  
}  
```  
  
 Varsayılan hata raporlama işlevi yükledikten sonra ek hata raporlama işlevleri ile yükleyebileceğiniz `_RTC_SetErrorFuncW`. Daha fazla bilgi için [_RTC_SetErrorFuncW](http://msdn.microsoft.com/library/b3e0d71f-1bd3-4c37-9ede-2f638eb3c81a).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yerel Çalışma Zamanı Denetimlerini Kullanma](../debugger/how-to-use-native-run-time-checks.md)
