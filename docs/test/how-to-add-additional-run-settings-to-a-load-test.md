---
title: Bir yük testi için çalıştırma ayarları ekleme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, run settings, adding
- load tests, run settings
ms.assetid: 257d2a24-d582-4cfe-8b2b-51f51ba9cc84
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c1d7f9d0c9ad07223d0b59d7aeca585b53432280
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63002249"
---
# <a name="how-to-add-additional-run-settings-to-a-load-test"></a>Nasıl yapılır: Bir yük testine ek çalışma ayarları ekleme

Çalıştırma ayarları yük testinin çeşitli diğer ayarları belirleyin. Bunlar, test sonuçları koleksiyon ayrıntı düzeyi ve test çalıştığında toplanan sayaç kümeleri süresini içerir. Oluşturun ve her bir yük testi için birden çok çalışma ayarlarını depolamak ve ardından test çalıştırması sırasında kullanmak için belirli bir ayar seçin. İlk çalıştırma ayarı kullanarak yük testi oluşturduğunuzda, yük testinize eklenir **Yeni Yük Testi Sihirbazı**.

Yük testi farklı koşullar altında çalıştırabilmeniz için daha fazla yük testinize farklı özellik ayarları ile çalışma ayarları ekleyebilirsiniz. Örneğin, yeni bir test ayarı ekleyin ve farklı bir örnek hızı kullanabilir veya bir uzun çalıştırma süresi belirtin. Ayar etkin olarak işaretleyerek kullanmaya çalıştığı belirtmeniz gerekir ve yalnızca bir çalışma ayarı teker teker kullanabilirsiniz.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-add-another-run-setting"></a>Başka bir çalıştırma ayarı eklemek için

1. Bir yük testi açın.

2. (İsteğe bağlı) Genişletin **çalıştırma ayarları** klasör.

3. Sağ **çalıştırma ayarları** klasörü ve select **çalıştırma ayarları Ekle**.

     Yeni bir çalışma ayarı eklenir **çalıştırma ayarları** klasör.

4. Üzerinde **görünümü** menüsünde seçin **Özellikler penceresi**.

     **Özellikleri** seçili çalışma ayarı için özelliklerle penceresi görüntülenir.

5. İçinde **özellikleri** penceresinde metin kutusunu kullanın **adı** ayar bir adı çalıştırılmasına vermek için özelliği çalışma ayarı amacını açıklar (örneğin, **ayarı çalıştırın: Beş dakika çalıştırma**).

6. Kullanım **özellikleri** çalıştırma ayarlarını değiştirmek için penceresi. Örneğin, çalışma süresini **00:05:00** testiniz için beş dakika çalıştırılacak.

    > [!NOTE]
    > Çalıştırma ayarları özellikleri ve açıklamalarının tam listesi için bkz: [yük testi çalıştırma ayarları özellikleri](../test/load-test-run-settings-properties.md).

     Eklenen çalıştırın ayarını etkin olarak kullanmak istediğiniz artık belirtebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Etkin çalışma ayarı için bir yük testi seçin](../test/how-to-select-the-active-run-setting-for-a-load-test.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testi çalıştırma ayarlarını yapılandırma](../test/configure-load-test-run-settings.md)
- [Sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testi içinde belirtin.](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)