---
title: "Nasıl yapılır: Tek başına Profiler'ı yükleme | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- performance tools, installing stand-alone profiler
- profiling tools, stand-alone profiler
ms.assetid: cae81c95-83cd-4ab6-8a98-84ef977a2f6d
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5923bc99906cf4bcad8ea92ad74a30470fb41a1c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432726"
---
# <a name="how-to-install-the-stand-alone-profiler"></a>Nasıl yapılır: Tek başına Profiler'ı yükleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] bir komut satırı tabanlı yüklemeden çalıştırabilirsiniz bağımsız profil oluşturucuyu sağlar [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] IDE. Bir bilgisayar yok ya da yüklü bir geliştirme ortamı olamaz bu durum oluşur. Örneğin, bir üretim Web sunucusunda bir geliştirme ortamı yüklememelidir.  
  
> [!NOTE]
> ASP.NET Web sitesi için performans verilerini toplamak için bağımsız profil oluşturucuyu kullanırken [VSPerfASPNetCmd](../profiling/vsperfaspnetcmd.md) Çizgi aracı üzerinden önerilir [VSPerfCmd](../profiling/vsperfcmd.md) aracı.  
  
### <a name="to-install-the-stand-alone-profiler"></a>Bağımsız profil oluşturucuyu yükleme  
  
1. Bağımsız Profil yükleyicisini (vs_profiler.exe) bulmak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] yükleme medyasında dizine \Standalone Profiler yolu içerir ve çalıştırın.  
  
2. Vsintr.exe ve msdis150.dll yollarını sistem yoluna ekleyin.  
  
    > [!NOTE]
    > Varsayılan yüklemede [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], vsinstr.exe ve msdis150.dll \Program Files\Visual Studio 10\Team Araçlar\Performans araçları içinde bulunur.  
  
3. Komut isteminde **Vsınstr**.  
  
    > [!NOTE]
    > Vsinstr.exe yönelik kullanım bilgilerini gösterilirse, her şeyin doğru şekilde ayarlanır. Vsinstr.exe belirten bir hata göreceğiniz ya da bağımlılıklarından biri bulunamadı, cihazınızdaki yollar 2. adımda açıklandığı gibi doğru şekilde ayarlanmış olduğundan emin olun.  
  
4. Sembol sunucusu ayarlamak, **_NT_SYMBOL_PATH** değişkenini **symsrv\*symsrv.dll\*c:\localcache\*http://msdl.microsoft.com/download/symbols**  
  
5. Sistem ortam değişkenlerini kullanarak sembol sunucunuz ayarladıktan sonra komut satırından profil oluşturucu Araçlar yeni bir komut isteminde çalıştırın. Bu, etkili olması yeni ortam değişkenlerini tanır. Komut İstemi penceresinde aşağıdaki komutu yazın:  
  
     **COMSPEC % Başlat**  
  
    > [!NOTE]
    > Sembol sunucusu paketi ayarlama konusunda ayrıntılı yönergeler için bkz: [nasıl yapılır: Başvuru Windows sembol bilgileri](../profiling/how-to-reference-windows-symbol-information.md).  
  
6. Kullanım [VSPerfReport](../profiling/vsperfreport.md) aracı profil oluşturma veri (.vsp) dosyasına, semboller serileştirmek için. Kullanım **VSPerfReport userrulesdirectory packsymbols** anahtarlar. Veri dosyasına eklenmiş semboller yoksa _NT_SYMBOL_PATH ortam değişken kümesi olduğunu emin olun.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komut satırından profil oluşturma](../profiling/using-the-profiling-tools-from-the-command-line.md)   
 [İzlenecek yol: Komut satırı kullanarak örnekleme profili oluşturma](../profiling/walkthrough-command-line-profiling-using-sampling.md)   
 [İzlenecek yol: Komut satırı araçları kullanarak profil oluşturma](../profiling/walkthrough-command-line-profiling-using-instrumentation.md)   
 [Nasıl yapılır: Başvuru Windows sembol bilgileri](../profiling/how-to-reference-windows-symbol-information.md)   
 [VSPerfReport](../profiling/vsperfreport.md)
