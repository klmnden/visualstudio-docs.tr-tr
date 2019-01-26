---
title: Kaynak çekişmeleri görünümü - çakışma verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.resourcecontention
helpviewer_keywords:
- Resource Contentions view
ms.assetid: 14a7f774-211f-4ef8-af05-94d1c8f65d2f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 57fc5075ee375ed73b448e8a90e8bb2c3e22e7bf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54970818"
---
# <a name="resource-contentions-view---contention-data"></a>Kaynak Çakışmaları Görünümü - Çakışma Verileri
Çekişme olayları kaynağı olan kaynaklar için Çekişme verisi kaynak çakışması görünümü listeler. Bir iş parçacığında bir işlev kaynağa erişim için başka bir iş parçacığı bir işlevde kaynağına özel erişim aldığından beklenecek zorlanır Çekişme olayı oluşur. Her kaynak Çekişme olayıyla sonuçlandı işlevi yürütme yollarını görüntüler bir çağrı ağacı kök düğümüdür.  
  
## <a name="data-values"></a>Veri değerleri  
  
### <a name="resource-values"></a>Kaynak değerler  
 Kaynak satırı verilerinde kaynağa erişimi engellenmiş olan toplam süre profil oluşturma verilerinin ve bu kaynağa erişim çakışması nedeniyle oluştu Çekişme olayları toplam sayısını görüntüler. Dahil ve hariç bir kaynak için her zaman aynı değerlerdir.  
  
### <a name="function-values"></a>İşlev değerleri  
 İşlev değerleri, çağrı ağacında temsil yürütme yolunu ortaya işlevi örneklerini temel alır.  
  
-   Özel değerler deyimleri kendi işlev gövdesindeki işlev yürütülürken gerçekleşen olayları temel alır. İşlev tarafından çağrılan işlevler içinde oluşan olaylar özel değerleri dahil edilmez.  
  
-   Kapsamlı değerler, işlev veya işlev tarafından çağrılan bir işlev yürütülürken gerçekleşen olayları temel alır.  
  
### <a name="percentage-values"></a>Yüzde değerleri  
 Yüzde değerleri, profil oluşturma verilerinin toplam süre veya Çekişme olayları temel alır. Rapor veya profil oluşturma çalışması görünümünü filtrelediyseniz yalnızca engellenme süresi ve çekişmeleri filtrelenmiş veri toplam değeri olarak kullanılır.  
  
## <a name="navigating-the-resource-allocation-view"></a>Kaynak ayırma görünümü gezinme  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Ad**|Kaynak veya işlevin adı.|  
|**Dışlamalı engellenme süresi**|-Bir kaynak için toplam süre bu kaynağa erişim engellenir ve beklenecek bir iş parçacığı nedeniyle.<br />-Bir işlev için işlevinin bu örnekler, işlev işlev gövdesinde kod yürütülürken üst kaynak erişimi engellenen zaman. İşlev tarafından çağrılan işlevler engellenme süresi dahil değildir.|  
|**Dışlamalı engellenme süresi yüzdesi**|-Bir kaynak, engellenmiş olan profil oluşturma veri tüm engellenme süresinin yüzdesi için bu kaynak süresi<br />-Bir işlev, bu işlevi örneklerin dışlamalı engellenme süresi olan profil oluşturma veri tüm engellenme süresinin yüzdesi için.|  
|**Dışlamalı Çekişmeler**|-Bir kaynak için toplam sayısı kaynağa erişim engellendi ve beklenecek bir iş parçacığı nedeniyle.<br />-Bir işlev için işlevinin bu örnekler, işlev işlev gövdesinde kod yürütülürken üst kaynak erişimi engellenen sayısı. İşlev tarafından çağrılan işlevler engelleme olayları dahil edilmez.|  
|**Dışlamalı Çekişme yüzdesi**|-Bir kaynak için tüm Çekişme olayları bu kaynağa erişim için Çekişme olayları olan profil oluşturma veri yüzdesi.<br />-Bir işlev için tüm Çekişme olayları dışlamalı Çekişme olayları üst kaynak için bu işlevi örneklerin olan profil oluşturma veri yüzdesi.|  
|**Kapsamlı engellenme süresi**|-Bir kaynak için toplam süre bu kaynağa erişim engellenir ve beklenecek bir iş parçacığı nedeniyle.<br />-Bir işlev için işlev veya tüm işlevlerin bu örnekler örnekleri tarafından çağrılan zaman işlev işlev gövdesinde kod yürütülürken üst kaynağına erişim engellendi.|  
|**Kapsamlı engellenme süresi yüzdesi**|-Bir kaynak, engellenmiş olan profil oluşturma veri tüm engellenme süresinin yüzdesi için bu kaynak süresi<br />-Bir işlev için çalışmasını profil oluşturma tüm engellenme süresinin yüzdesi bu işlevi örneklerin kapsamlı engellenme süresi oldu.|  
|**Kapsamlı Çekişmeler**|-Bir kaynak için toplam sayısı kaynağa erişim engellendi ve beklenecek bir iş parçacığı nedeniyle.<br />-Bir işlev için çalışmasını profil oluşturma tüm Çekişme olayları yüzdesi olan üst kaynak için bu işlevi örneklerin kapsamlı Çekişme olayları.|  
|**Kapsamlı Çekişme yüzdesi**|-Çekişme olayları bu kaynağa erişim için bir kaynak için çalışmasını profil oluşturma tüm Çekişme olayları yüzdesi yoktu.<br />-Bir işlev için işlevinin bu örnekler, işlev işlev gövdesinde kod yürütülürken üst kaynak erişimi engellenen sayısı. İşlev tarafından çağrılan işlevler engelleme olayları dahil edilmez.|  
|**Düzey**|Bu işlev çağrısı ağacında derinliği. Yalnızca [VSPerfReport](../profiling/vsperfreport.md) komut satırı raporlar.|  
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|  
|**Modül adı**|İşlevi içeren modül adı.|  
|**Modül yolu**|İşlevi içeren modül yolu.|  
|**İşlem kimliği**|İşlevi, yürütülmekte olan işlemin işlem kimliği (PID).|  
|**İşlem adı**|İşlemin adı.|  
|**Kaynak dosyası**|Bu işlevin tanımını içeren kaynak dosya.|