---
title: Yük Testlerini Düzenleme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- Load Test Editor
- load tests, Load Test Editor
ms.assetid: ba16ed02-137e-40bf-a4cb-45d87d922d37
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.openlocfilehash: 7a02db6fb91eb303a05a27b4f135445891098a7c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54995680"
---
# <a name="edit-load-tests"></a>Yük testlerini düzenleme

Çalıştırma web başarım testi veya birim testleri, bir sunucu aynı anda erişen birçok kullanıcının benzetimini yapmak için yük testleri. Bir yük testi uygulama stres ve performans verilerine erişmenizi sağlar. Bir yük testi, kullanıcı yükleri gibi çeşitli yük koşulları taklit etmek ve ağ türleri için yapılandırılabilir.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

Bir yük testi tarafından tanımlanan *senaryoları*, *sayaç kümeleri*, ve *çalıştırma ayarları*. Aşağıdaki çizim arasındaki farklar açıklanmaktadır [senaryoları](../test/edit-load-test-scenarios.md), [sayaç kümeleri](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md), ve [çalıştırma ayarları](../test/load-test-run-settings-properties.md):

![Yük testi mimarisi](../test/media/load_test_editor.png)

## <a name="software-requirements"></a>Yazılım gereksinimleri

Yalnızca Web performans ve yük testi projelerini Visual Studio Enterprise sürümünde kullanılabilir.

## <a name="edit-load-test-scenario-settings"></a>Yük testi senaryosu ayarlarını Düzenle

Bir senaryo, bir kullanıcı grubu, bir sunucu uygulaması ile nasıl etkileşimde bulunduğunu modellemek için kullanılır. Bir senaryo, bir yük düzeni, test karışımı modeli, test karışımı, tarayıcı karışımı ve ağ karışımını oluşur. Bir yük testi birden fazla senaryosu olabilir ve tek bir senaryo, web performans testleri ve birim testleri içerebilir. Gruplandırma benzer ayarıyla birlikte, bir senaryo grup ve testler bir yapıdaki birlikte çalıştırmanıza olanak tanır.

Daha fazla bilgi için [yük testi senaryolarını düzenleme](../test/edit-load-test-scenarios.md) ve [yük testi senaryosu özellikleri](../test/load-test-scenario-properties.md).

## <a name="configure-and-manage-performance-counter-sets"></a>Yapılandırma ve performans sayaç kümelerini Yönet

Yükleme testleri, performans sayacı verilerini çözümlediğinizde kullanışlı olan teknoloji tarafından düzenlenen adlandırılmış sayaç kümeleri sağlar. Sayaç kümleri, yükleme testi, IIS, ASP.NET ve SQL içerir. İle bir yük testi oluşturduğunuzda, **Yeni Yük Testi Sihirbazı**, başlangıç bir önceden tanımlanmış ve önemli sayaç kümesi yük testine dahil etmek üzere belirttiğiniz bilgisayarlar için yapılandırılır. Sayaçlarınızı yönettiğiniz **Yük Testi Düzenleyicisi**.

Daha fazla bilgi için [sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testinde belirtin](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md).

## <a name="configure-and-manage-load-test-run-settings"></a>Yapılandırma ve yükleme testi çalıştırma ayarlarını yönetme

Çalıştırma ayarları yük testinin çalışma biçimini etkileyen özelliklerdir. Çalıştırma ayarları kategorilere göre düzenlenir **özellikleri** penceresi.

Daha fazla bilgi için [yapılandırma yük testi çalıştırma ayarları](../test/configure-load-test-run-settings.md) ve [yük testi çalıştırma ayarları özellikleri](../test/load-test-run-settings-properties.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
- [Eşik kuralı ihlallerini çözümleme](../test/analyze-threshold-rule-violations-in-load-tests.md)