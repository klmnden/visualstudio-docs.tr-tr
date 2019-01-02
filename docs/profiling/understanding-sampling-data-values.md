---
title: Örnekleme veri değerlerini anlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method
- Profiling Tools, sampling
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d98a34abcd0e17f7b453ab3bd6e706665a9379bb
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53863478"
---
# <a name="understand-sampling-data-values"></a>Örnekleme veri değerlerini anlama

*Örnekleme* Bilgisayar işlemcisi belirlenen aralıklarla kesmeleri yöntemi Visual Studio profil oluşturma araçları, profil oluşturma ve işlev çağrı yığını toplar. A *çağrı yığını* işlemci üzerinde yürütülen işlevler hakkında bilgi depolayan dinamik bir yapıdır.

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

## <a name="see-also"></a>Ayrıca bkz.

[Nasıl yapılır: Koleksiyon metotları seçme](../profiling/how-to-choose-collection-methods.md)  
[Performans araçları verilerini analiz etme](../profiling/analyzing-performance-tools-data.md)