---
title: Çağrı ağacı görünümü - çakışma verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Call Tree view
ms.assetid: 9bd4bde2-2ca3-446c-9ccc-7421522e03ae
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 969945260ee453e84ae2aeec0f28559ca11933a0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62777017"
---
# <a name="call-tree-view---contention-data"></a>Çağrı ağacı görünümü - çakışma verileri
Çağrı ağacı görünümü, profili oluşturulan uygulamada geçiş işlev yürütme yollarını görüntüler. Ağacının kökü, uygulama veya bileşen giriş noktasıdır. Her işlev düğümü adlı tüm İşlevler, işlev engellendi sayısı ve diğer iş parçacıkları veya işlemlerdeki sahip bir kaynak için contending çünkü işlevi engellenen süreyi listeler.

 Çağrı ağacı görünümü çağrı ağacında üst işlev tarafından çağrılan işlev örnekleri için değerler. Yüzde değerleri, profil oluşturma çalıştırmasını çakışması toplam sayısı işlev örneği değerine karşılaştırılmasıyla hesaplanır.

## <a name="highlight-the-execution-hot-path"></a>Yürütme etkin yolu vurgulayın
 Çağrı ağacı görünümü genişletebilir ve işlem ya da çoğu Çekişme oluşturulan işlev yürütme yolunu vurgulayın.

- En etkin yol görüntülemek için işlem ya da işlev sağ tıklayın ve ardından **etkin yolu Genişlet**.

## <a name="set-the-call-tree-root-node"></a>Çağrı ağacı kök düğüm kümesi
 Profil oluşturma çalıştırmasını her işlem, bir kök düğüm olarak görünür. Çağrı ağacı görünümü başlangıç düğümünün ayarlamak için başlangıç düğümü olarak ayarlayın ve ardından istediğiniz düğümü **kümesi kök**.

 Kök düğümü ayarladığınızda, Seçili düğüme alt ağacı dışında görünümünden diğer tüm girişleri kaldırın. Kök düğümü özgün düğüme geri sıfırlamak için çağrı ağacı Görünümü'nde sağ tıklayın ve ardından **sıfırlama kök**.

|Sütun|Açıklama|
|------------|-----------------|
|**Dışlamalı engellenme süresi**|Bu yürütme yolunu Bu işlevde örneklerini profil oluşturma çalışmasında çalıştırılması engellenen zaman. Süresi alt işlevlerin işlev tarafından çağrılmış engellenme süresi içermez.|
|**Dışlamalı engellenme süresi yüzdesi**|Dışlamalı engellenme süresi için bu yürütme yolunu Bu işlevde, profil oluşturma çalışması içindeki tüm engellenme süresinin yüzdesi.|
|**Dışlamalı Çekişmeler**|Bu yürütme yolunu Bu işlevde örneklerinde oluştu çekişmelerin sayısı. Sayı, alt işlevlerin işlev tarafından çağırılan Çekişme içermez.|
|**Dışlamalı Çekişme yüzdesi**|Dışlamalı Çekişme çağrı ağacında üst işlev tarafından çağrılan örnekleri bu işlevin olan tüm profil oluşturma çalıştırmasını çakışması yüzdesi.|
|**İşlev adresi**|İşlevin adresi.|
|**İşlev adı**|İşlev tam adı.|
|**Kapsamlı engellenme süresi**|Bu yürütme yolunu Bu işlevde örneklerini profil oluşturma çalışmasında çalıştırılması engellenen toplam zaman. İşlev tarafından çağrılan alt işlevlerin engellenme süresi geçen süreyi de içerir.|
|**Kapsamlı engellenme süresi yüzdesi**|Profil çalıştıran tüm engellenme süresinin yüzdesi bu yürütme yolunu Bu işlevde örnekleri için kapsamlı engellenme süresi oldu.|
|**Kapsamlı Çekişmeler**|Bu yürütme yolunu Bu işlevde örneklerini engellenen çekişmelerin toplam sayısı. Sayı, alt işlevlerin işlev tarafından çağırılan Çekişme içerir.|
|**Kapsamlı Çekişme yüzdesi**|Profil çalıştıran tüm çekişmelerin yüzdesi bu yürütme yolunu bu işlevdeki örneklerin kapsamlı çekişmeler yoktu.|
|**Düzey**|İşlev çağrısı ağacında düzeyi. Yalnızca VSReport komut satırı raporlarda. Daha fazla bilgi için bkz [VSPerfReport](../profiling/vsperfreport.md).|
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|
|**Modül adı**|İşlevi içeren modül adı.|
|**Modül yolu**|İşlevi içeren modül yolu.|
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|
|**İşlem adı**|İşlemin adı.|
|**Kaynak dosyası**|Bu işlevin tanımını içeren kaynak dosya.|

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view.md)
- [Çağrı ağacı görünümü - izleme](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)
- [Çağrı ağacı görünümü - örnekleme](../profiling/call-tree-view-dotnet-memory-sampling-data.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view-instrumentation-data.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view-sampling-data.md)