---
title: 'İzlenecek yol: Grafik bilgilerini yakalama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 48f12f6e-57b4-48ec-a145-89fa71a42424
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 68ad8e09558aad1b6a4172acd0aa8b4749661854
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54930114"
---
# <a name="walkthrough-capturing-graphics-information"></a>İzlenecek yol: Grafik Bilgilerini Yakalama
Bu izlenecek yolda nasıl kullanılacağını gösterir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] el ile bir Direct3D uygulamadan grafik bilgilerini yakalamak için grafik tanılama.  
  
 Bu örneklerde bu görevler gösterilir:  
  
-   Grafik tanılama uygulamanıza takma  
  
-   Graf bilgilerini yakalama  
  
## <a name="capturing-graphics-information"></a>Graf bilgilerini yakalama  
 Grafik tanılama araçlarını kullanmak için öncelikle kullanır grafik bilgilerini yakalama olması. Yakalama özelliğini etkinleştirmek için kullanın **tanılamayı Başlat** başladığında uygulamanızı grafik tanılama yeteneklerinizi komutu.  
  
#### <a name="to-enable-the-capture-of-graphics-information-after-a-project-or-solution-is-loaded"></a>Bir proje veya çözüm sonra grafik bilgilerini yakalama etkinleştirmek için yüklenir  
  
1. İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], grafik bilgilerini yakalamak istediğiniz uygulama için bir proje veya çözüm dosya yükleyin.  
  
2. Grafik tanılama araç çubuğunda **tanılamayı Başlat**.  
  
#### <a name="to-enable-the-capture-of-graphics-information-without-loading-a-project-or-solution"></a>Bir proje veya çözüm yüklemeden grafik bilgilerini yakalamayı etkinleştirme  
  
1. Menü çubuğunda, **dosya**, **açık**, **proje/çözüm**. **Açık proje** iletişim kutusu görüntülenir.  
  
2. Yürütülebilir dosya, grafik bilgilerini yakalamak ve ardından istediğiniz uygulama için bir proje veya çözüm dosyası yerine belirtin **açık**.  
  
3. Menü çubuğunda, **hata ayıklama**, **grafik**, **tanılamayı Başlat**.  
  
   Uygulamayı başlatın ve işleme çerçeveler olduktan sonra grafik bilgilerini yakalayabilir.  
  
#### <a name="to-capture-graphics-information"></a>Grafik bilgilerini yakalamak için  
  
- Grafik tanılama araç çubuğunda **yakalama** düğmesi. ![Grafik yakalama düğmesinin simgesi](media/debuggingdirectxgraphics.png "DebuggingDirectXGraphics")  
  
   -veya-  
  
   Odak uygulamayla basın **Print Screen**.  
  
  Her zaman bir kare hakkında bilgi yakalama grafik tanılama Direct3D olayları ve ilişkili durumu kaydeder ve bu verileri bir grafik günlüğüne ekler. Yeni bir grafik günlüğü, her bir grafik Tanılama oturumu için oluşturulur. Grafik günlükleri hakkında daha fazla bilgi için bkz: [genel bakış](overview-of-visual-studio-graphics-diagnostics.md).  
  
## <a name="next-steps"></a>Sonraki Adımlar  
 Bu izlenecek yol, grafik bilgilerini elle yakalama gösterilmiştir. Sonraki adım olarak, bu seçenek göz önünde bulundurun:  
  
-   Grafik tanılama araçlarını kullanarak yakalanan grafik bilgileri analiz etmeyi öğrenin. Bkz: [genel bakış](overview-of-visual-studio-graphics-diagnostics.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Grafik Bilgilerini Yakalama](capturing-graphics-information.md)