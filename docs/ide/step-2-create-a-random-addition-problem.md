---
title: '2. Adım: Rasgele bir toplama problemi oluşturma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 6461c4cf-f2aa-4bf5-91ed-06820a4f893d
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 64a0b17d47d0906df680ed51c25fe3386d9b6b68
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53846119"
---
# <a name="step-2-create-a-random-addition-problem"></a>2. Adım: Rasgele bir toplama problemi oluşturma
Bu Eğitimin ikinci kısmında, sınav zorlu rastgele rakamlara dayanan matematik soruları ekleyerek olun. Adlı bir yöntem de oluşturduğunuz `StartTheQuiz()` ve problemleri dolduran ve geri sayım Zamanlayıcısını başlatır. Bu öğreticide daha sonra çıkarma, çarpma ve bölme sorularını ekleyeceksiniz.

> [!NOTE]
>  Bu konu, temel kodlama kavramları hakkındaki bir öğretici serisinin bir parçasıdır. Öğreticiye genel bakış için bkz. [öğretici 2: Zamanlı matematik testi oluşturma](../ide/tutorial-2-create-a-timed-math-quiz.md).

## <a name="to-create-a-random-addition-problem"></a>Rasgele bir toplama problemi oluşturma

1.  Form tasarımcısında formu (**Form1**).

2.  Menü çubuğunda, **görünümü** > **kod**.

     *Form1.cs* veya *Form1.vb* biçimin ardındaki kodu görüntüleyebilirsiniz. böylece, kullanmakta olduğunuz programlama diline göre görünür.

