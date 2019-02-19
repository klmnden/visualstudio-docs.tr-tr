---
title: Ayırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: d9d1b52c-7f28-467d-b1e0-512afc4e46c9
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1262e88055fceef0b2170c304c8ff646eea07205
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54793080"
---
# <a name="detach"></a>Ayır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe **ayırma** seçeneği keser profil oluşturucu belirtilen işlemleri veya tüm işlemlerden hiçbiri belirtilmezse. Profil oluşturma için örnekleme yöntemini kullanarak başlatılmış olması gerekir.  
  
 Profil oluşturma başlatıldı ile **başlatma** veya **iliştirme** seçenekleri bağlantısı ile **ayırma**. Profil Oluşturucu sonraki kullanarak reattched olabilir **iliştirme** komutları.  
  
 **Ayırma** profil oluşturma veri dosyasını kapatmak değil. Kullanım **kapatma** son profil oluşturma ve veri dosyasını kapatırsınız.  
  
> [!NOTE]
>  Varsa **Başlat** seçeneği ile belirtilen **Crosssession** seçeneğini çağrıları **VSPerfCmd /Attach** veya **VSPerfCmd/detach** gerekir Ayrıca belirtin **Crosssession**.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Detach[:PIDs|ProcessNames]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `PIDs|ProcessNames`  
 `PID` -Bir veya daha fazla işlem sayısal sistem tanımlayıcısını.  
  
 `ProcessNames` -işlem adı. Adlandırılmış işlemi birden çok örneğini çalıştırıyorsanız, sonuçlar tahmin edilemez.  
  
 Birden çok işlem virgülle ayırın.  
  
 Hiçbir işlem belirtilmezse, profil oluşturucu tüm profili oluşturulan işlemden ayrılır.  
  
## <a name="valid-options"></a>Geçerli seçenekler şunlardır:  
 Aşağıdaki **VSPerfCmd** seçenekleri ile birleştirilebilir **iliştirme** tek bir komut satırı seçeneği.  
  
 **Crosssession**  
 Oturumlarında oturum dışındaki uygulamaların profilini oluşturma etkinleştirir. Gerekli if **Başlat** seçeneği ile belirtilen **Crosssession** seçeneği.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, **ayırma** komutu, profil oluşturma askıya alır ve **kapatma** komutu, Profil Oluşturucu veri dosyasına kapatır.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
;REM Excercise the application  
VSPerfCmd.exe /Detach  
VSPerfCmd.exe /Shutdown  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
