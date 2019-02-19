---
title: WinCounter | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: ff319ffc-f249-4c3f-9eb2-06e392e3ae80
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9424eb099516761866ec459888ff830fcf56a28b
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54791570"
---
# <a name="wincounter"></a>WinCounter
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**WinCounter** seçeneği, farklı çalıştır profilinin sırasında belirlenen aralıklarla toplamak için bir Windows ya da uygulama performans sayacı belirtir. Windows ve uygulama performans sayaçları, profil oluşturma veri dosyasını işaretleri olarak listelenir. Ayrı seçeneklerinde toplamak için birden çok performans sayaçları belirtebilirsiniz.  
  
 Sayaçlar varsayılan olarak, toplanan her 500 milisaniye. Kullanım **AutoMark** seçeneği farklı bir koleksiyon aralığı belirtin.  
  
 Yalnızca bir **AutoMark** seçeneği kullanılır. Birden çok **AutoMark** seçenekler belirtilir, sonuncu kullanılır.  
  
 **WinCounter** seçeneği yalnızca kullanılabilir ile **Başlat** seçeneği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Start:Method /Wincounter:Path [/WinCounter:Path] [AutoMark:Milliseconds] [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `Path`  
 Windows performans sayacı PDH sayacı yol biçiminde.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **WinCounter** seçeneği yalnızca kullanılabilir ile **Başlat** seçeneği.  
  
 **Başlat:** `Method`  
 **Başlat** seçeneği belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır.  
  
## <a name="exclusive-options"></a>Dışlayan seçenekleri  
 **AutoMark** seçeneği yalnızca kullanılabilir ile **WinCounter** seçeneği.  
  
 **AutoMark:** `Milliseconds`  
 Windows performans sayacı verilerini toplama arasındaki milisaniye sayısını belirtir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte, 1000 milisaniye cinsinden zaman aralığı sırasında Tahsil edilecek Windows performans sayaçları iki belirtilir.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /WinCounter:"\Processor(0)\% Processor Time" /WinCounter:"\System\Context Switches/sec" /AutoMark:1000  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
