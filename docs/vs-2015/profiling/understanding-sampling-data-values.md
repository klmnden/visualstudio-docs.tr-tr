---
title: Örnekleme veri değerlerini anlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method
- Profiling Tools, sampling
ms.assetid: fad540a8-24b6-4ff9-91ce-e67e9a58399d
caps.latest.revision: 27
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 91a4a50ecc745c0b56167d6a5dbb1932af7ed2bf
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68145421"
---
# <a name="understanding-sampling-data-values"></a>Örnekleme Veri Değerlerini Anlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

*Örnekleme* yöntemi profil oluşturma [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları Bilgisayar işlemcisi belirlenen aralıklarla keser ve işlev çağrı yığını toplar. A *çağrı yığını* işlemci üzerinde yürütülen işlevler hakkında bilgi depolayan dinamik bir yapıdır.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
  Profil Oluşturucu analiz işlemci hedef işlemde kodu yürüten olup olmadığını belirler. Hedef işlemde işlemci kod yürütülmüyor örnek atılır.  
  
  İşlemci hedef kodu yürütülüyorsa, profil oluşturucu çağrı yığınında her işlev için örnek sayısını artırır. Örneği alınmış tarihte, çağrı yığınında yalnızca bir işlev şu anda kod yürüttüğünü. Yığında diğer işlevler işlev çağrılarının döndürmek bunların alt öğeleri için bekleyen sıradüzeni içindeki içindedir.  
  
  Örnek olay, profil oluşturucu artışlar için *özel* örnek sayısı, yönergeler şu anda yürüten işlev. Özel bir örnek de toplamın bir parçası olduğundan (*kapsamlı*) örnekleri işlevinin etkin işlev kapsayıcı örnek sayısı da artar.  
  
  Profil Oluşturucu çağrı yığınında diğer tüm işlevlerin kapsamlı örnek sayısını artırır.  
  
## <a name="inclusive-samples"></a>Kapsamlı örnekler  
 Hedef işlevi yürütülmesi sırasında toplanan örneklerin toplam sayısı.  
  
 Bu işlev kodu doğrudan yürütülmesi sırasında toplanan örnekler ve hedef işlev tarafından çağrılmış işlevler alt yürütülmesi sırasında toplanan örnekler içerir.  
  
## <a name="exclusive-samples"></a>Dışlamalı örnekler  
 Doğrudan yönergeleri hedef işlevin yürütülmesi sırasında toplanan örnek sayısı.  
  
 Dışlamalı örnekler hedef işlev tarafından çağrılmış işlevler yürütülmesi sırasında toplanan örnekler dahil değildir.  
  
## <a name="inclusive-percent"></a>Kapsamlı yüzde  
 Bir işlev veya veri aralığı kapsamlı örnekler olan profil oluşturma, kapsamlı örnekler toplam sayısının yüzdesi.  
  
## <a name="exclusive-percent"></a>Özel yüzde  
 Dışlamalı örnek bir işlev veya veri aralığı olan profil oluşturma çalışması içinde dışlamalı örnekler toplam sayısının yüzdesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)   
 [Performans Araçları Verilerini Analiz Etme](../profiling/analyzing-performance-tools-data.md)
