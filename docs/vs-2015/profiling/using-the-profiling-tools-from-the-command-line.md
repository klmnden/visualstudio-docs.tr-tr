---
title: Profil oluşturma kullanarak komut satırından araçları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- command line, performance tools
- command-line tools, performance tools
- profiling tools,command line
- tools, command-line
- command line, tools
ms.assetid: 6593fa82-181e-4009-a0ed-02aa24c2c063
caps.latest.revision: 40
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ebd0fbabb73d4c77d1d888b207882e7403f46aab
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63431613"
---
# <a name="using-the-profiling-tools-from-the-command-line"></a>Komut Satırından Profil Oluşturma Araçlarını Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Komut satırı araçlarını kullanabilirsiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profili uygulamalara komut isteminde ve toplu iş dosyaları kullanarak ve komut dosyası profil oluşturma otomatik hale getirmek için profil oluşturma araçları. Bir komut isteminde rapor dosyalarını da oluşturabilirsiniz. Basit bağımsız profil oluşturucuyu olmadığı bilgisayarlarda verileri toplamak için kullanabileceğiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] yüklü.  
  
> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Semboller konumunu ayarlayın:** Profil oluşturucu işlevleri ve parametre adlarını görüntülemek için profili oluşturulmuş ikili dosyalar için Sembol (.pdb) dosyalarını erişimi olmalıdır. Bu dosyalar, analiz görüntülemek istediğiniz uygulamaları ve Microsoft işletim sistemi için Sembol dosyaları içermelidir. Microsoft ikililer için doğru .pdb dosyalarına sahip olduğunuzdan emin olmak için genel Microsoft sembol Sunucusu'nu kullanabilirsiniz.|-   [Nasıl Yapılır: Komut Satırından Sembol Dosyası Konumlarını Belirtme](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md)|  
|**Uygulamanızın profilini:** Bir hedef uygulama profil oluşturma metodu uygulamanın türüne bağlı profili için kullandığınız seçenekleri ve komut satırı araçları ve hedef yönetilen veya yerel bir uygulama olup.|-   [Profil oluşturma yöntemlerini komut satırından kullanma](../profiling/using-profiling-methods-to-collect-performance-data-from-the-command-line.md)<br />-   [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)<br />-   [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)<br />-   [Profil oluşturma hizmetleri](../profiling/command-line-profiling-of-services.md)|  
|**.XML veya .csv raporları oluşturun:** Profil oluşturmayı komut isteminde, arabirimin görüntülenebilir veri dosyalarını oluşturur [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. .Xml veya virgülle ayrılmış değer (.csv) dosyaları verilerin VSPerfReport komut satırı aracını kullanarak da oluşturabilirsiniz.|-   [Komut satırından Profiler raporlar oluşturma](../profiling/creating-profiler-reports-from-the-command-line.md)<br />-   [VSPerfReport](../profiling/vsperfreport.md)|  
|**Visual Studio bulunmayan bilgisayarlarda kod profili:** Profil oluşturma araçları bağımsız profil oluşturucuyu sahip olmayan bilgisayarlarda uygulama verilerini toplamak için kullanabileceğiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] yüklü.|-   [Nasıl Yapılır: Bağımsız Profil Oluşturucuyu Yükleme](../profiling/how-to-install-the-stand-alone-profiler.md)|  
  
## <a name="reference"></a>Başvuru  
 [Komut Satırı Profil Oluşturma Araçları Başvurusu](../profiling/command-line-profiling-tools-reference.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Performans Gezgini](../profiling/performance-explorer.md)
