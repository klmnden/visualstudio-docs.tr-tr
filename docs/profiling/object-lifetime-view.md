---
title: Nesne ömrü görünümü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.objectlifetime
helpviewer_keywords:
- lifetime, objects
- Objects Lifetime view
- profiling tools reports, Lifetime view
- performance reports, objects lifetime view
- profiling tools, Lifetime view
ms.assetid: d0501fdd-4b3a-4e74-b6ac-51d950a2e15b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6127ae8e76ff7233ff7ad4f7b336325555e57b28
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747200"
---
# <a name="object-lifetime-view"></a>Nesne Ömrü Görünümü
Nesne ömrü görünümü kullanılabilir **ayrıca .NET nesnesi ömür verileri toplayın** üzerinde teslim edildi **performans oturumu** özellik sayfaları.

 .NET Framework'ün çöp toplayıcı ayrılmasını ve uygulamanız için bellek serbest yönetir. Atık toplayıcının performansını optimize etmek için Yönetilen yığın üç kuşaklar halinde ayrılmıştır: 0, 1 ve 2. Yeni nesneler, çalışma zamanının atık toplayıcı nesil 0 depolar. Sonra varlığını sürdüren nesneler yükseltilerek ve depolanan nesil 1 ve 2.

 Çöp toplayıcı tüm nesneleri nesil serbest bırakarak belleği geri kazanır. Profili oluşturulan uygulama tarafından oluşturulan nesneler için nesne ömrü görünümü sayısına ve boyutuna nesneleri ve geri alındığını nesil görüntüler.

## <a name="general"></a>Genel

|Sütun|Açıklama|
|------------|-----------------|
|**Sınıf adı**|Ayrılmış türün sınıf adı.|
|**İşlem kimliği**|Profil oluşturma işlemi kimliği.|
|**İşlem adı**|İşlemin adı.|
|**Modül adı**|İşlevi içeren modül adı.|
|**Modül yolu**|İşlevi içeren modül yolu.|

## <a name="instance-data"></a>Örnek veri
 Örnek verilerini, profil oluşturma çalıştırmasını ve nesil nesneler çöp toplayıcısı tarafından serbest oluşturulmuş türünden nesnelerin sayısını gösterir.

|Sütun|Açıklama|
|------------|-----------------|
|**Örnekler**|Bu tür nesnelerin ayırmaların sayısı.|
|**Toplam örnek sayısı yüzdesi**|Profil oluşturma çalıştırma yapılan ayırmaların toplam sayısının yüzdesi.|
|**0 kuşağı toplanan örnekler**|Nesil atık toplama algoritması 0 serbest türün örneklerinin sayısı.|
|**1 kuşağı toplanan örnekler**|Atık toplama algoritması 1. nesil serbest türün örneklerinin sayısı.|
|**2 kuşağı toplanan örnekler**|Atık toplama algoritması 2. nesil serbest türün örneklerinin sayısı.|
|**Sondaki örnekleri**|Profil oluşturmanın sonuna kadar serbest değil türün örneklerinin sayısını çalıştırın.|

## <a name="size-byte-data"></a>Veri boyutu (bayt)
 Veri boyutu (bayt), profil oluşturma çalıştırmasını ve her nesildeki nesnelerin serbest bırakılmış iadesi bellek miktarını oluşturulmuş türünden nesnelerin boyutunu gösterir.

|Sütun|Açıklama|
|------------|-----------------|
|**Ayrılan toplam bayt**|Türün tüm örnekleri için bayt olarak toplam sayısı.|
|**Toplam Bayt yüzdesi**|Profil oluşturma çalışması bu tür örnekleri için ayrılan ayrılan bayt toplam sayısının yüzdesi.|
|**0 kuşağı toplanan bayt**|Nesil atık toplama algoritması 0 serbest türün örneklerinin boyutu.|
|**1 kuşağı toplanan bayt**|Atık toplama algoritması 1. nesil serbest türün örneklerinin boyutu.|
|**2 kuşağı toplanan bayt**|Atık toplama algoritması 2. nesil serbest türün örneklerinin boyutu.|

## <a name="large-object-heap-data"></a>Büyük nesne yığın verileri
 .NET bellek ayırıcısı standart yönetilen yığından ayrı bir konumda çok geniş nesneleri yönetir. Büyük nesne yığın verisi sayısı ve boyutu bu konumda Yönetilen Nesne türü gösterir.

|Sütun|Açıklama|
|------------|-----------------|
|**Büyük nesne örnekleri toplanan bayt**|Bu tür, büyük nesne yığını içinde bulunan ve profil oluşturma toplanan örnek sayısını çalıştırın.|
|**Büyük nesne yığını toplanan bayt**|Bu tür örnekleri, büyük nesne yığını içinde bulunan ve profil oluşturma çalışmasında toplanan bayt cinsinden boyutu.|

## <a name="see-also"></a>Ayrıca bkz.
- [.NET bellek verisi görünümleri](../profiling/dotnet-memory-data-views.md)