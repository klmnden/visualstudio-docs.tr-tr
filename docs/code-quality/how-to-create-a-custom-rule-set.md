---
title: Visual Studio'da bir özel kod analizi kural oluşturma
ms.date: 04/04/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.addremoverulesets
helpviewer_keywords:
- Development Edition, rule sets
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: dce43c02f4976b51bab61a48f615fb0307102fc7
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49884192"
---
# <a name="customize-a-rule-set"></a>Bir kural kümesi özelleştirme

Kod Analizi için belirli proje gereksinimlerini karşılamak için özel bir kural oluşturabilirsiniz.

## <a name="create-a-custom-rule-set"></a>Özel kural kümesi oluşturma

Özel bir kural oluşturmak için yerleşik bir kural kümesi açabilirsiniz **kural kümesi düzenleyici**. Burada, ekleme veya kaldırma belirli kurallar ve kural ihlal edildiğinde gerçekleşen eylemi değiştirebilirsiniz&mdash;Örneğin, bir uyarı veya hata gösterir.

1. İçinde **Çözüm Gezgini**, projeye sağ tıklayın ve ardından **özellikleri**.

2. Üzerinde **özellikleri** sayfaları, select **Kod Analizi** sekmesi.

3. İçinde **bu kural kümesini Çalıştır** aşağı açılan listesinde, aşağıdakilerden birini yapın:

   - Özelleştirmek istediğiniz kural kümesi seçin.

     \- veya -

   - Seçin  **\<Gözat … >** mevcut bir kuralı kümesini belirlemek için listesinde değil.

4. Seçin **açık** kuralları kural kümesi Düzenleyicisi'nde görüntülemek için.

Öğesinden yeni bir kural kümesi dosyası da oluşturabilirsiniz **yeni dosya** iletişim:

1. Seçin **dosya** > **yeni** > **dosya**, veya basın **Ctrl**+**N**.

2. İçinde **yeni dosya** iletişim kutusunda **genel** solda, kategori seçip **Kod Analizi kural kümesi**.

3. **Aç**'ı seçin.

   Yeni *.ruleset* dosyası kural kümesi Düzenleyicisi'nde açılır.

### <a name="create-a-custom-rule-set-from-multiple-rule-sets"></a>Birden çok kural kümelerinden özel bir kural oluşturun

1. Çözüm Gezgini'nde projeye sağ tıklayın ve ardından **özellikleri**.

2. Üzerinde **özellikleri** sayfaları, select **Kod Analizi** sekmesi.

3. Seçin  **\<birden çok kural kümeleri... seçin >** gelen **bu kural kümesini Çalıştır**.

4. İçinde **Ekle veya Kaldır kural kümeleri** kural ayarlar seçin iletişim kutusunda, istediğiniz yeni kural kümesinde eklenecek.

   ![Ekleme veya kaldırma kural kümelerini iletişim kutusu](media/add-remove-rule-sets.png)

5. Seçin **Kaydet**, için bir ad girin *.ruleset* dosya ve ardından **Kaydet**.

   Yeni kural kümesi seçili **bu kural kümesini Çalıştır** listesi.

6. Seçin **açın** yeni kural kural kümesi Düzenleyicisi'nde kümesi açın.

## <a name="name-and-description"></a>Ad ve açıklama

Düzenleyicide açık olan bir kural kümesi görünen adını değiştirmek için **özellikleri** penceresini seçerek **görünümü** > **Özellikler penceresi** menü çubuğundaki. Görünen ad girin **adı** kutusu. Ayrıca kural kümesi için bir açıklama girebilirsiniz.

## <a name="next-steps"></a>Sonraki adımlar

Bir kural kümesi olduğuna göre sonraki adım, ekleme veya kaldırma kuralları veya önem derecesini kural ihlalleri değiştirme kuralları Özelleştir sağlamaktır.

> [!div class="nextstepaction"]
> [Kuralları kural kümesi Düzenleyici'sini değiştirme](../code-quality/working-in-the-code-analysis-rule-set-editor.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Yönetilen Kod Projesi İçin Kod Çözümlemesini Yapılandırma](../code-quality/how-to-configure-code-analysis-for-a-managed-code-project.md)
- [Kod çözümleme kural kümesi başvurusu](../code-quality/rule-set-reference.md)