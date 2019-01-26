---
title: '6. Adım: Zamanlayıcı ekleme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 09e7930b-cab6-4a22-9a6f-72e23f489585
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab5b1a83c377b58bd42f03e3898243b3e956e31b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55016371"
---
# <a name="step-6-add-a-timer"></a>6. Adım: Zamanlayıcı ekleme
Ardından, eklediğiniz bir <xref:System.Windows.Forms.Timer> eşleştirme oyunu denetimi. Zamanlayıcı belirtilen milisaniye sayısı kadar bekler ve ardından olarak adlandırılan bir olayı tetikler bir *değer çizgisi*. Bu olay, bir eylemi başlatmak veya eylemi düzenli aralıklarla yinelemek için kullanışlıdır. Bu durumda, oyuncuların iki simge seçmesini sağlamak ve simgeler eşleşmez ise, kısa bir süre sonra bu iki simgeyi yeniden gizlemek için bir zamanlayıcı kullanacaksınız.

## <a name="to-add-a-timer"></a>Zamanlayıcı eklemek için

1.  Araç kutusundan gelen **Windows Form Tasarımcısı**, seçin **Zamanlayıcı** (içinde **bileşenleri** kategori) ve ardından **Enter** anahtarı veya Zamanlayıcı forma bir zamanlayıcı denetimi eklemek için çift tıklayın. Adlı Zamanlayıcı simgesinin **Süreölçer1**, formun altındaki bir alanda aşağıdaki resimde gösterildiği gibi görünmesi gerekir.

     ![Zamanlayıcı](../ide/media/express_timer.png)
**Zamanlayıcı**

    > [!NOTE]
    >  Araç kutusu boş ise, araç kutusunu açmadan önce formun arkasındaki kodu değil de, form tasarımcısını seçtiğinizden emin olun.

2.  Seçin **Süreölçer1** Zamanlayıcıyı seçmek için simge. İçinde **özellikleri** penceresi, Özellikler olayları görüntüleme alanından anahtar. Ardından Zamanlayıcının **aralığı** özelliğini **750**, ancak kendi **etkin** özelliğini **False**. **Aralığı** özelliği Zamanlayıcı arasında beklenecek süreyi belirten *ticks*, veya ne zaman tetikleyeceğini kendi <xref:System.Windows.Forms.Timer.Tick> olay. 750 değeri zamanlayıcıya, Tick olayını tetiklemeden önce saniyenin dörtte üçü kadar (750 milisaniye) beklemesini bildirir. Sizi ararız <xref:System.Windows.Forms.Timer.Start> yalnızca oyuncu ikinci etiketi seçtikten sonra zamanlayıcıyı başlatmak için yöntemi.

3.  Zamanlayıcıyı seçmek denetim simgesini **Windows Form Tasarımcısı** seçip **Enter** anahtar ya da boş bir Tick olayı işleyicisi eklemek için zamanlayıcıya çift tıklayın. Kodu aşağıdaki kodla değiştirin ya da aşağıdaki kodu olay işleyicisine el ile girin.

     [!code-csharp[VbExpressTutorial4Step6#7](../ide/codesnippet/CSharp/step-6-add-a-timer_1.cs)]
     [!code-vb[VbExpressTutorial4Step6#7](../ide/codesnippet/VisualBasic/step-6-add-a-timer_1.vb)]

     Tick olayı işleyicisi üç şeyi yapar: İlk olarak, çağırarak Zamanlayıcının çalışmadığından emin olur <xref:System.Windows.Forms.Timer.Stop> yöntemi. İki başvuru değişkeni kullanıyorsa `firstClicked` ve `secondClicked`, oyuncunun seçtiği iki etiketin simgelerini yeniden görünmez yapmak için. Son olarak, sıfırlar `firstClicked` ve `secondClicked` başvuru değişkenlerini `null` Visual C# ve `Nothing` Visual Basic'te. Programın kendini sıfırlama şekli olması nedeniyle bu adım önemlidir. Bunu hiçbirini izlememektedir anda <xref:System.Windows.Forms.Label> denetimleri ve oyuncunun yeniden bir etiket seçmesi için hazır.

    > [!NOTE]
    >  Bir zamanlayıcı nesnesi olan bir `Start()` Zamanlayıcıyı başlatan bir yöntemi ve bir `Stop()` yöntemi. Zamanlayıcının ayarlandığında **etkin** özelliğini **True** içinde **özellikleri** penceresinde başladıktan program başlar başlamaz yolunda. Ancak çıktığınızda ayarlı olarak **False**, çağrılıncaya kadar işlemeye başlamaz kendi `Start()` yöntemi çağrılır. Normalde, bir Zamanlayıcının Tick olayını tekrar tekrar kullanarak tetiklemeden **aralığı** saat döngüleri arasında kaç milisaniye belirlemek için özellik. Fark etmiş olabilirsiniz nasıl Zamanlayıcının `Stop()` Tick olayı içinde yöntemi çağrılır. Zamanlayıcıyı koyar *tek sefer moduna*, yani `Start()` yöntemi çağrıldığında, belirtilen aralık kadar bekleyip, tek bir Tick olayını tetikler ve sonra durur.

4.  Zamanlayıcıyı iş başında görmek için kod düzenleyicisine gidin ve üst ve alt için aşağıdaki kodu ekleyin `label_Click()` olay işleyicisi yöntemi. (Ekliyorsunuz bir `if` deyimi üst ve alt kısmına; üç deyimi yöntemin geri kalanı aynı kalır.)

     [!code-csharp[VbExpressTutorial4Step6#8](../ide/codesnippet/CSharp/step-6-add-a-timer_2.cs)]
     [!code-vb[VbExpressTutorial4Step6#8](../ide/codesnippet/VisualBasic/step-6-add-a-timer_2.vb)]

     Yönteminin üst kısmına kodu değerini kontrol ederek Zamanlayıcının başlatılıp başlatılmadığını denetler **etkin** özelliği. Bu şekilde oyuncunun seçtiği ilk ve ikinci etiket denetimleri ve Zamanlayıcı başlarsa, üçüncü bir etiket seçildiğinde hiçbir şey olmaz.

     Kod yöntemi ayarlar altındaki `secondClicked` başvuru değişkenini oyuncunun seçtiği ve ardından bu etiketin simge rengini siyaha görünür yapmak için ayarlar ikinci etiket denetimini izlemek için. Daha sonra, 750 milisaniye bekler ve tek bir Tick olayı tetiklemesi için zamanlayıcıyı tek sefer modunda başlatır. Zamanlayıcının Tick olayı işleyicisi iki simgeyi de gizler ve sıfırlar `firstClicked` ve `secondClicked` başvuru değişkenlerini form oyuncunun başka bir simge çifti seçmesine hazır olması.

5.  Programınızı kaydedin ve çalıştırın. Bir simge seçin; bu simge görünür duruma gelir.

6.  Başka bir simge seçin. Kısa bir süre görünür ve sonra iki simge birden kaybolur. Bunu birçok kez tekrar edin. Form artık, seçtiğiniz birinci ve ikinci simgeleri takip ediyor ve simgelerin kaybolmasını sağlamadan önce duraklamak için zamanlayıcıyı kullanıyor.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [adım 7: Çiftleri görünür kılma](../ide/step-7-keep-pairs-visible.md).

-   Önceki öğretici adımına dönmek için bkz: [5. adım: Etiket başvuruları ekleme](../ide/step-5-add-label-references.md).
