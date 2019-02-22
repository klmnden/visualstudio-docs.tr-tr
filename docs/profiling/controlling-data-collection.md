---
title: Veri toplama denetimi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- advanced tasks for profiling tools
- profiling tools, advanced tasks
ms.assetid: e713ad63-b948-46f3-8db9-59b30922ebe5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 250ec5623a02f962a0d56d7f469ed37afee097ab
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630333"
---
# <a name="control-data-collection"></a>Veri toplamayı denetleme
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profil Oluşturma Araçları, bir performans oturumu sırasında profil oluşturma verilerinin ne zaman toplanacağını kontrol etmenizi ve profillenen işlevleri belirtmenizi sağlar. Bu bölümde, veri koleksiyonunu durdurmak ve başlatmak açıklar **performans Gezgini** ve **veri koleksiyonu denetimi** windows ve kendisi için profil oluşturma verilerinin toplandığı nesnelerin nasıl.

## <a name="common-tasks"></a>Ortak görevler

|Görev|İlgili içerik|
|----------|---------------------|
|**Başlatın ve profil oluşturmayı durdur:** Uygulama başlatıldığında bir uygulamanın veya profil oluşturucu zaten çalışan bir işleme iliştirilebilir profili başlayabilirsiniz. Hedef uygulama çalışırken, veri toplamayı duraklatabilir ve devam ettirebilirsiniz. Hedef uygulamayı kapatarak veya profil oluşturucuyu çalışan bir işlemden ayırarak bir profil oluşturma oturumunu sonlandırabilirsiniz. |-   [Nasıl Yapılır: Başlangıç ve bitiş performans verilerini toplama](../profiling/how-to-start-and-end-performance-data-collection.md)<br />-   [Nasıl Yapılır: Ekleme ve ayırma işlemleri çalıştırmak için performans araçları](../profiling/how-to-attach-and-detach-performance-tools-to-running-processes.md)<br />-   [Nasıl Yapılır: Duraklatma ve sürdürme performans verilerini toplama](../profiling/how-to-pause-and-resume-performance-data-collection.md)|
|**Toplanan verileri sınırlamak için profil oluşturma Araçları'nı yapılandırın:** Performans oturumu yapılandırma özelliklerini, şüpheli işlem yöntemini kullanan çalıştırmaları profil oluşturma çalışmasında toplanan verileri sınırlamak için kullanabilirsiniz. Belirli .dll dosyalarını, ad alanlarını, sınıfları ve işlevleri dahil edebilir veya hariç tutabilirsiniz. Ayrıca, belirttiğiniz bir boyut eşiğini karşılamayan işlevleri çıkarabilirsiniz.|-   [Nasıl Yapılır: Sınırı izlemeyi belirli DLL'ler](../profiling/how-to-limit-instrumentation-to-specific-dlls.md)<br />-   [Nasıl Yapılır: Belirli işlevler için izlemeyi sınırı](../profiling/how-to-limit-instrumentation-to-specific-functions.md)<br />-   [Nasıl Yapılır: Hariç tutma veya kısa işlevleri izlemeden içerir](../profiling/how-to-exclude-or-include-short-functions-from-instrumentation.md)|

## <a name="related-sections"></a>İlgili bölümler
- [Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)

## <a name="see-also"></a>Ayrıca bkz.
- [Performans Gezgini](../profiling/performance-explorer.md)