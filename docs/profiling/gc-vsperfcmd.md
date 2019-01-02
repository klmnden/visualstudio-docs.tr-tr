---
title: GC (VSPerfCmd) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 7c81e88b-a748-4cf5-a7a1-3429608e1b54
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f15cf7c5991187431c06a01c67c7105f48dc28de
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53913223"
---
# <a name="gc-vsperfcmd"></a>GC (VSPerfCmd)
**GC** seçenek, .NET Framework bellek ayırma ve nesne yaşam verilerinin koleksiyonunu etkinleştirir. **GC** seçeneği, yalnızca örnekleme profili oluşturma yöntemi ve yalnızca ile kullanılabilir **başlatma** seçeneği.  
  
 Kullanırken **GC** seçeneğini VSPerfClrEnv **/sampleon** komut gerekli değildir.  
  
 Parametre belirtilmezse veya **ayırma** parametresi belirtildiğinde, yalnızca .NET Framework bellek ayırma verileri toplanır. Varsa **ömrü** parametresi belirtildiğinde, hem .NET Framework bellek ayırma hem de .NET Framework nesne yaşam verisi toplanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
VSPerfCmd.exe /Launch:AppName /GC[:{Allocation|Lifetime}] [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 **ayırma**  
 Varsayılan. .NET Framework bellek ayırma verileri toplar.  
  
 **Ömür**  
 Hem .NET Framework bellek ayırma verisini hem de .NET Framework nesne yaşam süresi verisi toplar.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **GC** seçeneği yalnızca kullanılabilir ile **başlatma** seçeneği.  
  
 **Başlat:** `AppName`  
 Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir uygulama başlatır ve .NET Framework bellek ayırma verileri toplar.  
  
```cmd  
VSPerfCmd.exe /Launch:TestApp.exe /gc  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil hizmetler](../profiling/command-line-profiling-of-services.md)