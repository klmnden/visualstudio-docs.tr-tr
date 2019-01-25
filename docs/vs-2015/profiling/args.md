---
title: Args | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 20c35949-1f29-4282-ac75-4e6c237d71bc
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 65759da4363891c713f906e6cb10f00443bcbceb
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782586"
---
# <a name="args"></a>Bağımsız Değişkenler
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe **Args** seçeneği belirtir hedef uygulamaya geçirilen bağımsız değişkenlerin bir listesi **başlatma** alt.  
  
 **Args** yalnızca ne zaman kullanılabilir **başlatma** da komut satırı üzerinde belirtilmiş. **Args** isteğe bağlı olduğunda **başlatma** belirtilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Launch:AppName /Args:Arguments [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `Arguments`  
 Hedef uygulamayı bağımsız değişken listesi **başlatma** komutu.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **Başlat:** `AppName`  
 Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte **Args** TestApp.exe için bağımsız değişkenleri geçirmek için seçeneği.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /Args:"123, 'Hello World'"  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
