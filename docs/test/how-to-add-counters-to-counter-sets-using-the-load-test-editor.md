---
title: Yük testi için sayaç kümelerine sayaç ekleme
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- counters, counter sets
- counter sets
- load tests, counter sets
ms.assetid: e17d0e71-f982-4fc1-a2df-a1065d37473d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.openlocfilehash: 29ca2518e56adf95d11fcaf750d8ddd9aa15a3f9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54916520"
---
# <a name="how-to-add-counters-to-counter-sets-using-the-load-test-editor"></a>Nasıl yapılır: Yük Testi Düzenleyicisini kullanarak sayaç kümelerine sayaç ekleme

İle bir yük testi oluşturduğunuzda, **Yük Testi Sihirbazı**, bir başlangıç sayaç kümesini ekleyin. Bu, Yük testiniz için ön tanımlı sayaç kümeleri kümesini sunar. Daha fazla bilgi için [sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testinde belirtin](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

> [!NOTE]
> Yük testlerinizi Uzak makinelerde dağıtılmışsa, denetleyici ve aracı sayaçları denetleyicisi ve aracısı için eşlenen sayaç kümeleri. Uzak makinede yük testinizde kullanma hakkında daha fazla bilgi için bkz. [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).

Sayaçlarınızı yönettiğiniz **Yük Testi Düzenleyicisi**. Test zaten eklenmiş olan sayaç kümeleri görülebilir **sayaç kümeleri** düğümü yük testi. Bir yük testi oluşturduktan sonra var olan sayaç kümelerine sayaç yeni sayaçları ekleyebilirsiniz.

## <a name="to-add-counters-to-a-counter-set"></a>Sayaç için bir sayaç kümesi eklemek için

1.  Bir yük testi açın.

2.  Genişletin **sayaç kümeleri** düğümü. Yük testi için eklenmiş olan tüm sayaç kümeleri tarafından görülebilir.

    > [!NOTE]
    > Yük testi hiyerarşi ağacı de içeren **çalıştırma ayarları** düğümü. Bu düğümü içeren **sayaç kümesi eşlemeleri** düğümü, bu bilgisayarlara eşlenmiş sayaç kümeleri ve tüm bilgisayarları gösterir.

3.  Var olan bir sayaç kümesini sağ tıklatın ve ardından **Sayaç Ekle**.

     **Performans sayaçlarını Seç** iletişim kutusu görüntülenir.

4.  İçinde **bilgisayar** açılan eşlemek istediğiniz bilgisayarın adını yazın. Alternatif olarak, bilgisayarlardan biri aşağı açılan listeden seçin.

    > [!NOTE]
    > Performans verileri toplanmadan önce bir bilgisayara sayaç kümeleri eşlenmelidir için performans verilerini toplamak bir bilgisayar belirtmeniz gerekir.

5.  Seçin bir **performans kategorisi** performans veriler sayaçlarının kategorileri filtrelemek için. İki sütun hangi performans sayaçlarını seçmek verileri görürsünüz.

    > [!NOTE]
    > Bazı sayaç kategorileri örneği de seçmeniz gerekir. Örneğin, bir SQL sayaç seçerseniz, olabilir çünkü birden fazla hedef bilgisayarda yüklü SQL örneğini bir SQL örneği seçmeniz gerekir.

6.  Bir sayacı ve özel sayaç kümenize eklemek için örneği seçin.

     \- veya -

     Seçin **tüm sayaçları** radyo düğmesi kullanılabilir tüm sayaçları seçin.

7.  **Tamam**’ı seçin.

    > [!NOTE]
    > Sayaç kümesi varolan sayacı veya sayaç kategorisini Kopyala'yı seçip seçerek sayaçlar eklemek mümkündür ve ardından onu farklı sayaç yapıştırma düğüm kümesi. Kopyalanır, ancak gerekli değildir, ek sayaçları silinebilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Sayaç kümelerini ve eşik kurallarını bilgisayarlar için bir yük testi içinde belirtin.](../test/specify-counter-sets-and-threshold-rules-for-load-testing.md)
- [Yük testi çalıştırma ayarlarını yapılandırma](../test/configure-load-test-run-settings.md)