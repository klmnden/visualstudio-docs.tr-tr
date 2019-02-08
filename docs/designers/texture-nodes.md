---
title: Doku Düğümleri
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: b7df5ef3-dd4f-4964-9d96-34e0e180515e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 73f5bfe71866422cd3717c2a29f1eeb48d15cc76
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55911019"
---
# <a name="texture-nodes"></a>Doku düğümleri

Gölgelendirici Tasarımcısı'nda doku düğümleri çeşitli doku türleri ve geometri, örnek ve oluşturmak veya doku koordinatları dönüştürebilirsiniz. Dokular, renk ve ayrıntı nesneler üzerinde ışık sağlar.

## <a name="texture-node-reference"></a>Doku düğümü başvurusu

|Düğüm|Ayrıntılar|Özellikler|
|----------|-------------|----------------|
|**Küp harita örneği**|Belirtilen koordinatlarda bir küp haritasından bir renk örneği alır.<br /><br /> Bir küp, yansıma efektleri için renk ayrıntısı sağlamak ya da küresel bir nesneye doku 2B bir doku daha az bozulma uygulamak için kullanabilirsiniz.<br /><br /> **Giriş:**<br /><br /> `UVW`: `float3`<br /> Burada örnek alındıktan doku küpü konumu belirtir bir vektör. Örnek bu vektörü küp kesiştiği alınır.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Renk örneği.|**Doku**<br /> Örnekleyici ile ilişkili doku kaydı.|
|**Normal harita örneği**|Belirtilen koordinatlarda 2B bir normal haritayı normal örneği alır<br /><br /> Normal harita görünümü bir nesnenin yüzeyindeki ek geometrik ayrıntının görünümünün benzetimini yapmak için kullanabilirsiniz. Normal haritalar, renk verileri yerine bir birim vektörü temsil eder paket veriler içerir<br /><br /> **Giriş:**<br /><br /> `UV`: `float2`<br /> Burada örnek alındıktan koordinatları.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float3`<br /> Normal örneği.|**Eksen ayarlama**<br /> Normal harita örneğinin taşınabilirliğini ayarlamak için kullanılan etmen.<br /><br /> **Doku**<br /> Örnekleyici ile ilişkili doku kaydı.|
|**UV'yi Kaydır**|Planlar zaman işlevi belirtilen doku koordinatları.<br /><br /> Bu, bir dokuyu veya normal haritayı bir nesnenin yüzeyi taşımak için kullanabilirsiniz.<br /><br /> **Giriş:**<br /><br /> `UV`: `float2`<br /> Kaydırmak için koordinatları.<br /><br /> `Time`: `float`<br /> Tarafından saniyeler içinde kaydırmak için zaman uzunluğu.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float2`<br /> Panned koordinatları.|**Hız X**<br /> Saniyede x ekseni boyunca kaydırılan doku hücresi sayısı.<br /><br /> **Hız Y**<br /> Saniyede y ekseni boyunca kaydırılan doku hücresi sayısı.|
|**Parallax UV**|Belirtilen doku koordinatlarını bir yükseklik ve görüş açısı işlevi olarak değiştirileceğini.<br /><br /> Bu oluşturur etkili olarak da bilinen *paralaks eşlemesi*, ya da sanal yer değiştirme eşlemesi. Bir derinlik atmosferini düz bir yüzeydeki oluşturmak için kullanabilirsiniz.<br /><br /> **Giriş:**<br /><br /> `UV`: `float2`<br /> Öteleme koordinat.<br /><br /> `Height`: `float`<br /> İle ilişkili heightmap değer `UV` koordinatları.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float2`<br /> Hatalı yerleştirilen koordinatları.|**Derinlik düzlemi**<br /> Paralaks efekti için başvuru derinliği. Varsayılan olarak, 0,5 bir değerdir. Küçük değerler dokuyu taşıyın; daha büyük değerler yüzeye batar.<br /><br /> **Derinlik ölçeği**<br /> Paralaks efektini ölçek. Bu görünen derinliği daha fazla veya daha az belirgin hale getirir. Genel değerler 0,02 ile arasındadır 0,1.|
|**UV'yi Döndür**|Merkezi bir nokta etrafında belirtilen doku koordinatlarını zaman işlevi döndürür.<br /><br /> Bu, bir dokuyu veya normal haritayı bir nesnenin yüzeyinde dönecek şekilde kullanabilirsiniz.<br /><br /> **Giriş:**<br /><br /> `UV`: `float2`<br /> Döndürülecek koordinatları.<br /><br /> `Time`: `float`<br /> Tarafından saniyeler içinde kaydırmak için zaman uzunluğu.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float2`<br /> Döndürülen koordinatları.|**Merkez X**<br /> Döndürme merkezini tanımlayan x koordinatı.<br /><br /> **Merkez Y**<br /> Döndürme merkezini tanımlayan y koordinatı.<br /><br /> **hızı**<br /> Radyan cinsinden açı dokunun saniyede döndüğü tarafından.|
|**Doku koordinatı**|Geçerli pikselin doku koordinatları.<br /><br /> Doku koordinatlarını yakın köşelerin doku koordinatı öznitelikleri arasında ilişkilendirme ile belirlenir. Bu, doku alanındaki geçerli pikselin konumu olarak düşünebilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float2`<br /> Doku koordinatları.|Hiçbiri|
|**Doku boyutları**|Genişlik ve yükseklik bir 2B doku eşlemi çıkarır.<br /><br /> Genişlik ve yükseklik doku gölgelendirici de dikkate alınması gereken doku boyutları kullanabilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float2`<br /> Genişlik ve yükseklik vektör olarak ifade edilen dokunun. Genişliği vektör içindeki ilk öğeyi depolanır. İkinci öğe yüksekliği depolanır.|**Doku**<br /> Doku boyutları ile ilişkili doku kaydı.|
|**Doku hücresi Deltası**|Bir 2B doku eşlemi texel'in arasında (uzaklık) delta çıkarır.<br /><br /> Doku hücresi deltasını gölgelendiriciyi komşu texel değerleri örneklemek için kullanabilirsiniz.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float2`<br /> Delta (uzaklık) bir doku hücresi normalleştirilmiş doku alanında bir vektörü olarak ifade edilen (olumlu yönde çapraz taşıma), sonraki texel için. Tüm komşu texel'in konumlarını seçmeli olarak yoksayılıyor veya delta U veya V koordinatlarını negating türetebilirsiniz.|**Doku**<br /> Doku hücresi deltasını ile ilişkili doku kaydı.|
|**Doku örneği**|Belirtilen koordinatlarda 2B doku eşlemi haritasından bir renk örneği alır.<br /><br /> Bir nesnenin yüzeyinde renk ayrıntısını sağlamak için bir doku eşlemi kullanabilirsiniz.<br /><br /> **Giriş:**<br /><br /> `UV`: `float2`<br /> Burada örnek alındıktan koordinatları.<br /><br /> **Çıkış:**<br /><br /> `Output`: `float4`<br /> Renk örneği.|**Doku**<br /> Örnekleyici ile ilişkili doku kaydı.|