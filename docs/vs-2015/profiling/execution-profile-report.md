---
title: Yürütme Profil raporu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.execution
helpviewer_keywords:
- Concurrency Visualizer, Execution Profile Report
ms.assetid: c8128472-a8ed-46f4-b1c8-a25358d6f2c1
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a0d95d4593939b878194d2aeef79bdd0a8ad946a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54756523"
---
# <a name="execution-profile-report"></a>Yürütme Profil Raporu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yürütme Profil raporu geleneksel örnekleme profilidir. Örnekleri yaklaşık her milisaniyelik zaman bir iş parçacığı bir mantıksal çekirdek üzerinde çalışıyor ve örnek yığınları birikmiş kümesini harmanlama tarafından eşzamanlılık görselleştiricisi tipik çağrı ağacını oluşturur dönemlerde alınır. Bu tablodaki verileri geçerli zaman aralığını ve gizli dizileri ve uygulanabilir bu filtreler tarafından etkilenebilir:  
  
- Yalnızca kendi kodum seçili ise, yalnızca kullanıcı kodunu ve kullanıcı kodu aşağıda bir düzey olan yığın çerçevelerini gösterilmektedir.  
  
- Gürültü azaltma değeri ayarlarsanız, rapordan çıktıklarında belirtilen sıklıkta filtrelenir daha az olan yığınları Harmanlanmış  
  
  Aşağıdaki tabloda, raporda sütunları gösterir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|Ad|İşlev adı çağrı yığınının her düzeyi.|  
|Kapsamlı örnekler|Çağrı yığını ağacı bu düzeye toplanan tüm yığınları için toplanan örneklerin toplam sayısı. Bu işlev için dışlamalı örnekler ve kapsamlı sayaçları tüm alt düğümlerin toplamını kapsamlı sayıdır.|  
|Dışlamalı örnekler|Bu işlev çağrı yığınının en alt düzeyin olduğu toplanan örneklerin toplam sayısı.|  
|% Dahil|Kapsamlı örnekler sütununda gösterilen toplam örneklerin yüzdesi. Yüzde iki ondalık basamağa yuvarlanır.|  
|% Özel|Dışlamalı örnekler sütununda gösterilen toplam örneklerin yüzdesi. Yüzde iki ondalık basamağa yuvarlanır.|  
|Ayrıntılar|İşlev tam adı. Kullanılabilir olduğunda bu satır sayısını içerir.|  
  
 Bu raporu tablosu görülebilir [yürütme zamanı (iş parçacıkları görünümü)](../profiling/execution-time-threads-view.md) görünümü.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İş Parçacıkları Görünümü](../profiling/threads-view-parallel-performance.md)
