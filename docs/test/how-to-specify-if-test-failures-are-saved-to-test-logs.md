---
title: Test hataları için yük testi Kaydet
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, scenarios
- load tests, logging
ms.assetid: 08a7fe98-a7f7-4b8d-94a3-ec82b65a2aaf
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ef80a10954e9cf58db04e46f11934ffd86974bea
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60075174"
---
# <a name="how-to-specify-if-test-failures-are-saved-to-test-logs-using-the-load-test-editor"></a>Nasıl yapılır: Test hata günlükleri Yük Testi Düzenleyicisini kullanarak test etmek için kaydedilip kaydedilmediği belirleme

İle yükleme testinizi oluşturduktan sonra **Yeni Yük Testi Sihirbazı**, kullanabileceğiniz **Yük Testi Düzenleyicisi** test ihtiyaçlarınızı ve hedeflerinizi karşılamak için yük testi özelliklerini değiştirmek için. Bkz: [izlenecek yol: Bir yük testi oluşturma ve çalıştırma](../test/walkthrough-create-and-run-a-load-test.md). Test günlüğü değiştirerek bir yük testi içinde bir test başarısız olursa kayıtlı olmasını isteyip istemediğinizi belirtebilirsiniz **Test hatasında günlüğünü Kaydet** özelliği.

> [!NOTE]
> Çalıştırma ayarları özellikleri ve açıklamalarının tam listesi için bkz: [yük testi çalıştırma ayarları özellikleri](../test/load-test-run-settings-properties.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-specify-if-the-test-log-is-saved-when-a-test-fails-in-a-scenario"></a>Test günlüğü, bir senaryoda, bir test başarısız olduğunda kaydedilirse belirtmek için

1. Bir yük testi açın.

     **Yük Testi Düzenleyicisi** görünür. Yük testi ağacında görüntülenir.

2. Yük testi **çalıştırma ayarları** klasörü, en fazla test yinelemesi sayısını belirtmek istediğiniz çalışma ayarları düğümünü seçin.

3. Üzerinde **görünümü** menüsünde **Özellikler penceresi**.

     Çalıştırma ayarları kategoriler ve özellikler görüntülenir **özellikleri** penceresi.

4. İçinde **Test hatasında günlüğünü Kaydet** özelliği seçin **True** veya **False** senaryoda test hatası durumunda test günlüğü kaydetmek isteyip istemediğinizi belirtmek için.

     Özelliği değiştirmeyi bitirdikten sonra seçin **Kaydet** üzerinde **dosya** menüsü.

     Yük Testi Çözümleyicisinin Tablo görünümü kullanarak günlüğe kaydedilen verileri görüntülenebilir. Daha fazla bilgi için [yük testi sonuçlarını ve hatalarını Tablo görünümünde çözümlemek](../test/analyze-load-test-results-and-errors-in-the-tables-view.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi senaryolarını düzenleme](../test/edit-load-test-scenarios.md)
- [İzlenecek yol: Bir yük testi oluşturma ve çalıştırma](../test/walkthrough-create-and-run-a-load-test.md)