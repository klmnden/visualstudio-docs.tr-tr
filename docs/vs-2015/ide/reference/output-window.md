---
title: Çıkış penceresi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vs.build.output
- vs.debug.output
- vs.output
helpviewer_keywords:
- Output window, about Output window
- Output window
- Toolbox, removing controls
ms.assetid: d8931d88-250e-4db4-963f-2c5b3e99b45f
caps.latest.revision: 35
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7173abd87a9e7345e7d7caee02d2bb333f507514
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65696067"
---
# <a name="output-window"></a>Çıktı Penceresi
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

**Çıkış** penceresi, tümleşik geliştirme ortamında (IDE) çeşitli özellikler için durum iletilerini görüntüleyebilirsiniz. Açmak için **çıkış** menü çubuğunda, pencere **görünüm/çıkış** (veya CTRL + ALT + O).  
  
> [!WARNING]
> Çıkış penceresi, Visual Studio Express sürümlerinde Görünüm menüsünde görünmüyor. Bu ortaya çıkarmak için kısayol tuşu kullanma CTRL + ALT + o  
  
## <a name="toolbar"></a>Araç Çubuğu  
 **Çıktıyı Göster**  
 Görüntülemek için bir veya daha fazla çıkış bölmeleri görüntüler. Birkaç bölmeleri bilgilerinin hangi Araçlar IDE içinde kullanılan bağlı olarak, kullanılabilir **çıkış** pencere iletilerini kullanıcıya teslim etmek için.  
  
 **Kodda ileti Bul**  
 Ekleme noktasını, Kod Düzenleyicisi'nde seçili derleme hatası içeren satıra taşır.  
  
 **Önceki iletiye Git**  
 Odak değişiklikleri **çıkış** penceresinde önceki derleme hatası ve ekleme noktasını Kod Düzenleyicisi'nde hata oluşturan içeren satıra taşır.  
  
 **Sonraki iletiye Git**  
 Odak değişiklikleri **çıkış** sonraki pencereyi derleme hatası ve ekleme noktasını Kod Düzenleyicisi'nde hata oluşturan içeren satıra taşır.  
  
 **Tümünü temizle**  
 Tüm metni temizler **çıkış** bölmesi.  
  
 **Sözcük kaydırmayı Aç/Kapat**  
 Sözcük kaydırma özelliğini açar ve kapatır **çıkış** bölmesi. Sözcük kaydırma etkin olduğunda, uzun girdileri görüntüleme alanının genişletir metin satırında görüntülenir.  
  
## <a name="output-pane"></a>Çıkış bölmesi  
 **Çıkış** bölmesinde seçili **çıktıyı Göster** liste belirtilen kaynak çıktı görüntüler.  
  
## <a name="routing-messages-to-the-output-window"></a>Yönlendirme iletilerini çıkış penceresine  
 Görüntülenecek **çıkış** içinde bir proje oluşturduğunuzda penceresi **genel, projeler ve çözümler, Seçenekler** iletişim kutusunda **derleme başladığında çıkış Göster penceresi**. Düzenleme için bir kod dosyası açıkken, ardından **sonraki iletiye Git** ve **önceki ileti** düğmelerini **çıkış** girişleri içinde seçmeküzerepenceresiaraççubuğu **Çıkış** bölmesi. Bunu yaparken, ekleme noktasını, seçilen sorunun oluştuğu kod satırına Kod Düzenleyicisi atlar.  
  
 Bazı IDE özellikleri ve içinde çağrılan komutlarda [komut penceresi](../../ide/reference/command-window.md) çıktılarını için teslim **çıkış** penceresi. Genellikle bir komut istemi penceresinde gösterilen çıkış .bat ve .com dosyaları gibi dış araçlarından yönlendirileceğini bir **çıkış** seçtiğinizde bölmesinde **çıktı penceresini kullan** seçeneğinde[Dış araçları yönetme](../../ide/managing-external-tools.md). İletileri diğer birçok türde görüntülenebilen **çıkış** bölmelerinde. Hedef veritabanında bir saklı yordamda Transact-SQL söz dizimi işaretlendiğinde, örneğin, sonuçları görüntülenir **çıkış** penceresi.  
  
 Kendi uygulamalarınızı çalışma zamanında tanılama iletileri yazmak için de programlayabileceğiniz bir **çıkış** bölmesi. Bunu yapmak için üyeleri kullanan <xref:System.Diagnostics.Debug> sınıfı veya <xref:System.Diagnostics.Trace> sınıfını <xref:System.Diagnostics> ad alanı .NET Framework sınıf kitaplığı. Üyeleri <xref:System.Diagnostics.Debug> çözüm veya projenin hata ayıklama yapılandırmaları oluşturduğunuzda sınıfı görünen çıkış; üyeleri <xref:System.Diagnostics.Trace> sınıfı görüntü çıktısı hata ayıklama veya yayın yapılandırmaları oluşturduğunuzda. Daha fazla bilgi için [çıkış penceresindeki tanılama iletileri](../../debugger/diagnostic-messages-in-the-output-window.md).  
  
 İçinde [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)], özel derleme adımları oluşturma ve derleme olayları, uyarıları ve hataları görüntülenir ve sayılı **çıkış** bölmesi. Çıkış bir satıra F1'e basarak uygun bir Yardım konusu görüntüleyebilirsiniz. Daha fazla bilgi için [özel derleme adımı veya derleme olayının çıktısını biçimlendirme](https://msdn.microsoft.com/library/92ad3e38-24d7-4b89-90e6-5a16f5f998da).  
  
## <a name="scrolling-behavior"></a>Kaydırma davranışını  
 Çıkış penceresinde autoscrolling kullanın ve ardından fareyi veya ok tuşlarını kullanarak gidin, autoscrolling durdurur. Autoscrolling sürdürmek için CTRL + END tuşlarına basın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Çıkış penceresindeki tanılama iletileri](../../debugger/diagnostic-messages-in-the-output-window.md)   
 [Nasıl yapılır: Çıkış penceresini denetleme](https://msdn.microsoft.com/library/91aebd15-8854-4a7a-9f7d-57376fb4e858)   
 [Derleme ve oluşturma](../../ide/compiling-and-building-in-visual-studio.md)   
 [Derleme yapılandırmalarını anlama](../../ide/understanding-build-configurations.md)   
 [Sınıf Kitaplığına Genel Bakış](https://msdn.microsoft.com/library/7e4c5921-955d-4b06-8709-101873acf157)
