---
title: Sorunları araçları performans sorunlarını giderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: troubleshooting
ms.assetid: 0b61cdf7-75b7-4abd-aff2-7bd997717626
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 91ccf1637d6b8a1f612031c8d59deeef8e07efc7
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60077361"
---
# <a name="troubleshooting-performance-tools-issues"></a>Performans sorunlarını giderme araçları sorunları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Profil oluşturma Araçları'nı kullandığınızda aşağıdaki sorunlardan biriyle karşılaşabilirsiniz:  
  
- [Profil oluşturma araçları tarafından toplanan veri yok](#NoDataCollected)  
  
- [Performans görünümleri ve raporlar için işlev adlarını sayıları görüntüleme](#NoSymbols)  
  
## <a name="NoDataCollected"></a> Profil oluşturma araçları tarafından toplanan veri yok  
 Bir uygulamanın profilini sonra profil oluşturma veri (.vsp) dosyası oluşturulmaz ve çıktı penceresinde ya da komut penceresinde aşağıdaki uyarıyı alırsınız:  
  
 PRF0025: Hiçbir veri toplanamadı.  
  
 Bu sorunu çeşitli sorunları neden olabilir:  
  
- Örnekleme veya .NET bellek yöntemi kullanarak profili oluşturulmuş bir işlem uygulama işi yapar işlem haline gelen bir alt işlemi başlatır. Örneğin, bazı uygulamalar, bir Windows uygulaması veya bir komut satırı uygulaması olarak başlatılmış olup olmadığını belirlemek için komut satırını okur. Bir Windows uygulaması istendi, özgün işlem bir Windows uygulaması olarak yapılandırılmış yeni bir işlem başlatır ve ardından özgün işlem çıkar. Profil oluşturma araçları otomatik olarak alt işlemleri için veri toplama için hiçbir veri toplanır.  
  
     Bu durumda profil oluşturma verilerini toplamak için profil oluşturucu uygulamaya Profil Oluşturucu ile başlatma yerine alt işlem ekleme. Daha fazla bilgi için [nasıl yapılır: Ekleme ve ayırma performans araçlarını çalışan işlemlere](../profiling/how-to-attach-and-detach-performance-tools-to-running-processes.md) ve [(VSPerfCmd) ekleme](../profiling/attach.md)  
  
## <a name="NoSymbols"></a> Performans görünümleri ve raporlar için işlev adlarını sayıları görüntüleme  
 Bir uygulamanın profilini sonra raporları ve görünümleri işlev adları yerine numaraları görürsünüz.  
  
 Bu sorun, kaynak kod bilgisi, bu işlev adları ve satır numaralarını derlenmiş dosyasına eşleşen sembol bilgilerini içeren .pdb dosyaları erişememe profil oluşturma araçları bir analiz motoru kaynaklanır. Uygulama dosyası oluşturulduğunda varsayılan olarak, derleyici .pdb dosyasını oluşturur. .Pdb dosyasının yerel dizin başvurusu derlenmiş uygulama depolanır. Analiz altyapısı, .pdb dosyasını başvurulan dizinini ve ardından şu anda uygulama dosyası içeren dosyayı arar. .Pdb dosyası bulunamazsa, bir analiz motoru işlevi uzaklıkları yerine işlev adlarını kullanır.  
  
 İki yoldan biriyle sorunu düzeltebilirsiniz:  
  
- .Pdb dosyaları bulun ve uygulama dosyaları aynı dizine koyun.  
  
- Sembol bilgilerini profil oluşturma veri (.vsp) dosyasına ekleyin. Daha fazla bilgi için [performans veri dosyalarıyla kaydetme sembol bilgilerini](../profiling/saving-symbol-information-with-performance-data-files.md).  
  
> [!NOTE]
>  Analiz altyapısı, .pdb dosyasını derlenmiş uygulama dosyası aynı sürümde olmasını gerektirir. Önceki veya sonraki bir derleme uygulama dosyasının .pdb dosyasından çalışmaz.
