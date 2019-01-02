---
title: C çalışma zamanı kitaplığını kullanmadan çalışma zamanı kullanarak denetler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.runtime
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- run-time errors, error checks
- CRT, run-time checks
- debugger, native run-time checks
- run-time errors, run-time checks
- run-time checks, /RTC option
- debugging [Visual Studio], run-time routines
ms.assetid: 30ed90f3-9323-4784-80a4-937449eb54f6
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1ae0b5831ef6007832438c4d589c4385711666dc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53921935"
---
# <a name="using-run-time-checks-without-the-c-run-time-library"></a>C Çalışma Zamanı Kitaplığını Kullanmadan Çalışma Zamanı Denetimlerini Kullanma
Programınızın C çalışma zamanı kitaplığı olmadan kullanıyorsa **/nodefaultlıb**ve çalışma zamanı denetimlerini kullanmak istiyorsanız, RunTmChk.lib ile bağlanmanız gerekir.  
  
 `_RTC_Initialize` programınızın çalışma zamanı denetimleri başlatır. C çalışma zamanı kitaplığı ile bağlamazsanız, programınızın çalışma zamanı hata denetimleri çağırmadan önce ile derlenmiş olup olmadığını görmek için denetlemelisiniz `_RTC_Initialize`gibi:  
  
```cpp
#ifdef __MSVC_RUNTIME_CHECKS  
    _RTC_Initialize();  
#endif  
```  
  
 C çalışma zamanı kitaplığı ile bağlamazsanız, çağrılan işlev ayrıca tanımlamalısınız `_CRT_RTC_INITW`. `_CRT_RTC_INITW` Kullanıcı tanımlı işlevinizi varsayılan hata raporlama işlevi, şu şekilde yükler:  
  
```cpp
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
  
 Varsayılan hata raporlama işlevi yükledikten sonra ek hata raporlama işlevleri ile yükleyebileceğiniz `_RTC_SetErrorFuncW`. Daha fazla bilgi için [_RTC_SetErrorFuncW](/cpp/c-runtime-library/reference/rtc-seterrorfuncw).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yerel çalışma zamanı denetimlerini kullanma](../debugger/how-to-use-native-run-time-checks.md)
