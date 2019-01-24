---
title: GC (VSPerfCmd) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 7c81e88b-a748-4cf5-a7a1-3429608e1b54
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2bdb28f74dd305dc497521e95d38e00192c21c54
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54769070"
---
# <a name="gc-vsperfcmd"></a>GC (VSPerfCmd)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**GC** seçenek, .NET Framework bellek ayırma ve nesne yaşam verilerinin koleksiyonunu etkinleştirir. **GC** seçeneği, yalnızca örnekleme profili oluşturma yöntemi ve yalnızca ile kullanılabilir **başlatma** seçeneği.  
  
 Kullanırken **GC** seçeneğini VSPerfClrEnv **/sampleon** komut gerekli değildir.  
  
 Parametre belirtilmezse veya **ayırma** parametresi belirtildiğinde, yalnızca .NET Framework bellek ayırma verileri toplanır. Varsa **ömrü** parametresi belirtildiğinde, hem .NET Framework bellek ayırma hem de .NET Framework nesne yaşam verisi toplanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
  
```  
VSPerfCmd.exe /Launch:TestApp.exe /gc  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
