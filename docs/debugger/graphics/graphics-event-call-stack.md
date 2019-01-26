---
title: Grafik olay Çağırma yığını | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.graphics.callstack
ms.assetid: 8a30168d-8b39-4de1-b094-c7356ba101a3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1c335c9360df30fc76579b8dd8e6513f61fc5196
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55037011"
---
# <a name="graphics-event-call-stack"></a>Grafik Olay Çağırma Yığını
Grafik olay çağrı yığını'nı Visual Studio grafik Çözümleyicisi sorunlu grafik olaylarını ve uygulamanızın kaynak kodu arasındaki ilişkiyi eşlemenize yardımcı olur.  
  
 Bu olay çağrı yığını penceresinde.  
  
 ![Önceki DrawIndexed olay çağrı yığını. ](media/gfx_diag_demo_graphics_event_call_stack_orientation.png "gfx_diag_demo_graphics_event_call_stack_orientation")  
  
## <a name="understanding-the-graphics-event-call-stack"></a>Grafik olay çağrı yığını anlama  
 Olay çağrı yığını, belirli bir Direct3D olaya yol açan akışını anlamak için kullanabilirsiniz. Seçili Direct3D olayın gerçekleştiği edildiğinde bulunduğu gibi geçerli iş parçacığının geçerli çağrı yığınını çalışan bir uygulamada görüntülemek yerine, çağrı yığınını görüntüler dışında Visual Studio çağrı yığını penceresini benzer. Olay çağrısı yığını, çevreleyen kod İnceleme seçili Direct3D olayın çağrı sitesini atlayabilirsiniz.  
  
 Bir sorun olay kaynaklandığı kod yolu belirlemek için olay çağrı yığını kullanarak olası sorun kaynaklarını çıkarmaya kod tabanının bilginizi kullanabilirsiniz veya Geleneksel kullanabilmesi için uygulamanızın kaynak kodunda kesme noktaları ekleyebilirsiniz. teknikleri, uygulama veya olay parametreleri durumunu işlemiyorsa olayın neden nasıl incelemek için hata ayıklama. Bu inceleme, yalnızca işleme sorunları bildirilen kaynak kodundaki sorunlarını bulmanıza yardımcı olabilir.  
  
### <a name="graphics-event-call-stack-information"></a>Grafik olay çağrı yığını bilgilerini  
 Olay Çağırma yığını öncesi çerçeve olayları veya kullanıcı tanımlı olayları desteklemez. Grafik olay çağrı yığını, tablo biçiminde görüntülenir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|Çağrı sitesini içeren işlev benzersiz olarak tanımlayan bir simge. Hata ayıklama sembolü işlev için kullanılabilir hale geldiğinde görüntülenir; Aksi halde, işlev uzaklık görüntülenir.|  
|**Dosya**|Kaynak kodu dosyanızı veya çağrı sitesini içeren kitaplık dosyasının dosya adı.|  
|**Konum**|Çağrı sitesini satır sayısı.|  
  
### <a name="links-to-graphics-objects"></a>Grafik nesneleri bağlantılar  
 Seçilen grafik olay anlamak için ilişkili Direct3D nesneleri hakkındaki bilgileri gerekebilir. **Grafik olay çağrı yığını** penceresi bu bilgilere bağlantılar sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: Köşe Gölgeleme Nedeniyle Eksik Nesneler](walkthrough-missing-objects-due-to-vertex-shading.md)