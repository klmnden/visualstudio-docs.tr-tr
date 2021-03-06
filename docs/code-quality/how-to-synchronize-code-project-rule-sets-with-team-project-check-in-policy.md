---
title: İade İlkesi ile eşitleme proje kural kümeleri
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.selecttfsruleset
ms.assetid: 9b02f934-2db6-41ec-aaff-9c31ceec2f04
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 80d13afe27eab28c88d2513b6c8be986ab1c960a
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66260845"
---
# <a name="how-to-synchronize-code-project-rule-sets-with-an-azure-devops-project-check-in-policy"></a>Nasıl yapılır: Azure DevOps projesi iade ilkesiyle kod proje kural kümelerini eşitleme

Azure DevOps projesi iade ilkesiyle kod proje için Kod Analizi ayarları, en az belirtilen kural kümesi için iade ilkesi kuralları içeren bir kural kümesi belirterek eşitleyin. Geliştirici sağlama, ad ve kural kümesi için iade ilkesi konumunu bildirebilirsiniz. Proje için Kod Analizi kuralları doğru kümesini kullandığından emin olmak için aşağıdaki seçeneklerden birini kullanabilirsiniz:

- İade İlkesi Microsoft yerleşik kural kümelerini kullanıyorsa, kod projesi için özellikleri iletişim kutusunu açın, Kod Analizi sayfayı görüntülemek ve kod projesi ayarları Kod Analizi sayfasında ayarlama kuralı seçin. Microsoft Standart kural kümelerinden Visual Studio ile otomatik olarak yüklenir, salt okunur olarak ayarlanır ve düzenlenmemelidir. Kural kümeleri düzenlenemez, yerel kural kümeleri ve ilke kuralları eşleştirmek için garanti edilir.

- İade İlkesi özel bir kural kümesini kullanıyorsa, yerel bir kopya oluşturmak için sürüm denetiminde kural kümesi dosyası üzerinde bir alma işlemi gerçekleştirin. Ardından, yerel bir konum kod projesi için Kod Analizi ayarları belirtin. Kuralları kural kümesi için iade ilkesi güncel değilse eşleştirilecek garanti edilir.

     Sürüm denetimi konumu Azure DevOps projesi kök kod projeniz gibi aynı ilişki içindeki yerel bir klasöre eşleyin, kural konumu göreli bir yol kullanılarak ayarlanır. Kod Analizi için kod proje ayarı diğer bilgisayarlara taşınabilir göreli bir yol sağlar.

- Kural için bir kod projesi için iade ilke kümesi bir kopyasını özelleştirin. Yeni Kural kümesini iade ilkesi tüm kuralları ve dahil etmek istediğiniz diğer tüm kurallar içerdiğinden emin olun. Tüm kurallar kural kümesi, kural kümesi için iade ilkesi içerdiğinden emin olmanız gerekir.

## <a name="to-specify-a-microsoft-standard-rule-set"></a>Bir Microsoft Standart kural belirtmek için ayarlayın

1. İçinde **Çözüm Gezgini**kod projesine sağ tıklayın ve ardından **özellikleri**.

2. Tıklayın **Kod Analizi**.

3. İçinde **bu kural kümesini Çalıştır** İade İlkesi kural kümesi'ni tıklatın.

## <a name="to-specify-a-custom-check-in-policy-rule-set"></a>Özel İade İlkesi kural kümesi belirtmek için

1. Gerekirse, iade ilkesi belirten kural kümesi dosyası üzerinde bir alma işlemi gerçekleştirin.

2. İçinde **Çözüm Gezgini**kod projesine sağ tıklayın ve ardından **özellikleri**.

3. Tıklayın **Kod Analizi**.

4. İçinde **bu kural kümesini Çalıştır** listesinde  **\<Gözat … >** .

5. İçinde **açık** iletişim kutusunda, İade İlkesi kural kümesi dosyası belirtin.

## <a name="to-create-a-custom-rule-set-for-a-code-project"></a>Özel bir kural oluşturmak için bir kod projesi için ayarlayın.

1. Proje Ayarları iletişim kutusu, Kod Analizi sayfasında Azure DevOps projesi iade ilkesi seçmek için daha önce bu konudaki yordamları izleyin.

2. Tıklayın **açık**.

3. Ekleyip kuralları kullanarak [kural kümesi düzenleyici](../code-quality/working-in-the-code-analysis-rule-set-editor.md).

4. Yerel bilgisayardaki bir .ruleset dosyası veya bir UNC yolu olarak değiştirilmiş kuralı kaydedin.

5. Kod projesi için özellikleri iletişim kutusunu açmak ve görüntülemek **Kod Analizi** sayfası.

6. İçinde **bu kural kümesini Çalıştır** listesinde  **\<Gözat … >** .

7. İçinde **açık** iletişim kutusunda, kural kümesi dosyası belirtin.
