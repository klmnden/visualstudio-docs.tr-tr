---
title: Kaynak çakışması veri değerlerini anlama | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- concurrency profiling method
- Profiling Tools, concurrency method
ms.assetid: 071c0f0f-1eba-4dc8-ae87-0810e4086dd0
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2955790cdd0f322c1a1df75b6586b7e08ce03367
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2018
ms.locfileid: "51727364"
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



