---
title: Yük testi için bir eşik kuralı ekleme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, monitoring
- load tests, thresholds
- load tests, analyzing
- thresholds in load tests
ms.assetid: 3d8fac8f-426f-4155-9ced-f7cd4c79792c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.openlocfilehash: e06ed07ba37b6f9c6442c69edab86aaf0f10e9de
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971107"
---
# <a name="how-to-add-a-threshold-rule-using-the-load-test-editor"></a>Nasıl yapılır: Yük Testi Düzenleyicisini kullanarak bir eşik kuralı ekleme

Yük testlerindeki eşik kuralları, bir performans sayacı değeri bir sabit değer ya da başka bir performans sayacı değeri ile karşılaştırın.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="to-add-a-threshold-rule"></a>Eşik kuralı ekleme

1.  Bir yük testi açın.

2.  Yük Testi Düzenleyicisi'nde genişletin **sayaç kümeleri** düğümü.

3.  Birini genişletin **sayaç kategorileri** sayaç kümelerinden birinde. Örneğin, seçebileceğiniz **YüklemeTesti**. Düğümünü genişletin.

4.  Örneğin, sayaçları birine sağ tıklayın **kullanıcı yükü**altında **YüklemeTesti**. Seçin **eşik kuralı ekleme**.

     **Eşik Kuralı Ekle** iletişim kutusu görüntülenir.

5.  İki kural türlerinden birini seçebilirsiniz: **Sabiti Karşılaştır** ve **karşılaştırma sayaç**. Uygun türünü seçin ve şu değerleri ayarlayın.

    > [!NOTE]
    > Ayarlama **aşarsa uyar** özelliğini **True** bir Eşiği aşan bir sorun olduğunu belirtmek için veya **False** eşiğin altında kalan bir sorun olduğunu belirtmek için.

## <a name="see-also"></a>Ayrıca bkz.

- [Eşik kuralı ihlallerini çözümleme](../test/analyze-threshold-rule-violations-in-load-tests.md)
- [Sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testi içinde belirtin.](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)
- [Yük testi sonuçlarını çözümleme](../test/analyze-load-test-results-using-the-load-test-analyzer.md)
