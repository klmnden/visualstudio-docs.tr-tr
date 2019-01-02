---
title: İşlem görünümü - çakışma verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Process view
ms.assetid: 8821d98c-0771-43b2-a38b-e9039a3abd75
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c5eb2a476dd093bf661e40f88795598e4878c313
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53943895"
---
# <a name="process-view---contention-data"></a>İşlem görünümü - çakışma verileri
İşlem görünümü işlemleri ve profil oluşturma çalışması sırasında yürütülen iş parçacığı için Çekişme verilerini görüntüler.  
  
 Semboller kullanılabilir olduğunda işlemler adına göre listelenmiştir. Simgeleri kullanılabilir durumda değilse, işlemleri kendi bellek adresi onaltılık biçiminde listelenir. İş parçacıkları, onları oluşturan işlemin alt öğesi olarak listelenir.  
  
 İşlem görünümü tablodaki sütun değerleri aşağıdaki tabloda açıklanmaktadır.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Başlangıç zamanı**|Milisaniye veya işlemci sayısını, işlem veya iş parçacığı başına profil oluşturma başlangıç geçiş yapar.|  
|**Engellenme süresi**|Bu sırada iş parçacığı ve işlem işlevlerini yürütülmesini engellenen toplam süresi.|  
|**Engellenme süresi yüzdesi**|İşlem veya iş parçacığı ve işlem işlevlerini çalıştırılması engellenen iş parçacığı ömrünün yüzdesi.|  
|**Çakışmaları**|İş parçacığı ve işlem işlevlerini çalıştırılması engellenen sayısı.|  
|**Çekişme yüzdesi**|Profil çalıştıran tüm çekişmelerin yüzdesi, işlem veya iş parçacığı Çekişme yoktu.|  
|**Bitiş zamanı**|Milisaniye veya işlemci sayısını başından sonuna kadar işlem veya iş parçacığı profil oluşturma.|  
|**ID**|Sistem tarafından oluşturulan tanımlayıcısını işlem veya iş parçacığı.|  
|**Yaşam süresi**|Milisaniye veya işlemci sayısını, işlem ya da iş parçacığı işlem veya iş parçacığı sonuna ya da profil oluşturmanın sonuna başından itibaren geçiş yapar.|  
|**Tür**|Satır türü işlem veya iş parçacığı.<br /><br /> Yalnızca **VSReport** komut satırı raporlar. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).|  
|**Ad**|İşlem veya iş parçacığı adı.|  
|**Benzersiz kimliği**|İş parçacığı ve işlem için benzersiz olan bir profil oluşturucu tarafından oluşturulan bir tanımlayıcı.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)   
 [İşlem Görünümü](../profiling/process-view.md)