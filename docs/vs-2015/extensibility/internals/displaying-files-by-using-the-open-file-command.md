---
title: Dosya Aç komutunu kullanarak dosyaları görüntüleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- project types, supporting Open File command
- Open File command
- persistence, supporting Open File command
ms.assetid: 4fff0576-b2f3-4f17-9769-930f926f273c
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 96953d77e82dfcec79257da47845ece8281ec869
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60106104"
---
# <a name="displaying-files-by-using-the-open-file-command"></a>Dosya Aç Komutunu Kullanarak Dosyaları Görüntüleme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Aşağıdaki adımlar, IDE nasıl işlediğini açıklar **açık dosya** kullanılabilir olan komutunu **dosya** menüde [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. Adımları ayrıca nasıl projeleri bu komutu kaynaklanan çağrıları yanıt açıklar.  
  
 Kullanıcı tıkladığında **açık dosya** komutunu **dosya** menüsünde, bir dosyadan seçer **açık dosya** iletişim kutusunda aşağıdaki süreç gerçekleşir.  
  
1. Çalıştırılan Belge tablosu kullanarak IDE dosyanın zaten projede açık olup olmadığını belirler.  
  
    - Dosya açık değilse, IDE penceresi resurfaces.  
  
    - Dosya açık değilse, IDE çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.IsDocumentInProject%2A> her proje, proje dosyasını açabilirsiniz belirlemek için sorgulanamıyor.  
  
        > [!NOTE]
        >  Proje uygulamanızda <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.IsDocumentInProject%2A>, projenizi, dosyayı açar düzeyini gösteren bir öncelik değeri sağlayın. Öncelik değerleri sağlanan <xref:Microsoft.VisualStudio.Shell.Interop.VSDOCUMENTPRIORITY> sabit listesi.  
  
2. Her proje önemini gösteren bir öncelik düzeyi ile yanıt dosyasını açmak için bir proje olan üzerinde yerleştirir.  
  
3. IDE, proje dosyası açılır belirlemek için aşağıdaki ölçütleri kullanır:  
  
    - En yüksek öncelik (DP_Intrinsic) ile yanıtlar proje dosyasını açar. Bu önceliğine sahip birden fazla proje yanıt verirse, yanıt için ilk proje dosyasını açar.  
  
    - Hiçbir proje yanıtlar, en yüksek öncelikli (DP_Intrinsic), ancak aynı, daha düşük önceliğe sahip tüm projeleri yanıt etkin proje dosyasını açar. Hiçbir proje etkin olursa, yanıt için ilk proje dosyasını açar.  
  
    - Proje dosyası (DP_Unsupported) sahipliğini talep, çeşitli dosyalar projeleri dosyasını açar.  
  
         Çeşitli dosyalar projeleri örneği oluşturduysanız, proje her zaman DP_CanAddAsExternal değeri ile yanıt verir. Bu değer, proje dosyayı açabilmesini gösterir. Bu proje, başka bir projede olmayan açık dosyaları barındırmak için kullanılır. Bu projede öğelerin listesini kalıcı değil; Bu proje görülebilir **Çözüm Gezgini** yalnızca bir dosyayı açmaya kullanıldığında.  
  
         Çeşitli dosyalar projeleri dosyayı açabilmesini denenemeyeceğini belirtmiyorsa, proje örneği oluşturulmamış. Bu durumda, IDE çeşitli dosyalar projeleri örneği oluşturur ve dosyayı proje söyler.  
  
4. Proje dosyası açılır IDE belirler hemen sonra çağrılır <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.OpenItem%2A> proje yöntemi.  
  
5. Proje, projeye özgü Düzenleyici ya da bir standart düzenleyici kullanarak dosyayı açma seçeneğini ardından sahiptir. Daha fazla bilgi için [nasıl yapılır: Projeye özgü düzenleyicileri açma](../../extensibility/how-to-open-project-specific-editors.md) ve [nasıl yapılır: Standart düzenleyicileri açma](../../extensibility/how-to-open-standard-editors.md)sırasıyla.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komutu ile Aç'ı kullanarak dosyaları görüntüleme](../../extensibility/internals/displaying-files-by-using-the-open-with-command.md)   
 [Açma ve proje öğelerini kaydetme](../../extensibility/internals/opening-and-saving-project-items.md)   
 [Nasıl yapılır: Projeye özgü düzenleyicileri açma](../../extensibility/how-to-open-project-specific-editors.md)   
 [Nasıl yapılır: Open Standard Editors](../../extensibility/how-to-open-standard-editors.md)
