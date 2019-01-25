---
title: Kaynak çakışması veri değerlerini anlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- concurrency profiling method
- Profiling Tools, concurrency method
ms.assetid: 071c0f0f-1eba-4dc8-ae87-0810e4086dd0
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5983396924f38c31b6dafcd42b762042e1880e8d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784122"
---
# <a name="understanding-resource-contention-data-values"></a>Kaynak Çakışması Veri Değerlerini Anlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kaynak Çekişme profil oluşturma, paylaşılan bir kaynağa erişim için beklenecek rakip iş parçacığı bir uygulamada zorlanan ayrıntılı çağrı yığını bilgileri her zaman toplar.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
  Kaynak Çekişme raporları Çekişme ve modüller, İşlevler, kaynak kod satırlarına ve yönergeleri bekleniyor gerçekleştiği için bir kaynak beklerken geçen toplam süre toplam sayısını görüntüler.  
  
- Kapsamlı değerleri bir işlev tarafından kaynak çakışmaları beklenecek zorunlu Çekişme ve işlev beklenen toplam süre toplam sayısını görüntüler.  İşlev tarafından çağrılan alt işlevler kaynaklanan Çekişme kapsamlı değerleri dahil edilir.  
  
- Özel değeri yalnızca, zorlamalı beklenecek bir işlev ve işlev gövdesindeki kod tarafından neden çekişmelerin sayısı görüntüler. Çekişme alt işlevlerin neden dahil edilmez. Dışlamalı süre işlevi, işlev gövdesindeki deyimleri kaynaklanan bekleme süresini de içerir.  
  
  Kaynak çakışması rapor görünümleri Ayrıca, zaman içindeki tek tek Çekişme olayları Göster zaman çizelgesi grafikleri içerir ve belirli olay oluşturulan çağrı yığınları göster. Daha fazla bilgi için aşağıdaki konulardan birine bakın:  
  
- [İş Parçacığı Ayrıntıları Görünümü](../profiling/thread-details-view-contention-data.md)  
  
- [Kaynak Ayrıntıları Görünümü](../profiling/resource-details-view-contention-data.md)  
  
  Eşzamanlılık profil oluşturması ikinci modu hakkında daha fazla bilgi için bkz: [eşzamanlılık görselleştiricisi](../profiling/concurrency-visualizer.md).
