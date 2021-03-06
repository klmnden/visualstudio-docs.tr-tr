---
title: Özel Kod Analizi kural kümesi oluşturma
ms.date: 11/02/2018
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.addremoverulesets
helpviewer_keywords:
- rule sets
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f2f642ea8e41e4a9ccf2b35f432df528fc5e81d0
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65676556"
---
# <a name="customize-a-rule-set"></a>Bir kural kümesi özelleştirme

Kod Analizi için belirli proje gereksinimlerini karşılamak için özel bir kural oluşturabilirsiniz.

## <a name="create-a-custom-rule-set-from-an-existing-rule-set"></a>Var olan bir kural kümesinden özel bir kural oluşturun

Özel bir kural oluşturmak için yerleşik bir kural kümesi açabilirsiniz **kural kümesi düzenleyici**. Burada, ekleme veya kaldırma belirli kurallar ve kural ihlal edildiğinde gerçekleşen eylemi değiştirebilirsiniz&mdash;Örneğin, bir uyarı veya hata gösterir.

1. İçinde **Çözüm Gezgini**, projeye sağ tıklayın ve ardından **özellikleri**.

2. Üzerinde **özellikleri** sayfaları, select **Kod Analizi** sekmesi.

3. İçinde **bu kural kümesini Çalıştır** aşağı açılan listesinde, aşağıdakilerden birini yapın:

   - Özelleştirmek istediğiniz kural kümesi seçin.

     \- veya -

   - Seçin  **\<Gözat … >** mevcut bir kuralı kümesini belirlemek için listesinde değil.

4. Seçin **açık** kuralları kural kümesi Düzenleyicisi'nde görüntülemek için.

> [!NOTE]
> Bir .NET Core veya .NET Standard projesi varsa, işlemi biraz farklı olmadığından hiçbir **Kod Analizi** özellik sekmesi. Adımlarını izleyin [projenize ve etkin kural kümesi olarak ayarladığınızda önceden tanımlanmış bir kuralı kopyalamak](analyzer-rule-sets.md). Bir kural kümesi kopyaladıktan sonra [kural kümesi Düzenleyicisi Visual Studio Düzenle](working-in-the-code-analysis-rule-set-editor.md) ondan açarak **Çözüm Gezgini**.

## <a name="create-a-new-rule-set"></a>Yeni bir kural kümesi oluşturma

Yeni bir kural kümesi dosyasını oluşturabilirsiniz **yeni dosya** iletişim:

1. Seçin **dosya** > **yeni** > **dosya**, veya basın **Ctrl**+**N**.

2. İçinde **yeni dosya** iletişim kutusunda **genel** solda, kategori seçip **Kod Analizi kural kümesi**.

3. **Aç**'ı seçin.

   Yeni *.ruleset* dosyası kural kümesi Düzenleyicisi'nde açılır.

## <a name="create-a-custom-rule-set-from-multiple-rule-sets"></a>Birden çok kural kümelerinden özel bir kural oluşturun

> [!NOTE]
> Aşağıdaki yordam yoksa .NET Core projeleri için geçerli değildir bir **Kod Analizi** özellik sekmesi.

1. İçinde **Çözüm Gezgini**, projeye sağ tıklayın ve ardından **özellikleri**.

2. Üzerinde **özellikleri** sayfaları, select **Kod Analizi** sekmesi.

3. Seçin  **\<birden çok kural kümeleri... seçin >** gelen **bu kural kümesini Çalıştır**.

4. İçinde **Ekle veya Kaldır kural kümeleri** kural ayarlar seçin iletişim kutusunda, istediğiniz yeni kural kümesinde eklenecek.

   ![Ekleme veya kaldırma kural kümelerini iletişim kutusu](media/add-remove-rule-sets.png)

5. Seçin **Kaydet**, için bir ad girin *.ruleset* dosya ve ardından **Kaydet**.

   Yeni kural kümesi seçili **bu kural kümesini Çalıştır** listesi.

6. Seçin **açın** yeni kural kural kümesi Düzenleyicisi'nde kümesi açın.

## <a name="rule-precedence"></a>Kural önceliği

- Aynı kural listelenen iki veya daha fazla kez farklı önem dereceleri ile bir kural olarak, derleyici bir hata oluşturur. Örneğin:

   ```xml
   <RuleSet Name="Rules for ClassLibrary21" Description="Code analysis rules for ClassLibrary21.csproj." ToolsVersion="15.0">
     <Rules AnalyzerId="Microsoft.Analyzers.ManagedCodeAnalysis" RuleNamespace="Microsoft.Rules.Managed">
       <Rule Id="CA1021" Action="Warning" />
       <Rule Id="CA1021" Action="Error" />
     </Rules>
   </RuleSet>
   ```

- Aynı kural listelenen iki veya daha çok kez bir kural kümesi içinde *aynı* önem derecesi, aşağıdaki uyarıyı karşılaşabilirsiniz **hata listesi**:

   **CA0063: Kural kümesi dosyası yüklenemedi. '\[,] .ruleset ' veya onun bağlantılı kural birini dosyaları ayarlayın. Dosya, kural kümesi şemasına uymuyor.**

- Kural kümesini kullanarak bir alt kural içeriyorsa bir **INCLUDE** etiketi ve alt ve üst kural kümelerini iki listesinden aynı kural ancak farklı önem dereceleri ile ardından üst kural kümesindeki önem öncelik kazanır. Örneğin:

   ```xml
   <!-- Parent rule set -->
   <?xml version="1.0" encoding="utf-8"?>
   <RuleSet Name="Rules for ClassLibrary21" Description="Code analysis rules for ClassLibrary21.csproj." ToolsVersion="15.0">
     <Include Path="classlibrary_child.ruleset" Action="Default" />
     <Rules AnalyzerId="Microsoft.Analyzers.ManagedCodeAnalysis" RuleNamespace="Microsoft.Rules.Managed">
       <Rule Id="CA1021" Action="Warning" /> <!-- Overrides CA1021 severity from child rule set -->
     </Rules>
   </RuleSet>

   <!-- Child rule set -->
   <?xml version="1.0" encoding="utf-8"?>
   <RuleSet Name="Rules from child" Description="Code analysis rules from child." ToolsVersion="15.0">
     <Rules AnalyzerId="Microsoft.Analyzers.ManagedCodeAnalysis" RuleNamespace="Microsoft.Rules.Managed">
       <Rule Id="CA1021" Action="Error" />
     </Rules>
   </RuleSet>
   ```

## <a name="name-and-description"></a>Ad ve açıklama

Düzenleyicide açık olan bir kural kümesi görünen adını değiştirmek için **özellikleri** penceresini seçerek **görünümü** > **Özellikler penceresi** menü çubuğundaki. Görünen ad girin **adı** kutusu. Ayrıca kural kümesi için bir açıklama girebilirsiniz.

## <a name="next-steps"></a>Sonraki adımlar

Bir kural kümesi olduğuna göre sonraki adım, ekleme veya kaldırma kuralları veya önem derecesini kural ihlalleri değiştirme kuralları Özelleştir sağlamaktır.

> [!div class="nextstepaction"]
> [Kuralları kural kümesi Düzenleyici'sini değiştirme](../code-quality/working-in-the-code-analysis-rule-set-editor.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Yönetilen kod projesi için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-a-managed-code-project.md)
- [Kod çözümleme kural kümesi başvurusu](../code-quality/rule-set-reference.md)