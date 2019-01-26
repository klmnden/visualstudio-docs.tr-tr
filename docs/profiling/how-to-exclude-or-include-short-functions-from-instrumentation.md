---
title: 'Nasıl yapılır: Hariç tutma veya dahil kısa işlevleri izlemeden | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools, instrument events
- profiling tools, include short functions
- profiling tools, exclude short functions
ms.assetid: eaeead79-aafe-4490-86ff-6ed4cad9c15f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 46edc453e16fec43028876d7d590c88651229994
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54965529"
---
# <a name="how-to-exclude-or-include-short-functions-from-instrumentation"></a>Nasıl yapılır: Kısa işlevleri izlemeden hariç tutma veya izlemeye dahil etme
Varsayılan olarak, profil oluşturma araçları hariç *küçük işlevlerin* İzleme'den. Küçük işlevlerin işlev çağrıları yapmayın kısa işlevlerdir. Bu küçük işlevler hariç için izleme yükü daha azdır sağlar ve bu nedenle izleme hızı geliştirildi. Küçük işlevlerin dışlama ayrıca profil oluşturma veri dosyasından performans azaltır (. *Vsp*) boyutunu ve analiz için gerekli olduğu süre. Küçük işlevlerin dışlanırsa, küçük işlevlerde geçen süre üst işlevlerini özel ve kapsamlı süre karşı sayar. Küçük işlevlerin dışlanan veya Araçları'nda, aşağıdaki yordamda açıklandığı gibi dahil.  
  
### <a name="to-exclude-or-include-short-functions-from-instrumentation"></a>Kısa işlevleri izlemeden hariç tutmak veya  
  
1.  İçinde **performans Gezgini**seçin **performans oturumu** ve ardından sağ tıklayıp **özellikleri**.  
  
     **Özellik sayfaları** iletişim kutusu görüntülenir.  
  
2.  İçinde **özellik sayfaları**, tıklayın **izleme** özellikleri.  
  
3.  Kısa işlevleri izlemeden hariç tutmak için seçin **kısa işlevleri izlemeden hariç**. Varsayılan ayar budur.  
  
     -veya-  
  
     Kısa işlevleri Araçları'nda dahil etmek için Temizle **kısa işlevleri izlemeden hariç**.  
  
4.  **Tamam**'ı tıklatın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Veri toplamayı denetleme](../profiling/controlling-data-collection.md)   
 [Performans oturumu özellikleri](../profiling/performance-session-properties.md)