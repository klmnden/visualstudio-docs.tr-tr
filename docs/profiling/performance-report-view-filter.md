---
title: Performans Raporu Görünüm Filtresi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools, Profiler Report view filter
- Profiler Report View filter, profiling tools
ms.assetid: 35f89d86-4683-4db1-aa0c-ae0ce65fa524
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ae4c5281386cb43d4dddb55db8578aea7515dce1
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56620908"
---
# <a name="performance-report-view-filter"></a>Performans Raporu Görünüm Filtresi
**Profiler Rapor Görünümü Filtresi** penceresinin en üstündeki bulunduğu **performans raporu** penceresi. Göremiyorsanız, tıklayın **Göster filtre** düğmesi.

 Her filtre yan tümcesi, sonuçlarınızı daraltmak için değiştirebilirsiniz. Aşağıdaki sütunlar, filtre Oluşturucusu'nda kullanılabilir.

|Filtre öğesi|Açıklama|
|-----------------|-----------------|
|Ve/veya|Seçin **ve** eşleşiyorsa bir sonuç bu yan tümce hem de sonraki yan tümcesi her ikisi de true olmalıdır. Seçin **veya** eşleşiyorsa bir sonucu veya bu yan tümce hem de sonraki yan tümcesi True olabilir.|
|Alan|Filtre yan tümcesi geçerli rapor dosyada kullanılabilir olan veri alanları listesinden kullanılacak bir alan seçin.|
|İşleç|Alan ve değer arasında istediğiniz ilişkiyi belirtir işleci seçin.<br /><br /> = Eşittir<br /><br /> <> Eşit değildir<br /><br /> < Küçüktür<br /><br /> > Büyüktür<br /><br /> < = küçüktür veya eşittir<br /><br /> > = büyüktür veya eşittir|
|Değer|Aranacak bir değer girin veya seçin. Bazı alanları, alan için kullanılabilen değerleri listeler.|

 Filtre en iyi sonuçlar verecek düşündüğünüz kadar filtre yan tümce ekleyebilirsiniz. Tıklayın **yürütme filtre** veri dosyasına filtre uygulamak için.

 Gelen **işaretleri** rapor görünümü, verileri iki işaretler arasında toplanan veriler için rapor görünümlerini sınırlandırmak için filtre yan tümcesi üretebilir. Başlangıç ve bitiş veri, sonra sağ tıklayıp ya da rapor için istediğiniz işaretleri seçin **işaretleri filtreye Ekle** veya **zaman damgalarına Filtre Ekle**. Her iki filtreleri aynı aralığa geçerli veri dosyasındaki verileri sınırlamak; **İşaretleri filtreye Ekle** diğer .vsp dosyalarına uygulanabilir.

 Filtre kaydetmek için tıklatın **dışarı aktarma filtre** üzerinde **performans raporu** araç ve ardından bir konum ve dosya adını belirtin. *vspf* dosya. Daha önce kaydedilen bir filtreyi yüklemek için tıklayın **içeri aktarma filtre** ve kaydedilmiş filtre dosyasını bulun. Filtre dosyaları, veri dosyalarını bağımsız profil oluşturma araçları yüklü olan bilgisayarlarda filtrelemek için de kullanılabilir. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Performans araçları verilerini analiz etme](../profiling/analyzing-performance-tools-data.md)
- [VSPerfReport](../profiling/vsperfreport.md)