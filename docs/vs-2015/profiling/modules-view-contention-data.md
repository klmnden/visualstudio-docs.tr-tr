---
title: Modüller görünümü - çakışma verileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Modules view
ms.assetid: 1a9aa122-2d8f-4a09-b503-92975aa6b648
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9a2553396614cacbc22925f8f7f3a61d56c50541
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771046"
---
# <a name="modules-view---contention-data"></a>Modüller Görünümü - Çakışma Verileri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Modüller görünümü Çekişme veri profil oluşturma verileri örneklenen modüller tarafından gruplandırılmış eşzamanlılık verileri görüntüler. Her bir hiyerarşik ağaç kökünde modülüdür. Çekişme olayları oluştuğu modülündeki işlevlerin modülü düğümünün altında listelenir.  
  
 Diğer bir deyişle, çekişmeyi olay gerçekleştiğinde, kendi kod işlevi çalıştırıldığında işlev çağrı yığını, kaynak satırları ve yönerge Yürütülüyor adresler işlevi düğümü altında listelenen üst kısmındaki oluştu. Satırı veya yönerge yürüttüğünde veri kaynak satırı veya bir yönerge işaretçisini toplandığından, dahil ve hariç olan değerler her zaman satır verileri hem de yönerge veri için aynıdır.  
  
 Çekişme verisi, modüller görünümünde sütun değerleri aşağıdaki tabloda açıklanmaktadır.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Dışlamalı engellenme süresi**|-Bir işlev için bu işlev, işlev gövdesinde kod yürütürken gelen engellendiği zaman. İşlev tarafından çağrılan işlevler engellenme süresi dahil değildir.<br />-Bir modül için modülündeki işlevlerin dışlamalı engellenme süresi toplamı.<br />-Bir satır veya bir yönerge, saati için bu satırı veya yönerge yürütülmesini engellendi.|  
|**Dışlamalı engellenme süresi yüzdesi**|-Bir işlev veya modül için profil çalıştıran tüm engellenme süresinin yüzdesi bu işlev veya modül dışlamalı engellenme süresi oldu.<br />-Bir satır veya bir yönerge, profil oluşturma çalıştırmasını burada tüm engellenen süreyi bu satırı veya yönerge yürütülmesini engellendi yüzdesi için.|  
|**Dışlamalı Çekişmeler**|-Bir işlev için bu işlev, işlev gövdesinde kod yürütürken gelen engellendi sayısı. İşlev tarafından çağrılan işlevler çakışması dahil edilmez.<br />-Bir modül için modülündeki işlevlerin dışlamalı çekişmeler toplamı.<br />-Bir satır veya bu satırı veya yönerge yürütülmesini engellendiğini bir yönerge sayısı için.|  
|**Dışlamalı Çekişme yüzdesi**|-Bir işlev veya modül için profil çalıştıran tüm çekişmelerin yüzdesi bu işlev veya modül dışlamalı çekişmeler yoktu.<br />-Bir satır veya bir yönerge için profil çalıştıran tüm çekişmelerin yüzdesi bu satırı veya yürütülmesini yönerge engellenen Çekişme yoktu.|  
|**Kapsamlı engellenme süresi**|-Bir işlev için bu işlev veya bu işlev tarafından çağrılan bir işlevin yürütülmesini engellendiği zaman.<br />-Bir modül için bu modülün hangi en az bir işlevdeki engellenme süresi toplamı yığında oluştu.<br />-Bir satır veya bir yönerge, saati için bu satırı veya yönerge yürütülmesini engellendi.|  
|**Kapsamlı engellenme süresi yüzdesi**|-Bir işlev veya modül için profil çalıştıran tüm engellenme süresinin yüzdesi bu işlev veya modül, kapsamlı engellenme süresi oldu.<br />-Bir satır veya bir yönerge için profil oluşturma tüm engellenme süresinin yüzdesi çalıştırın, bu satırı veya yönerge Yürütülüyor içinde.|  
|**Kapsamlı Çekişmeler**|-Bir işlev için bu işlevi veya bu işlev tarafından çağrılan bir işlevin yürütülmesini engellendi sayısı.<br />-Bir modül için hangi en az bir işlevde bu modülündeki çekişmelerin sayısı yığında oluştu.<br />-Bir satır veya bu satırı veya yönerge yürütülmesini engellendiğini bir yönerge sayısı için.|  
|**Kapsamlı Çekişme yüzdesi**|-Bir işlev veya bir modül için çalışmasını profil oluşturma tüm çekişmelerin yüzdesi bu işlev veya modül kapsamlı çakışmaları oldu.<br />-Bir satır veya bir yönerge için profil oluşturma tüm engellenme süresinin yüzdesi çalıştırın, bu satırı veya yönerge Yürütülüyor içinde.|  
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|  
|**Modül adı**|İşlevi, çizgi veya yönerge işaretçisini içeren modül adı.|  
|**Modül yolu**|Modül, işlev, satır veya yönerge işaretçisini içeren modül yolu.|  
|**Ad**|Modülün veya işlevin adı.|  
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|  
|**İşlem adı**|İşlemin adı.|  
|**Kaynak dosyası**|Bu işlevin tanımını içeren kaynak dosya.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)   
 [Modüller görünümü](../profiling/modules-view.md)   
 [Modüller görünümü - izleme](../profiling/modules-view-dotnet-memory-instrumentation-data.md)   
 [Modüller görünümü - örnekleme](../profiling/modules-view-dotnet-memory-sampling-data.md)   
 [Modüller görünümü](../profiling/modules-view-instrumentation-data.md)   
 [Modüller Görünümü](../profiling/modules-view-sampling-data.md)
