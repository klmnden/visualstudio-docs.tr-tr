---
title: Katman etkileşimleri görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.tierinteraction
helpviewer_keywords:
- Tier Interactions view
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8a3bf4f5fd7ab18efb13e1c52847daf647e908b7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640850"
---
# <a name="tier-interactions-view"></a>Katman Etkileşimleri Görünümü

Katman etkileşim profili oluşturma veritabanları ile iletişim kuran çok verili uygulamaların yürütme sürelerini işlevleri hakkında ek bilgi sağlayan [!INCLUDE[vstecado](../data-tools/includes/vstecado_md.md)]. Verileri yalnızca zaman uyumlu işlev çağrıları için toplanır.

**Gereksinimler**

- Visual Studio Enterprise

Etkileşimleri görünümü iki dosyada katman etkileşim verileri görüntüler:

- Ana bölme bir hiyerarşik ağaç vardır. Veritabanı bağlantıları ilişkin birleşik veriler en üst düzey satır içeren bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] sayfası ya da işlem. Alt düğümler üst veritabanı bağlantıları ilişkin birleşik veriler içerir.

- Bir veritabanı çağrısı düğüm ana bölmede tıkladığınızda, veriler veritabanı çağrısı örneği için Ayrıntılar bölmesinde görüntülenir.

  Süre, milisaniye sayısını veya CPU saat işareti olarak görüntülenir. Görüntülenen zaman birimi değiştirmek için tıklayın **Araçları** menüsünde tıklayın **seçenekleri**ve ardından aşağıdakilerden birini seçin **zamanın gösterilme biçimi değerleri olarak** seçenekleri.

## <a name="master-pane"></a>Ana bölmesi

|Sütun|Açıklama|
|------------|-----------------|
|**Ad**|-Bir üst düzey satır, profili oluşturulmuş işlem ya da Web sayfası adı için.<br />-Veritabanı bağlantısı için bir satır, veritabanını barındıran sunucunun adı.|
|**Veritabanı**|(Yalnızca veritabanı bağlantı satırlar) veritabanının adı.|
|**Sayısı**|İşlem, Web sayfası veya veritabanı bağlantısı tarafından oluşturulan isteklerinin toplam sayısı.|
|**Toplam geçen süre**|İşlem, Web sayfası veya veritabanı bağlantısı herhangi bir isteği yürütmek için harcanan toplam süre.|
|**Geçen maksimum süre**|İşlem, Web sayfası veya veritabanı bağlantısı herhangi bir istek yürütülürken harcanan maksimum süre.|
|**Geçen minimum süre**|İşlem, Web sayfası veya veritabanı bağlantısı herhangi bir istek yürütülürken harcanan minimum süre.|
|**Geçen ortalama süre**|İşlem, Web sayfası veya veritabanı bağlantısı isteği yürütmek için harcanan ortalama süre.|

## <a name="database-connection-details-pane"></a>Veritabanı bağlantı ayrıntıları bölmesi

|Sütun|Açıklama|
|------------|-----------------|
|**Komut metni**|İsteğin SQL sorgusu.|
|**Sorgu sayısı**|Sorgu çalıştırılma sayısı.|
|**Toplam geçen süre**|Örnek sorgu yürütmek için harcanan toplam süre.|
|**Geçen maksimum süre**|Herhangi bir örnek sorgu yürütmek için harcanan maksimum süre.|
|**Geçen minimum süre**|Herhangi bir örnek sorgu yürütmek için harcanan minimum süre.|
|**Geçen ortalama süre**|Bir örnek sorgu yürütmek için harcanan ortalama süre.|