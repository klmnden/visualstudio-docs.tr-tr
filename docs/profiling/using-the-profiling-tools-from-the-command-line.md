---
title: Profil oluşturma kullanarak komut satırından araçları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- command line, performance tools
- command-line tools, performance tools
- profiling tools,command line
- tools, command-line
- command line, tools
ms.assetid: 6593fa82-181e-4009-a0ed-02aa24c2c063
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 049e1163f54dfcdfe2338faa59ae8c37c3114fa7
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63422048"
---
# <a name="use-the-profiling-tools-from-the-command-line"></a>Komut satırından profil oluşturma araçlarını kullanma
Komut satırı araçlarını kullanabilirsiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profili uygulamalara komut isteminde ve toplu iş dosyaları kullanarak ve komut dosyası profil oluşturma otomatik hale getirmek için profil oluşturma araçları. Bir komut isteminde rapor dosyalarını da oluşturabilirsiniz. Basit bağımsız profil oluşturucuyu olmadığı bilgisayarlarda verileri toplamak için kullanabileceğiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] yüklü.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

## <a name="common-tasks"></a>Ortak görevler

| Görev | İlgili içerik |
| - | - |
| **Semboller konumunu ayarlayın:** İşlevler ve parametre adlarını görüntülemek için profil oluşturucu sembol erişiminiz olması gerekir (. *pdb*) profili oluşturulan ikili dosyaları. Bu dosyalar, analiz görüntülemek istediğiniz uygulamaları ve Microsoft işletim sistemi için Sembol dosyaları içermelidir. Doğru olduğundan emin olmak için genel Microsoft sembol Sunucusu'nu kullanabilirsiniz. *pdb* Microsoft ikili dosyaları. | -   [Nasıl Yapılır: Sembol dosyası konumlarını komut satırından belirtme](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md) |
| **Uygulamanızın profilini:** Bir hedef uygulama profil oluşturma metodu uygulamanın türüne bağlı profili için kullandığınız seçenekleri ve komut satırı araçları ve hedef yönetilen veya yerel bir uygulama olup. | -   [Komut satırından profil oluşturma yöntemlerini kullanma](../profiling/using-profiling-methods-to-collect-performance-data-from-the-command-line.md)<br />-   [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)<br />-   [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)<br />-   [Profil hizmetler](../profiling/command-line-profiling-of-services.md) |
| **.XML veya .csv raporları oluşturun:** Profil oluşturmayı komut isteminde, arabirimin görüntülenebilir veri dosyalarını oluşturur [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Da oluşturabilirsiniz. *xml* veya virgülle ayrılmış değer (. *CSV*) VSPerfReport komut satırı aracını kullanarak veri dosyaları. | -   [Komut satırından profil oluşturucu raporlar oluşturma](../profiling/creating-profiler-reports-from-the-command-line.md)<br />-   [VSPerfReport](../profiling/vsperfreport.md) |
| **Visual Studio bulunmayan bilgisayarlarda kod profili:** Profil oluşturma araçları bağımsız profil oluşturucuyu sahip olmayan bilgisayarlarda uygulama verilerini toplamak için kullanabileceğiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] yüklü. | -   [Nasıl Yapılır: Bağımsız profil oluşturucuyu yükleme](../profiling/how-to-install-the-stand-alone-profiler.md) |

## <a name="reference"></a>Başvuru
- [Komut satırı profil araçları başvurusu](../profiling/command-line-profiling-tools-reference.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Performans Gezgini](../profiling/performance-explorer.md)