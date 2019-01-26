---
title: Kanca işlevlerini rapor | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- hooks, report
- _CrtDbgReport function
- debugger, report hook functions
- memory allocation, debug heap
- debugging [C++], hook functions
- _CrtSetReportHook function
- report hook functions
ms.assetid: 1854bca7-d7eb-4502-89bf-b1ee64cb50ef
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 18485d94aaedcb1f41c0ed747dc6af0be7f7e276
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54952880"
---
# <a name="report-hook-functions"></a>Kanca İşlevlerini Raporla
Bir rapor kanca işlevini kullanarak yüklü [_CrtSetReportHook](/cpp/c-runtime-library/reference/crtsetreporthook), her zaman çağrılır [_CrtDbgReport](/cpp/c-runtime-library/reference/crtdbgreport-crtdbgreportw) hata ayıklama raporunu oluşturur. Filtreleme raporların ayırmaları belirli türlerde odaklanmak, başka şeylerin yanında, kullanabilirsiniz. Bir rapor kanca işlevini aşağıdaki gibi bir prototipe sahip olmalıdır:  
  
```cpp
int YourReportHook(int nRptType, char *szMsg, int *retVal);  
```  
  
 Geçirdiğiniz işaretçiyi **_CrtSetReportHook** türünde **_CRT_REPORT_HOOK**CRTDBG içinde tanımlanan gibi. Y:  
  
```cpp
typedef int (__cdecl *_CRT_REPORT_HOOK)(int, char *, int *);  
```  
  
 Çalışma zamanı kitaplığı, kanca işlevini çağırdığında *nRptType* bağımsız değişken içeren rapor kategorisi (**_CRT_WARN**, **_CRT_ERROR**, veya **_CRT _ASSERT**), *szMsg* montajı rapor ileti dizeye bir işaretçi içerir ve *retVal* belirtir olup olmadığını `_CrtDbgReport` normal yürütmenin devam etmelidir rapor veya başlangıç hata ayıklayıcı oluşturduktan sonra. (A *retVal* sıfır değeri, yürütme devam eder, hata ayıklayıcı 1 değerini başlatır.)  
  
 Daha fazla raporlama olmadan gerekli olacak şekilde kanca söz konusu iletiyi tamamen işleyen, döndürme zorunluluğu **TRUE**. Döndürürse **FALSE**, `_CrtDbgReport` rapor normalde ileti olur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklama kanca işlevi yazma](../debugger/debug-hook-function-writing.md)   
 [crt_dbg2 örnek](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/crt/crt_dbg2)
