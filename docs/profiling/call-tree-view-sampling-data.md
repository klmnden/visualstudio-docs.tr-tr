---
title: Çağrı ağacı görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method,Call Tree view
- Call Tree view
ms.assetid: 5c4e8ec3-d0d3-485a-93bd-9060df4eb739
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6d0655c0faf57a72d6e99ba65f9f84db059e5fe0
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63406010"
---
# <a name="call-tree-view---sampling-data"></a>Çağrı ağacı görünümü - örnekleme verileri
Çağrı ağacı görünümü, profili oluşturulan uygulamada geçiş işlev yürütme yollarını görüntüler.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

 Ağacının kökü, uygulama veya bileşen giriş noktasıdır. Her işlev düğüm, tüm bu işlev çağrıları ile ilgili performans verilerini ve onu çağıran işlevlerini listeler.

 Çağrı ağacı görünümü çağrı ağacında üst işlev tarafından çağrılan işlev örnekleri için değerler. Yüzde değerleri, profil oluşturma çalıştırmasını örneklerin toplam sayısı işlev örneği değerine karşılaştırılmasıyla hesaplanır.

## <a name="highlight-the-execution-hot-path"></a>Yürütme etkin yolu vurgulayın
 Çağrı ağacı görünümü genişletebilir ve işlem ya da en sık örneklenen işlevi yürütme yolunu vurgulayın. En etkin yol görüntülemek için işlem ya da işlev sağ tıklayın ve ardından **etkin yolu Genişlet**.

## <a name="set-the-call-tree-root-node"></a>Çağrı ağacı kök düğüm kümesi
 Profil oluşturma çalıştırmasını her işlem, bir kök düğümü olarak görüntülenir. Çağrı ağacı görünümü başlangıç düğümünün ayarlamak için başlangıç düğümü olarak ayarlayıp istediğiniz düğümü **kümesi kök**.

 Kök düğümü ayarladığınızda, Seçili düğümün alt ağacı dışında görünümünden diğer tüm girişleri kaldırın. Kök düğümü özgün düğüme geri sıfırlamak için çağrı ağacı Görünümü penceresine sağ tıklatın ve seçin **sıfırlama kök**.

|Sütun|Açıklama|
|------------|-----------------|
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|
|**İşlem adı**|İşlemin adı.|
|**Modül adı**|İşlevi içeren modül adı.|
|**Modül yolu**|İşlevi içeren modül yolu.|
|**Kaynak dosyası**|Bu işlevin tanımını içeren kaynak dosya.|
|**İşlev adı**|İşlev tam adı.|
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|
|**İşlev adresi**|İşlevin adresi.|
|**Düzey**|Bu işlev çağrısı ağacında derinliği. Yalnızca [VSPerfReport](../profiling/vsperfreport.md) komut satırı raporlar.|
|**Dışlamalı örnekler**|Çağrı ağacında üst işlevi tarafından çağrıldığında, bu işlevde harcanan toplanan örnek sayısı. Bu sayı toplanan örnek işlev tarafından çağrılan işlevler içermez.|
|**Dışlamalı örnek yüzdesi**|Çağrı ağacında üst işlevi tarafından çağrıldığında, bu işlevin dışlamalı örnekler olan tüm profil oluşturma çalıştırmasını örneklerin yüzdesi.|
|**Kapsamlı örnekler**|Çağrı ağacında üst işlevi tarafından çağrıldığında, bu işlevde harcanan toplanan örnek sayısı. Bu sayı toplanan örnek işlev tarafından çağrılan işlevler içerir.|
|**Kapsamlı örnek yüzdesi**|Çağrı ağacında üst işlevi tarafından çağrıldığında, bu işlevin kapsamlı örnekler olan tüm profil oluşturma çalıştırmasını örneklerin yüzdesi.|

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)
- [Çağrı ağacı görünümü - profil oluşturucu örnekleme verileri](../profiling/call-Tree-view-sampling-data.md)
- [Çağrı ağacı görünümü - örnekleme](../profiling/call-tree-view-dotnet-memory-sampling-data.md)
- [Çağrı ağacı görünümü - izleme](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view-instrumentation-data.md)