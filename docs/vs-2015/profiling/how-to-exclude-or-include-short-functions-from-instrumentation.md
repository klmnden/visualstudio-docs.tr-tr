---
title: 'Nasıl yapılır: Hariç tutma veya dahil kısa işlevleri izlemeden | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- profiling tools, instrument events
- profiling tools, include short functions
- profiling tools, exclude short functions
ms.assetid: eaeead79-aafe-4490-86ff-6ed4cad9c15f
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d37984b6535e353053ba6ee71090797e4ce119d3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801667"
---
# <a name="how-to-exclude-or-include-short-functions-from-instrumentation"></a>Nasıl yapılır: Hariç tutma veya kısa işlevleri izlemeden içerir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan olarak, profil oluşturma araçları hariç *küçük işlevlerin* İzleme'den. Küçük işlevlerin işlev çağrıları yapmayın kısa işlevlerdir. Bu küçük işlevler hariç için izleme yükü daha azdır sağlar ve bu nedenle izleme hızı geliştirildi. Küçük işlevlerin dışlama performans profil oluşturma veri (.vsp) dosyasının boyutu ve analiz için gerekli süreyi de azaltır. Küçük işlevlerin dışlanırsa, küçük işlevlerde geçen süre üst işlevlerini özel ve kapsamlı süre karşı sayar. Küçük işlevlerin dışlanan veya Araçları'nda, aşağıdaki yordamda açıklandığı gibi dahil.  
  
### <a name="to-exclude-or-include-short-functions-from-instrumentation"></a>Kısa işlevleri izlemeden hariç tutmak veya  
  
1.  İçinde **performans Gezgini**seçin **performans oturumu** ve ardından sağ tıklayıp **özellikleri**.  
  
     **Özellik sayfaları** iletişim kutusu görüntülenir.  
  
2.  İçinde **özellik sayfaları**, tıklayın **izleme** özellikleri.  
  
3.  Kısa işlevleri izlemeden hariç tutmak için seçin **kısa işlevleri izlemeden hariç**. Varsayılan ayar budur.  
  
     -veya-  
  
     Kısa işlevleri Araçları'nda dahil etmek için Temizle **kısa işlevleri izlemeden hariç**.  
  
4.  **Tamam**'ı tıklatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Veri toplama denetimi](../profiling/controlling-data-collection.md)   
 [Performans Oturumu Özellikleri](../profiling/performance-session-properties.md)
