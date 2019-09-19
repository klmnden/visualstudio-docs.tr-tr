---
title: '4\. Adım: Her etikete bir tıklama olayı işleyicisi ekleme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
dev_langs:
- CSharp
- vb
ms.assetid: 16bdbc7c-4129-411d-bace-f4a3e5375975
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 705ddc48e37c557a1d0c77fc3f1ca82cbb3995e7
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71118757"
---
# <a name="step-4-add-a-click-event-handler-to-each-label"></a>4\. Adım: Her etikete bir tıklama olayı işleyicisi ekleme

Eşleştirme oyunu aşağıdaki gibi çalışır:

1. Oyuncu gizli simge içeren karelerden birini seçtiğinde, program simge rengini siyaha dönüştürerek bu simgeyi oyuncuya gösterir.

2. Oyuncu daha sonra başka bir gizli simge seçer.

3. Simgeler eşleşirse görünür olarak kalırlar. Aksi takdirde iki simge de tekrar gizlenir.

   Programınızın bu şekilde çalışmasını sağlamak için, seçilen etiketin rengini değiştiren bir <xref:System.Windows.Forms.Control.Click> olay işleyicisi ekleyin.

## <a name="to-add-a-click-event-handler-to-each-label"></a>Her etikete bir tıklama olayı işleyicisi eklemek için

1. **Windows Form Tasarımcısı**formunu açın. **Çözüm Gezgini**' de *Form1.cs* veya *Form1. vb*öğesini seçin. Menü çubuğunda **Görünüm** > **Tasarımcısı**' nı seçin.

2. İlk etiket denetimini belirleyip seçin. Daha sonra, seçmek için diğer etiketlerin her birini seçerken **CTRL** tuşunu basılı tutun. Her etiketin seçildiğinden emin olun.

3. Özellikler **penceresinde** **Olaylar** sayfasını görüntülemek için **Özellikler** penceresindeki araç çubuğundan **Olaylar** düğmesini seçin. **Click** olayına aşağı kaydırın ve aşağıdaki resimde gösterildiği gibi kutuya **label_Click** girin.

     ![Tıklama olayını gösteren Özellikler penceresi](../ide/media/express_labelclick.png)

4. **ENTER** tuşunu seçin. IDE, koda çağrılan `Click` `label_Click()` bir olay işleyicisi ekler ve formdaki her etikete takar.

5. Kodun geri kalanını aşağıdaki gibi doldurun:

     [!code-csharp[VbExpressTutorial4Step2_3_4#4](../ide/codesnippet/CSharp/step-4-add-a-click-event-handler-to-each-label_1.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#4](../ide/codesnippet/VisualBasic/step-4-add-a-click-event-handler-to-each-label_1.vb)]

    > [!NOTE]
    > Kodu el ile girmek yerine `label_Click()` kod bloğunu kopyalayıp yapıştırırsanız, var olan `label_Click()` kodun değiştirilmesini unutmayın. Aksi takdirde, yinelenen bir kod bloğu ile karşı karşıya kalırsınız.

    > [!NOTE]
    > Olay işleyicisinin en `object sender` üstünde, [öğretici 2 ' de kullanılan bir tane olarak tanınabilir: Süreli bir matematik testi](../ide/tutorial-2-create-a-timed-math-quiz.md) öğreticisi oluşturun. Tek bir olay işleyicisi yöntemine farklı etiket denetimi tıklamadıklarından, aynı yöntem kullanıcının seçtiği etiketle aynı şekilde çağrılır. Olay işleyicisi yönteminin hangi etiketin seçili olduğunu bilmesi gerekir, bu nedenle etiket denetimini tanımlamak için adı `sender` kullanır. Yöntemin ilk satırı programa yalnızca genel bir nesne değil, özellikle bir etiket denetimi olduğunu ve etiketin özelliklerine ve yöntemlerine erişmek için adı `clickedLabel` kullandığını söyler.

     Bu yöntem ilk olarak bir `clickedLabel` nesneden bir etiket denetimine başarıyla dönüştürülüp dönüştürülmediğini denetler. Başarısız olursa, `null` (C#) veya `Nothing` (Visual Basic) değerine sahiptir ve yöntemdeki kodun geri kalanını yürütmek istemezsiniz. Sonra, yöntemi etiketin **ForeColor** özelliğini kullanarak seçilen etiketin metin rengini denetler. Etiketin metin rengi siyah ise, simge zaten seçilmiş ve yöntem bitmiş demektir. `return` (Deyimin şunları yapar: Programın yöntemi yürütmeyi durdurmasını söyler.) Aksi takdirde simge seçilmemiş demektir ve dolayısıyla program etiketin metin rengini siyah olarak değiştirir.

6. Menü çubuğunda, devam etmek için **Dosya** > **Tümünü Kaydet** ' i seçin ve ardından menü çubuğunda **Hata Ayıkla** > **Başlat hata ayıklama Başlat** ' ı seçerek programınızı çalıştırın. Mavi arka planlı boş bir form görmeniz gerekir. Formdaki hücrelerden herhangi birini seçtiğinizde, simgelerden birinin görünür hale gelmesi gerekir. Formda farklı yerler seçmeye devam edin. Siz simgeleri seçtikçe görünmeleri gerekir.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 5. Adım: Etiket başvuruları](../ide/step-5-add-label-references.md)ekleyin.

- Önceki öğretici adımına dönmek için bkz [. Adım 3: Her etikete](../ide/step-3-assign-a-random-icon-to-each-label.md)rastgele bir simge atayın.
