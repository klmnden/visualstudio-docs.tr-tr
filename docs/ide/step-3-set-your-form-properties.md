---
title: '3\. Adım: Form özelliklerinizi ayarlama'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 634ef037-1525-48c8-ac7f-abf04be69376
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4e2742103585321b4f752a74e53253409e449bcf
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68918810"
---
# <a name="step-3-set-your-form-properties"></a>3\. Adım: Form özelliklerinizi ayarlama
Daha sonra, formunuzun görünüşünü değiştirmek için **Özellikler** penceresini kullanın.

![video](../data-tools/media/playvideo.gif)bağlantısı bu konunun video sürümü için bkz [. öğretici 1: Visual Basic-video 1](http://go.microsoft.com/fwlink/?LinkId=205209) veya [öğretici 1 ' de bir resim Görüntüleyicisi oluşturun: Video 1 C# ](http://go.microsoft.com/fwlink/?LinkId=205199)' de bir resim görüntüleyici oluşturun. Bu videolar, Visual Studio 'nun önceki bir sürümünü kullanır, bu nedenle bazı menü komutlarında ve diğer kullanıcı arabirimi öğelerinde küçük farklılıklar vardır. Ancak, kavramlar ve yordamlar Visual Studio 'nun geçerli sürümünde benzer şekilde çalışır.

## <a name="to-set-your-form-properties"></a>Form özelliklerinizi ayarlamak için

1. **Windows Form Tasarımcısı**baktığınızdan emin olun. Visual Studio tümleşik geliştirme ortamında (IDE), **Form1.cs [Design]** (ya da **Form1. vb [Design]** ) sekmesini seçerek Visual Basic).

2. Seçmek için **Form1** form içinde herhangi bir yeri seçin. Şimdi form özelliklerini göstermeli **Özellikler** penceresine bakın. Formlarda çeşitli özellikler vardır. Örneğin, ön plan ve arka plan rengini, formun üstünde görünen başlık metnini, formun boyutunu ve diğer özellikleri ayarlayabilirsiniz.

   > [!NOTE]
   > **Özellikler** penceresi görünmezse, araç çubuğunda kare **ayıklamayı Durdur** düğmesini seçerek programınızı durdurun veya yalnızca pencereyi kapatın. Program durdurulmuşsa ve yine de **Özellikler** penceresini görmüyorsanız, menü çubuğunda**Özellikler penceresini** **görüntüle** > ' yi seçin.

3. Form seçildikten sonra, **Özellikler** penceresinde **Text** özelliğini bulun. Listenin nasıl sıralandığına bağlı olarak aşağı kaydırmanız gerekebilir. **Metin**' i seçin, **resim görüntüleyici**yazın ve ardından **ENTER**' u seçin.  Formunuz artık başlık çubuğunda metin **resmi görüntüleyicisine** sahip olmalıdır ve **Özellikler** penceresi aşağıdaki resme benzer görünmelidir.

    ![Özellikler penceresi](../ide/media/express_edittextproperty.png)
   **Özellikler** penceresi

   > [!NOTE]
   > Özellikler, **kategorilere ayrılmış** veya **alfabetik** bir görünüme göre sıralanabilir. **Özellikler** penceresindeki düğmeleri kullanarak bu iki görünüm arasında geçiş yapabilirsiniz. Bu öğreticide, **alfabetik** görünüm aracılığıyla özellikleri bulmak daha kolay.

4. **Windows Form Tasarımcısı**'e geri dönün. Formun sağ alt kısmındaki küçük beyaz kare olan ve aşağıdaki gibi görünen formun sağ alt sürükleme tutamacını seçin.

    ![Sürükle tutamacı](../ide/media/express_bottomrt_drag.png) sürükle tutamacı

    Formu daha geniş ve biraz uzun olacak şekilde yeniden boyutlandırmak için tutamacı sürükleyin.

5. **Özellikler** penceresine bakın ve **Boyut** özelliğinin değiştiğini unutmayın. Formu her yeniden boyutlandırışınızda **size** özelliği değişir. Formun tutamacını, yaklaşık **550, 350** (tam olması gerekmez) form boyutuyla yeniden boyutlandırmak için, bu proje için iyi bir şekilde çalışacak şekilde sürüklemeyi deneyin. Alternatif olarak, değerleri doğrudan **Boyut** özelliğine girebilir ve ardından **ENTER** tuşunu seçebilirsiniz.

6. Programınızı yeniden çalıştırın. Programınızı çalıştırmak için aşağıdaki yöntemlerden herhangi birini kullanacağınızı unutmayın.

   - **F5** tuşunu seçin.

   - Menü çubuğunda **hata** > **ayıklamayı Başlat hata**Ayıkla ' yı seçin.

   - Araç çubuğunda, aşağıdaki gibi görünen **hata ayıklamayı Başlat** düğmesini seçin.

      ![Hata ayıklamayı Başlat araç](../ide/media/express_icondebug.png)
     çubuğu düğmesi**başlatma hata ayıklama** araç çubuğu düğmesi

     Daha önce olduğu gibi, IDE de programınızı oluşturup çalıştırır ve bir pencere görüntülenir.

7. Bir sonraki adıma geçmeden önce, IDE çalışırken programınızı değiştirmenize izin vermediğinden programınızı durdurun. Programınızı durdurmak için aşağıdaki yöntemlerden herhangi birini kullanacağınızı unutmayın.

   - Araç çubuğunda **hata ayıklamayı Durdur** düğmesini seçin.

   - Menü çubuğunda **hata** > **ayıklamayı Durdur hata**Ayıkla ' yı seçin.

   - **Form1** penceresinin üst köşesindeki **X** düğmesini seçin.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 4. Adım: Bir TableLayoutPanel denetimiyle](../ide/step-4-lay-out-your-form-with-a-tablelayoutpanel-control.md)formunuzu düzenleyin.

- Önceki öğretici adımına dönmek için bkz [. 2. Adım: Programınızı](../ide/step-2-run-your-program.md)çalıştırın.
