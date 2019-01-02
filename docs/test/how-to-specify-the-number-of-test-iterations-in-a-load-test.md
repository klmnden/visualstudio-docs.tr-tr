---
title: Yük testi çalışma ayarı Test yineleme sayısını belirtme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, properties
- load tests, run settings
ms.assetid: 45a625db-b3e7-4d64-beda-b9a76248096d
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.openlocfilehash: 6ef3b4197067b379343ea65eb39c734f0ce8916f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53903021"
---
# <a name="how-to-specify-the-number-of-test-iterations-in-a-load-test-run-setting"></a>Nasıl Yapılır: Bir yük testi çalışma ayarı içinde test yineleme sayısını belirtme

İle yükleme testinizi oluşturduktan sonra **Yeni Yük Testi Sihirbazı**, kullanabileceğiniz **Yük Testi Düzenleyicisi** test ihtiyaçlarınızı ve hedeflerinizi karşılayacak şekilde değiştirmek için. Daha fazla bilgi için [izlenecek yol: Bir yük testi oluşturma ve çalıştırma](../test/walkthrough-create-and-run-a-load-test.md).

Kullanarak **Yük Testi Düzenleyicisi**, düzenleyebileceğiniz **Test Yinelemeleri** çalıştırma ayarları değer özelliğini **özellikleri** penceresi. **Test Yinelemeleri** özelliği, tüm web başarım ve birim testleri tüm senaryolarda kullanarak bir yük testi çalıştırmak için yineleme sayısını belirtir **Yük Testi Düzenleyicisi**.

> [!NOTE]
> Çalıştırma ayarları özellikleri ve açıklamalarının tam listesi için bkz: [yük testi çalıştırma ayarları özellikleri](../test/load-test-run-settings-properties.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-specify-the-number-of-test-iterations-in-a-run-setting"></a>Bir çalışma ayarında test yineleme sayısını belirtmek için

1.  Bir yük testi açın.

     **Yük Testi Düzenleyicisi** görünür ve yük testi ağacında görüntüler.

2.  Ağaç, yük test **çalıştırma ayarları** klasör, bir çalışma ayarı seçin.

3.  Üzerinde **görünümü** menüsünde **Özellikler penceresi** yük ayarın kategoriler ve Özellikler çalışma görüntülemek için.

4.  Ayarlama **Test Yinelemeleri Kullan** özelliğini **True**.

5.  İçinde **Test Yinelemeleri** özelliği, yük testi sırasında çalıştırılacak test yineleme sayısını gösteren bir sayı girin.

6.  Özelliği değiştirmeyi bitirdikten sonra seçin **Kaydet** üzerinde **dosya** menüsü. Daha sonra yeni kullanarak yük testlerini çalıştırabilirsiniz **Test Yinelemeleri** değeri.

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi çalıştırma ayarlarını yapılandırma](../test/configure-load-test-run-settings.md)
- [Yük testi senaryosu özellikleri](../test/load-test-scenario-properties.md)