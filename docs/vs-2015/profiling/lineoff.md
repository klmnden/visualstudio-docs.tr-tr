---
title: Lıneoff | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 76082063-20ef-47ae-ad64-81b43b654865
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fbe8a715c5bb179c5293dd666f1879c07068d8b2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54800283"
---
# <a name="lineoff"></a>LineOff
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Örnekleme profili oluşturma yöntemi kullanırken, varsayılan olarak, profil oluşturucu kaynak kodu satır numarasını ve satır numarası uzaklık veri toplar. VSPerfCmd **Lıneoff** seçeneği devre dışı bırakır satır numarası veri koleksiyonunu VSPerfCmd uygulamayı başlatmak için kullanıldığında. Profil oluşturma verilerinin işleve toplandığı zaman düzey **Lıneoff** belirtilir.  
  
 Kullanabileceğiniz **Lıneoff** yalnızca **başlatma** seçeneği, ve yalnızca zaman profil oluşturucu örnekleme için kullanarak başlatıldı **Başlat**:**örnek** seçeneği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Launch:AppName /LineOff [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 Hiçbiri  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **Lıneoff** seçeneği yalnızca içeren bir komut satırında kullanılabilir **başlatma** seçeneği.  
  
 **Başlat:** `AppName`  
 Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.  
  
## <a name="example"></a>Örnek  
 Bu örnek, uygulama ve profil oluşturucuyu başlatır ve satır düzeyi örnekleme devre dışı bırakır.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /LineOff  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
