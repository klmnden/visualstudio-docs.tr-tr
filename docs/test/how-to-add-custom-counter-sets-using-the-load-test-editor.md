---
title: Yük testi için özel sayaç kümeleri ekleme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- counters, counter sets
- counter sets
- load tests, counter sets
ms.assetid: 499aca80-1069-408d-ac68-326da6a50645
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 40ce0d5d4c1988e40a7b7530b61fcfbaa1f7131d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62950299"
---
# <a name="how-to-add-custom-counter-sets-using-the-load-test-editor"></a>Nasıl yapılır: Yük Testi Düzenleyicisini kullanarak özel sayaç kümeleri ekleme

İle bir yük testi oluşturduğunuzda, **Yeni Yük Testi Sihirbazı**, bir başlangıç sayaç kümesini ekleyin. Bu, Yük testiniz için ön tanımlı sayaç kümeleri kümesini sunar.

> [!NOTE]
> Yük testlerinizi Uzak makinelerde dağıtılmışsa, denetleyici ve aracı sayaçları denetleyicisi ve aracısı için eşlenen sayaç kümeleri. Uzak makinede yük testinizde kullanma hakkında daha fazla bilgi için bkz. [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

Sayaçlarınızı yönettiğiniz **Yük Testi Düzenleyicisi**. Test zaten eklenmiş olan sayaç kümeleri görülebilir **sayaç kümeleri** düğümü yük testi. Bir yük testi oluşturduktan sonra yeni özel sayaç kümeleri ekleyebilirsiniz.

![Özel sayaç kümesi](../test/media/loadtestcustomcounter.png)

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-add-a-custom-counter-set-to-a-load-test"></a>Özel sayaç kümesi bir yük testine eklemek için

1. Bir yük testi açın.

2. Genişletin **sayaç kümeleri** düğümü. Yük testi için eklenmiş olan tüm sayaç kümeleri tarafından görülebilir.

3. Sağ **sayaç kümeleri** düğümünü seçip alt **özel sayaç kümesi Ekle**.

    > [!NOTE]
    > Sayaç kümesi gibi varsayılan bir ad verilir **Custom1**. Adı kullanarak değiştirebileceğiniz **özellikleri** penceresi. Tuşuna **F4** görüntülenecek **özellikleri** penceresi.

4. Sayaçları özel sayaç kümesi, yeni sayaç kümesini sağ tıklatın ve ardından eklemek için **Sayaç Ekle**. Sayaçları ekleme hakkında daha fazla bilgi için bkz. [nasıl yapılır: Sayaç kümelerine sayaç ekleme](../test/how-to-add-counters-to-counter-sets-using-the-load-test-editor.md).

    > [!NOTE]
    > Varolan bir sayaç kümesini sağ tıklatıp, kopyala öğesini seçip ardından onu sayaç kümeleri düğümüne yapıştırarak da özel sayaç kümesi eklemek mümkündür. Kopyalanır, ancak gerekli değildir, ek sayaçları silinebilir. Kullanarak yeni sayacın adını değiştirebilirsiniz **özellikleri** penceresi.

## <a name="see-also"></a>Ayrıca bkz.

- [Sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testi içinde belirtin.](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)
- [Yük testi çalıştırma ayarlarını yapılandırma](../test/configure-load-test-run-settings.md)