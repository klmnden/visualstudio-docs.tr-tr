---
title: '5. Adım: ENTER NumericUpDown denetimleri için olay işleyicileri ekleme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 45a99a5d-c881-4298-b74d-adb481dec5ee
author: TerryGLee
ms.author: tglee
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: fae776ebe8c79947fc79f766f1abe1764df0c17a
ms.sourcegitcommit: 59c48e1e42b48ad25a4e198af670faa4d8dae370
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2019
ms.locfileid: "54204378"
---
# <a name="step-5-add-enter-event-handlers-for-the-numericupdown-controls"></a>5. Adım: ENTER NumericUpDown denetimleri için olay işleyicileri ekleme

Bu Eğitimin beşinci kısmında, ekleyeceksiniz <xref:System.Windows.Forms.Control.Enter> girmek için olay işleyicileri için sınav sorularının biraz kolay yanıtlar. Bu kodu seçin ve kaldırın. geçerli değeri her <xref:System.Windows.Forms.NumericUpDown> sınava seçer ve farklı bir değer girmeye başladıktan hemen sonra Denetim.

> [!NOTE]
> Bu konu, temel kodlama kavramları hakkındaki bir öğretici serisinin bir parçasıdır. Öğreticiye genel bakış için bkz. [öğretici 2: Zamanlı matematik testi oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md).

## <a name="to-verify-the-default-behavior"></a>Varsayılan davranışı doğrulama

1. Programınızı çalıştırın ve sınavı başlatın.

     İçinde **NumericUpDown** denetlemek için ek sorunun, imleç yanında yanıp söner **0** (sıfır).

2. Girin **3**, Denetim gösterir Not **30**.

3. Girin **5**yani **350** görünür ancak değişikliklerini **100** bir saniye sonra.

     Bu sorunu gidermeden önce neler olduğu hakkında düşünün. Neden göz önünde bulundurun **0** girdiğiniz kaybolmadığını **3** ve neden **350** değiştirilecek **100** ancak hemen.

     Bu davranış garip görünebilir ancak kodun mantığı verilen mantıklıdır. Seçeneğini belirlediğinizde **Başlat** düğmesi, kendi **etkin** özelliği **False**, ve düğme soluklaşır ve kullanılamaz. Programınız geçerli seçimi (odağı), ek sorunun NumericUpDown denetimi sonraki en düşük TabIndex değerine sahip denetime değiştirir. Kullanırken **sekmesini** anahtar bir NumericUpDown denetimine gitmek için imleci otomatik olarak girdiğiniz sayılar sol tarafındaki ve sağ tarafında görünür neden olan denetim başlangıcında konumlandırıldı. Bir sayı belirtirseniz değerinden daha yüksek olan **MaximumValue** girdiğiniz sayı 100 olarak ayarlanmışsa özelliği, özelliğin değeriyle değiştirilir.

## <a name="to-add-an-enter-event-handler-for-a-numericupdown-control"></a>NumericUpDown denetimi için bir Enter olay işleyicisi eklemek için

1. İlk seçin **NumericUpDown** ("sum" adında) denetimi form üzerinde ve ardından **özellikleri** iletişim kutusunda **olayları** araç çubuğundaki simgeye.

   ![Özellikler araç çubuğu düğmesini olayları](media/control-properties-events.png)

   **Olayları** sekmesinde **özellikleri** iletişim kutusu (işleyebileceğiniz) formda seçtiğiniz öğenin yanıt verin olayların tümünü görüntüler. NumericUpDown denetimini seçtiğinizden, tüm etkinlikler buna ilişkindir.

2. Seçin **Enter** olay, türü `answer_Enter`ve tuşuna **Enter** anahtarı.

   ![Olay işleyicisi yöntem adı girin](media/enter-event.png)

   Toplama NumericUpDown denetimi için az önce bir Enter olay işleyicisini eklediniz ve işleyiciyi adlı **answer_Enter**.

3. Yöntem için **answer_Enter** olay işleyicisine aşağıdaki kodu ekleyin:

     [!code-vb[VbExpressTutorial3Step5_6#11](../ide/codesnippet/VisualBasic/step-5-add-enter-event-handlers-for-the-numericupdown-controls_1.vb)]
     [!code-csharp[VbExpressTutorial3Step5_6#11](../ide/codesnippet/CSharp/step-5-add-enter-event-handlers-for-the-numericupdown-controls_1.cs)]

     Bu kod karmaşık görünebilir, ancak şimdi adım adım bakarsanız anlayabilirsiniz. Önce yöntemin üstüne bakın: `object sender` C# veya `sender As System.Object` Visual Basic'te. Bu parametre gönderen olarak bilinen, olayı tetiklenmekte olan nesneye başvurur. Bu durumda gönderen nesnesi NumericUpDown denetimidir. Bu nedenle, yöntemin ilk satırında gönderenin herhangi genel amaçlı nesne olmadığının olarak NumericUpDown denetimi değildir belirtin. (Her NumericUpDown denetimi bir nesnedir ancak her nesne bir NumericUpDown denetimidir.) NumericUpDown denetimine **answerBox** Bu yöntemde tüm formunda NumericUpDown denetimleri için kullanılacağından yalnızca toplama NumericUpDown denetimi. Bu yöntemde answerBox değişkeni bildirdiğinizden, kapsamı yalnızca bu yönteme uygulanır. Diğer bir deyişle, değişken, yalnızca bu yöntem içinde kullanılabilir.

     Sonraki satır answerBox başarıyla dönüştürülüp dönüştürülmediğini doğrular (bir nesneden bir NumericUpDown denetimine atama). Dönüştürme başarısız oldu, değişkenin değerini gerekir `null` (C#) veya `Nothing` (Visual Basic). Üçüncü satır NumericUpDown denetiminde görünen yanıt uzunluğu alır ve geçerli değeri bu uzunluğa göre denetim dördüncü satırı seçer. Artık, sınava giren denetimi seçtiğinde, Visual Studio bu da geçerli yanıtın seçilmesine neden olur. Bu olay tetiklenir. Sınava giren farklı bir yanıt girmeye başladıktan hemen sonra önceki yanıt temizlenir ve yeni yanıt ile değiştirilir.

4. İçinde **Windows Form Tasarımcısı**, fark seçin **NumericUpDown** denetimi.

5. İçinde **olayları** sayfasının **özellikleri** iletişim kutusu, aşağı kaydırın **Enter** olay satırın sonundaki aşağı açılır oku seçin ve ardından `answer_Enter`eklediğiniz olay işleyicisi.

6. Ürün ve bölüm NumericUpDown denetimleri için önceki adımı yineleyin.

7. Programınızı kaydedin ve ardından çalıştırın.

     Seçeneğini belirlediğinizde bir **NumericUpDown** denetimi, mevcut değer otomatik olarak seçilir ve farklı bir değer girmeye başladığınızda seçilip silinir.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz: [adım 6: Çıkarma problemi ekleme](../ide/step-6-add-a-subtraction-problem.md).

- Önceki öğretici adımına dönmek için bkz: [4. adım: CheckTheAnswer() yöntemi ekleme](../ide/step-4-add-the-checktheanswer-parens-method.md).