3.  Oluşturma bir <xref:System.Random> nesne ekleyerek bir `new` ekranın üst kısmında aşağıdaki gibi kod deyimi.

     [!code-csharp[VbExpressTutorial3Step2#1](../ide/codesnippet/CSharp/step-2-create-a-random-addition-problem_1.cs)]
     [!code-vb[VbExpressTutorial3Step2#1](../ide/codesnippet/VisualBasic/step-2-create-a-random-addition-problem_1.vb)]

     Formunuza rasgele nesne eklendi ve nesneyi **randomizer**.

     `Random` bir nesne olarak bilinir. Daha önce bu sözcüğü olasılıkla duydunuz ve bir sonraki öğreticide programlama için demek olduğu hakkında daha fazla bilgi edinin. Şimdilik, hemen kullanabileceğiniz unutmayın `new` deyimlerini düğmeler, etiketler, paneller, Openfiledialog'lar, Colordialog'lar, Soundplayer'lar, Random'lar ve hatta biçimler ve bu öğeleri oluşturmak için nesne olarak adlandırılır. Programınızı çalıştırdığınızda form başlatılır ve ardındaki kod bir rastgele nesnesi oluşturur ve onu olduğunda **randomizer**.

     Yakında yanıtlarını sınavınız her problem için ürettiği rastgele sayıları depolamak için değişkenleri kullanmalısınız denetlemek için bir yöntem oluşturacaksınız. Bkz: [değişkenleri](/dotnet/visual-basic/programming-guide/language-features/variables/index) veya [türleri](/dotnet/csharp/programming-guide/types/index). Değişkenleri düzgün kullanmak için bunları, yani adlarını ve veri türlerini listeleme bildirmeniz gerekir.

4.  Forma iki tamsayı değişkeni ekleyin ve bunları **addend1** ve **addend2**.

    > [!NOTE]
    >  Bir tamsayı değişkeni C# veya Visual Basic'te bir tamsayı tamsayı olarak bilinir. Bu türde bir değişken, -2147483648 ile 2147483647 arasında bir pozitif veya negatif sayı depolar ve ondalık değil yalnızca tam sayılara depolayabilirsiniz.

     Aşağıdaki kodun gösterdiği gibi rastgele bir nesne eklemek için yaptığınız gibi bir tam sayı değişkeni eklemek için benzer bir söz dizimi kullanın.

     [!code-csharp[VbExpressTutorial3Step2#2](../ide/codesnippet/CSharp/step-2-create-a-random-addition-problem_2.cs)]
     [!code-vb[VbExpressTutorial3Step2#2](../ide/codesnippet/VisualBasic/step-2-create-a-random-addition-problem_2.vb)]

5.  Adlı bir yöntem ekleyin `StartTheQuiz()` rastgele nesnenin kullanan ve <xref:System.Random.Next> etiketleri rastgele sayıları göstermek için yöntemi. `StartTheQuiz()` sonunda tüm problemleri doldurun ve süreölçeri başlatacak, bu nedenle bir açıklama ekleyin. İşlev, aşağıdaki gibi görünmelidir.

     [!code-csharp[VbExpressTutorial3Step2#3](../ide/codesnippet/CSharp/step-2-create-a-random-addition-problem_3.cs)]
     [!code-vb[VbExpressTutorial3Step2#3](../ide/codesnippet/VisualBasic/step-2-create-a-random-addition-problem_3.vb)]

     Nokta (.) girdiğinizde, sonra dikkat `randomizer` kodda, bir IntelliSense penceresinin açılır ve tüm çağırabilirsiniz rastgele nesnenin yöntemleri gösterir. Örneğin, IntelliSense listeler `Next()` yöntemini aşağıdaki gibi.

     ![Sonraki yöntem](../ide/media/express_randomwhite.png) sonraki yöntemi

     Bir nesneden sonra bir nokta girdiğinizde, IntelliSense nesnenin üyeleri, özellikler, yöntemler ve olaylar gibi bir listesini gösterir.

    > [!NOTE]
    >  Kullandığınızda `Next()` yöntemiyle `Random` çağırdığınızda gibi nesne `randomizer.Next(50)`, (Başlangıç, 0 ile 49 arasında) 50'den küçük rastgele bir sayı alın. Bu örnekte, aradığınız `randomizer.Next(51)`. Böylece iki rastgele sayı 0 ile 100 arası bir yanıt ekleyecek 51 ve 50 değil kullanılır. 50 geçirirseniz `Next()` yöntemi, bir sayı seçer 0 ile 49 arasında en yüksek olası yanıt 100 değil 98, bu nedenle. Her iki tamsayı değişkenleri, bir yöntemin ilk iki deyim, çalıştırdıktan sonra **addend1** ve **addend2**, 0 ile 50 arasında rastgele bir sayı tutun. Bu ekran Visual C# kodunu göstermektedir, ancak IntelliSense Visual Basic için aynı şekilde çalışır.

     Bu deyimlere daha yakından bakalım.

     [!code-csharp[VbExpressTutorial3Step2#18](../ide/codesnippet/CSharp/step-2-create-a-random-addition-problem_4.cs)]
     [!code-vb[VbExpressTutorial3Step2#18](../ide/codesnippet/VisualBasic/step-2-create-a-random-addition-problem_4.vb)]

     Deyimler **metin** özelliklerini **plusLeftLabel** ve **plusRightLabel** böylece bunlar iki rastgele sayı görüntüler. Bir tamsayının kullanmalısınız `ToString()` sayıları metne dönüştürmek için yöntemi. (Programlamada dize metin anlamına gelir. Etiket denetimleri, sayılar değil yalnızca metin görüntüler.

6.  Tasarım penceresinde, çift tıklayın ya da **Başlat** düğmesini veya bunu seçin ve ardından **Enter** anahtarı.

     Sınavı alan bu düğmeyi seçtiğinde sınavın başlaması gerekir ve bu davranışı gerçekleştirmek için bir tıklama olayı işleyicisi yalnızca ekledik.

7.  Aşağıdaki iki deyimi ekleyin.

     [!code-csharp[VbExpressTutorial3Step2#4](../ide/codesnippet/CSharp/step-2-create-a-random-addition-problem_5.cs)]
     [!code-vb[VbExpressTutorial3Step2#4](../ide/codesnippet/VisualBasic/step-2-create-a-random-addition-problem_5.vb)]

     İlk deyim yeni çağıran `StartTheQuiz()` yöntemi. İkinci deyim ayarlar **etkin** özelliği **startButton** denetimini **False** böylece sınavı alanın sınav sırasında düğmeyi seçemezsiniz.

8.  Kodunuzu kaydedin, çalıştırın ve ardından **Başlat** düğmesi.

     Rasgele bir toplama problemi, aşağıdaki çizimde gösterildiği gibi görünür.

     ![Rasgele bir toplama problemi](../ide/media/express_additionproblem.png) rasgele bir toplama problemi

     Öğreticinin bir sonraki adımda toplamı ekleyeceksiniz.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [3. adım: Bir geri sayım Zamanlayıcısı ekleme](../ide/step-3-add-a-countdown-timer.md).

-   Önceki öğretici adımına dönmek için bkz: [1. adım: Proje oluşturma ve formunuza etiketler ekleme](../ide/step-1-create-a-project-and-add-labels-to-your-form.md).
