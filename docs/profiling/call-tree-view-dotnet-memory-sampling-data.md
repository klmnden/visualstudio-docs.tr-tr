---
title: Çağrı ağacı görünümü - .NET bellek örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Call Tree view
ms.assetid: fbb6cb60-420b-4ca9-8306-2494f7d321fe
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 8d05809d7d2c3c0c93044eee4d44603eac2bffec
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62776819"
---
# <a name="call-tree-view---net-memory-sampling-data"></a>Çağrı ağacı görünümü - .NET bellek örnekleme verileri
Çağrı ağacı görünümü, profili oluşturulan uygulamada geçiş işlev yürütme yollarını görüntüler. Ağacının kökü, uygulama veya bileşen giriş noktasıdır. Her işlev düğümü adlı tüm işlevleri ve bu işlev çağrıları hakkında .NET bellek ayırma verisini listeler.

 Çağrı ağacı görünümü çağrı ağacında üst işlev tarafından çağrılan işlev örnekleri için değerler. Yüzde değerleri, toplam sayısı veya boyutu ayırma profil oluşturma, işlev örneği değerine karşılaştırılmasıyla hesaplanır.

## <a name="highlight-the-execution-hot-path"></a>Yürütme etkin yolu vurgulayın
 Çağrı ağacı görünümü genişletebilir ve işlem ya da en büyük oluşturulan işlev veya çoğu bellek nesneleri yürütme yolunu vurgulayın. En etkin yol görüntülemek için işlem ya da işlev sağ tıklayın ve ardından **etkin yolu Genişlet**.

## <a name="set-the-call-tree-root-node"></a>Çağrı ağacı kök düğüm kümesi
 Profil oluşturma çalıştırmasını her işlem, bir kök düğümü olarak görüntülenir. Çağrı ağacı görünümü başlangıç düğümünün farklı bir düğüme ayarlamak için başlangıç düğümü olarak ayarlayıp istediğiniz düğümü **kümesi kök**.

 Kök düğümü ayarladığınızda, Seçili düğümün alt ağacı dışında görünümünden diğer tüm girişleri kaldırın. Görüntülemekte olduğunuz düğüme geri kök düğümü sıfırlayabilirsiniz; Çağrı ağacı Görünümü penceresine sağ tıklayıp **sıfırlama kök**.

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
|**Düzey**|İşlev çağrısı ağacında derinliği.|
|**Kapsamlı ayırmalar**|Çağrı ağacında üst işlev tarafından çağrılan örnekleri bu işlev tarafından ayrılan nesnelerin sayısı. Bu sayı, alt işlevler tarafından yapılan ayırmaları içerir.|
|**Kapsamlı ayırma yüzdesi**|, Profil oluşturma çalışmasında oluşturulan tüm nesnelerin yüzdesi, bu işlevin kapsamlı ayırmalar yoktu.|
|**Dışlamalı ayırmalar**|Çağrı ağacında üst işlev tarafından çağrılan örnekleri bu işlev tarafından ayrılan nesnelerin sayısı. Bu sayı, alt işlevler tarafından yapılan ayırmaları içermez.|
|**Dışlamalı ayırma yüzdesi**|Yüzde, profil oluşturma çalışmasında oluşturulan tüm nesnelerin çağrı ağacında üst işlev tarafından çağrılan işlev örneklerinin dışlamalı ayırmalar yoktu.|
|**Kapsamlı bayt**|Çağrı ağacında üst işlev tarafından çağrılan örnekleri bu işlev tarafından ayrılan bellek bayt sayısı. Bu sayı, alt işlevler tarafından yapılan ayırmaları içerir.|
|**Kapsamlı bayt yüzdesi**|, Profil oluşturma çalışmasında ayrılan tüm bellek bayt yüzdesi, bu işlevin kapsamlı ayırmalar yoktu.|
|**Dışlamalı bayt**|Çağrı ağacında üst işlev tarafından çağrılan örnekleri bu işlev tarafından ayrılan bellek bayt sayısı. Bu sayı, alt işlevler tarafından yapılan ayırmaları içermez.|
|**Dışlamalı bayt yüzdesi**|, Profil oluşturma çalışmasında ayrılan tüm bellek bayt yüzdesi, bu işlevin dışlamalı ayırmalar yoktu.|

## <a name="see-also"></a>Ayrıca bkz.
- [Çağrı ağacı görünümü - izleme](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view-sampling-data.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view-instrumentation-data.md)