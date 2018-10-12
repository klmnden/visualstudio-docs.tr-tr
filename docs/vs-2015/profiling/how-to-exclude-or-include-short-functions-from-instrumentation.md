---
title: 'Nasıl yapılır: kısa işlevleri izlemeden dahil veya hariç tutmak | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- profiling tools, instrument events
- profiling tools, include short functions
- profiling tools, exclude short functions
ms.assetid: eaeead79-aafe-4490-86ff-6ed4cad9c15f
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ffc2e09dda4d65cf467fe6cd1e5cc26a18bade19
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49285213"
---
# <a name="how-to-exclude-or-include-short-functions-from-instrumentation"></a>Nasıl yapılır: Kısa İşlevleri İzlemeden Hariç Tutma veya Dahil Etme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan olarak, profil oluşturma araçları hariç *küçük işlevlerin* İzleme'den. Küçük işlevlerin işlev çağrıları yapmayın kısa işlevlerdir. Bu küçük işlevler hariç için izleme yükü daha azdır sağlar ve bu nedenle izleme hızı geliştirildi. Küçük işlevlerin dışlama performans profil oluşturma veri (.vsp) dosyasının boyutu ve analiz için gerekli süreyi de azaltır. Küçük işlevlerin dışlanırsa, küçük işlevlerde geçen süre üst işlevlerini özel ve kapsamlı süre karşı sayar. Küçük işlevlerin dışlanan veya Araçları'nda, aşağıdaki yordamda açıklandığı gibi dahil.  
  
### <a name="to-exclude-or-include-short-functions-from-instrumentation"></a>Kısa işlevleri izlemeden hariç tutmak veya  
  
1.  İçinde **performans Gezgini**seçin **performans oturumu** ve ardından sağ tıklayıp **özellikleri**.  
  
     **Özellik sayfaları** iletişim kutusu görüntülenir.  
  
2.  İçinde **özellik sayfaları**, tıklayın **izleme** özellikleri.  
  
3.  Kısa işlevleri izlemeden hariç tutmak için seçin **kısa işlevleri izlemeden hariç**. Varsayılan ayar budur.  
  
     veya  
  
     Kısa işlevleri Araçları'nda dahil etmek için Temizle **kısa işlevleri izlemeden hariç**.  
  
4.  **Tamam**'ı tıklatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Veri toplama denetimi](../profiling/controlling-data-collection.md)   
 [Performans Oturumu Özellikleri](../profiling/performance-session-properties.md)



