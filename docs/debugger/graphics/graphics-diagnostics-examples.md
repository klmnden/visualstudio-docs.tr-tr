---
title: Grafik tanılama örnekleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 45dd86b2-801e-4b07-a8c4-7bd25641d7f8
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 8419ea4f653d870802fd104da2824952b422ab6f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53867033"
---
# <a name="graphics-diagnostics-examples"></a>Grafik Tanılama Örnekleri
Bu örnekler kullanarak DirectX tabanlı uygulamalarda işleme sorunları hatalarını ayıklamak nasıl [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] grafik tanılama.  
  
## <a name="capturing-graphics-information"></a>Graf bilgilerini yakalama  
 Uygulamanızda işleme sorunlarını tanılamak için grafik Tanılama'yı kullanabilmeniz için önce çalıştığı sırada bir uygulamadan grafik bilgilerini yakalama gerekir. Grafik bilgilerini yerel olarak çalışan bir uygulamadan veya uzak bir bilgisayar veya başka bir cihaz üzerinde çalışan bir uygulamadan yakalanabilir. Bu izlenecek yollar nasıl el ile veya programlama yoluyla bir uygulamadan grafik bilgilerini yakalayabilir gösterilmektedir:  
  
-   [İzlenecek yol: Grafik bilgilerini yakalama](walkthrough-capturing-graphics-information.md)  
  
-   [İzlenecek yol: Grafik bilgilerini programla yakalama](walkthrough-capturing-graphics-information-programmatically.md)  
  
## <a name="use-graphics-diagnostics-with-an-arm-based-device"></a>ARM tabanlı bir cihazla grafik Tanılama'yı kullanma  
 Uzaktan hata ayıklamayı kullanarak ARM tabanlı bir cihaz üzerinde Direct3D uygulamanızın hatalarını ayıklamak için grafik tanılama kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Bir ARM cihazla grafik tanılama kullanmak](/visualstudio/debugger/graphics/graphics-diagnostics-examples).  
  
## <a name="playing-back-graphics-information"></a>Grafik bilgilerini kayıttan yürütme  
 Çalışan bir uygulamadan grafik bilgilerini yakalama sonra işleme sorunlarını tanılamak için yakalanan olayları oynatabilirsiniz. Kayıttan yürütme için geliştirme makinenizi kullanabilirsiniz veya bir uzak makine ya da bağlı olduğunuz cihaz kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Grafik tanılama kayıttan yürütme makinesini değiştirme](how-to-change-the-graphics-diagnostics-playback-machine.md).  
  
## <a name="debugging-missing-objects"></a>Eksik nesneleri hata ayıklama  
 Eksik bir nesne (veya nesneler) deneyimine grafik geliştiriciler en yaygın işleme sorunlarını biridir. Bu tür sorunlar, hataları birkaç farklı türde nesneyi görünüşe göre kaybolmasına neden olabilir çünkü tanı koymak güç olabilir. Eksik nesneleri tipik nedenleri yapılandırılmış cihaz durumu, nesnenin geometrisini veya yanlış yapılandırılmış grafik ardışık düzen dönüştürme sorunları olabilir.  
  
 Bu senaryolar, bir nesne neden eksik olduğunu belirlemek ve sorumlu kodu bulmak için grafik tanılama nasıl kullanabileceğinizi gösterir.  
  
-   [İzlenecek yol: Cihaz durumu nedeniyle nesnelerin eksikliği](walkthrough-missing-objects-due-to-device-state.md)  
  
-   [İzlenecek yol: Köşe gölgeleme nedeniyle nesnelerin eksikliği](walkthrough-missing-objects-due-to-vertex-shading.md)  
  
-   [İzlenecek yol: Yanlış yapılandırılmış ardışık düzen nedeniyle eksik nesneler](walkthrough-missing-objects-due-to-misconfigured-pipeline.md)  
  
## <a name="debugging-rendering-errors"></a>İşleme hatalarını ayıklama  
 Doğru görünümü olmaması bir nesne (veya nesneler) grafik geliştiriciler deneyimini başka bir yaygın bir sorundur. Bu tür sorunlar yanlış görünümünü ve bunun nedenini gelen çok belirgin değişebilir olduğundan tanı koymak güç olabilir — yanlış doku bağlama — çok çok hafif — gölgelendirici kodu veya gölgelendiricileri arasındaki etkileşim beklenmeyen bir hata. Bazı sorunların hatalarının bir bileşimiyle kaynaklanıyor olabilir.  
  
 Küçük gölgelendirici hata tarafından neden olmayan şekilde Zarif işleme sorunuyla aşağı izlemek için grafik tanılama nasıl kullanabileceğinizi gösteren bir senaryo aşağıda verilmiştir:  
  
-   [İzlenecek yol: Gölgeleme nedeniyle çıkan oluşturma hatalarını ayıklama](walkthrough-debugging-rendering-errors-due-to-shading.md)  
  
## <a name="debugging-compute-shaders"></a>Hesaplayıcı gölgelendiricilerde hata ayıklama  
 DirectCompute hesaplayıcı gölgelendiricisi hatalı sonuçlar üreten bir çekirdek hata ayıklamak için grafik tanılama kullanabilirsiniz. DirectCompute ile GPU işlem gücüne çok sayıda paralel veri öğeleri üzerinde hesaplamalar gerçekleştirmek için kullanabilirsiniz. Belirli tür sorunları, GPU kullanan birden çok kez daha iyi iyileştirilmiş CPU kod daha hızlı gerçekleştirebilirsiniz. Bununla birlikte, geleneksel hata ayıklayıcılar, GPU üzerinde çalışan kod algılayamaz. Bu türde bir kod hata ayıklama, çoğunlukla satıcıya özgü ve daha iyi Visual Studio ile tümleşebilen değil özel araçlar gerektirir. Bir aralık Gpu'lar, COMPUTE gölgelendirici hata ayıklaması daha tutarlı hale getirmek için grafik tanılama gönderme DirectCompute olayları yakalar; Direct3D işleme olaylarının yanı sıra — böylece sorunları compute gölgelendirici kodunuzda hata ayıklamak için alışık olduğunuz araçları kullanabilirsiniz.  
  
 Bir hesaplayıcı gölgelendiricisinde hata nedeniyle bir simülasyon sorunu çözmeye anlatan bir senaryo için bkz [izlenecek yol: Hesaplayıcı Gölgelendiricisinde hata ayıklamak için grafik tanılamayı kullanma](walkthrough-using-graphics-diagnostics-to-debug-a-compute-shader.md).