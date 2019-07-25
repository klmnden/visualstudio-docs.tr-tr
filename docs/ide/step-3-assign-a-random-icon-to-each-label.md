---
title: '3\. Adım: Her etikete rastgele bir simge atama'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- csharp
- vb
ms.assetid: 0ba5ed7a-9aaa-41f4-95d2-e3c2d567bc79
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ae4b635f86eb67f04db3ba6243e7b0ba4634bfb4
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416670"
---
# <a name="step-3-assign-a-random-icon-to-each-label"></a>3\. Adım: Her etikete rastgele bir simge atama
Simgeler her oyunda aynı hücrelerde gösterilirse, oyun pek de zorlu olmaz. Bunu önlemek için, bir `AssignIconsToSquares()` yöntemi kullanarak simgeleri formunuzdaki etiket denetimlerine rastgele atayın.

## <a name="to-assign-a-random-icon-to-each-label"></a>Her etikete rasgele bir simge atamak için

1. Aşağıdaki kodu eklemeden önce yöntemin nasıl çalıştığını düşünün. Yeni bir anahtar sözcük vardır: `foreach` görselde C# ve `For Each` Visual Basic. (Satırlardan biri bilerek derleme dışı bırakılmıştır; bunun nedeni bu yordamın sonunda açıklanmaktadır.)

     [!code-csharp[VbExpressTutorial4Step2_3_4#2](../ide/codesnippet/CSharp/step-3-assign-a-random-icon-to-each-label_1.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#2](../ide/codesnippet/VisualBasic/step-3-assign-a-random-icon-to-each-label_1.vb)]

2. Yöntemi, `AssignIconsToSquares()` önceki adımda gösterildiği gibi ekleyin. Bunu adım 2 ' de [eklediğiniz kodun hemen altına yerleştirebilirsiniz: Rastgele bir nesne ve simge](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)listesi ekleyin.

     Daha önce belirtildiği gibi `AssignIconsToSquares()` , yöntetiğiniz yeni bir şey vardır: görsel `foreach` C# ve `For Each` Visual Basic içinde bir döngü. Bir `For Each` döngüyü, aynı eylemi birden çok kez yapmak istediğiniz zaman kullanabilirsiniz. Bu durumda, aşağıdaki kodda açıklandığı gibi <xref:System.Windows.Forms.TableLayoutPanel>, içindeki her etiket için aynı deyimleri yürütmek istersiniz. İlk satır, her denetimi bir kez `control` depolayan adlı bir değişken oluşturur ve bu denetim, üzerinde yürütülen deyimlerdeki deyimler vardır.

     [!code-csharp[VbExpressTutorial4Step2_3_4#14](../ide/codesnippet/CSharp/step-3-assign-a-random-icon-to-each-label_2.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#14](../ide/codesnippet/VisualBasic/step-3-assign-a-random-icon-to-each-label_2.vb)]

    > [!NOTE]
    > "iconLabel" (simge etiketi) ve "control" (denetim) kullanılmasının nedeni bu adların açıklayıcı olmasıdır. Bu adların yerine istediğiniz adları kullanabilirsiniz; ilgili adı döngüdeki her bir deyimde de değiştirdiğiniz sürece kod tamamen aynı şekilde çalışacaktır.

     `AssignIconsToSquares()` Yöntemi TableLayoutPanel içindeki her etiket denetimi boyunca yinelenir ve her biri için aynı deyimleri yürütür. Bu deyimler, adım 2 ' de [eklediğiniz listeden rastgele bir simge çeker: Rastgele bir nesne ve simge](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)listesi ekleyin. (Bu nedenle, listedeki her bir simgenin ikisini de eklemiş olursunuz, bu nedenle rastgele etiket denetimlerine atanan bir çift simge vardır.)

     `foreach` Veya`For Each` döngüsünün içinde çalışan koda daha yakından bakın. Bu kod burada tekrar üretilmektedir.

     [!code-csharp[VbExpressTutorial4Step2_3_4#16](../ide/codesnippet/CSharp/step-3-assign-a-random-icon-to-each-label_3.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#16](../ide/codesnippet/VisualBasic/step-3-assign-a-random-icon-to-each-label_3.vb)]

     İlk satır, **Denetim** değişkenini **iconLabel**adlı bir etikete dönüştürür. Bundan sonraki satır, dönüştürmenin çalıştığından `if` emin olmak için denetleyen bir ifadedir. Dönüştürme işe alıyorsa, `if` deyimindeki deyimler çalışır. (Önceki öğreticilerden hatırlayabileceğiniz gibi, `if` ifade belirttiğiniz koşulu değerlendirmek için kullanılır.) `if` Deyimdeki ilk satır, simgeler listesindeki öğelerden birine karşılık gelen rastgele bir sayı içeren **rasgelenumber** adlı bir değişken oluşturur. Bunu yapmak için, daha önce oluşturduğunuz <xref:System.Random.Next> <xref:System.Random> nesnenin yöntemini kullanır. `Next` Yöntemi rastgele sayı döndürür. Bu satır, rastgele sayının <xref:System.Collections.Generic.List%601.Count> seçim aralığını belirlemek için **simgeler** listesinin özelliğini de kullanır. Sonraki satır, simge listesi öğelerinden <xref:System.Windows.Forms.Label.Text> birini etiketin özelliğine atar. Derleme dışı bırakılan satır bu konunun sonunda açıklanmaktadır. Son olarak, `if` deyimindeki son satır, forma eklenmiş olan simgeyi listeden kaldırır.

     Kodun belirli bir bölümünün ne işe yaradığından emin olamadığınızda, fare işaretçisini kod öğesinin üzerine getirip ortaya çıkan araç ipucunu gözden geçirebileceğinizi unutmayın. Ayrıca, Visual Studio hata ayıklayıcısını kullanarak, program çalışırken kodun her satırını adım adım geçebilirsiniz. Nasıl yaparım? [bkz: Visual Studio 'daki hata ayıklayıcıyla adımla mı? veya daha fazla bilgi için [hata ayıklayıcıyla kod üzerinden gezinebilirsiniz.](../debugger/navigating-through-code-with-the-debugger.md) ](https://msdn.microsoft.com/vstudio/ee672313.aspx)

3. Oyun panosunu simgelerle doldurmanız için Program başlatıldıktan hemen sonra `AssignIconsToSquares()` yöntemi çağırmanız gerekir. Görsel C#kullanıyorsanız `InitializeComponent()` , **Form1**_oluşturucusunda_yöntemine yapılan çağrının hemen altına bir ifade ekleyin, böylece formunuz görüntülenmeden önce kendisini ayarlamak için yeni yönteminizi çağırır. Oluşturucular, sınıf veya yapı gibi yeni bir nesne oluşturduğunuzda çağrılır. Daha fazla bilgi için bkz. [oluşturucular (C# programlama kılavuzu)](/dotnet/csharp/programming-guide/classes-and-structs/constructors) veya Visual Basic [oluşturucular ve Yıkıcılar kullanma](/previous-versions/visualstudio/visual-studio-2008/2z08e49e\(v\=vs.90\)) .

     [!code-csharp[VbExpressTutorial4Step2_3_4#13](../ide/codesnippet/CSharp/step-3-assign-a-random-icon-to-each-label_4.cs)]

     Visual Basic için yöntemine `AssignIconsToSquares()` yöntem çağrısını `Form1_Load` ekleyerek kodun aşağıdaki gibi görünmesini sağlayın.

    ```vb
    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        AssignIconsToSquares()
    End Sub
    ```

4. Programınızı kaydedip çalıştırın. Her etikete rasgele simgelerin atandığı bir form gösterilmesi gerekir.

5. Programınızı kapatın ve yeniden çalıştırın. Aşağıdaki resimde gösterildiği gibi, her etikete farklı simgeler atandığına dikkat edin.

     ![Rastgele simgelerle eşleşen oyun ile](../ide/media/express_tut4step3.png) eşleşen oyun

     Henüz gizlemediğiniz için simgeler şimdilik görünmektedir. Bunları Player 'dan gizlemek için, her etiketin **ForeColor** özelliğini **BackColor** özelliği ile aynı renge ayarlayabilirsiniz.

    > [!TIP]
    > Etiketler gibi denetimleri gizlemenin bir diğer yolu da **Visible** özelliğini **false**olarak ayarlamanıza olanak sağlar.

6. Simgeleri gizlemek için programı durdurun ve `For Each` döngü içindeki açıklamalı kod satırının açıklama işaretlerini kaldırın.

     [!code-csharp[VbExpressTutorial4Step2_3_4#15](../ide/codesnippet/CSharp/step-3-assign-a-random-icon-to-each-label_5.cs)]
     [!code-vb[VbExpressTutorial4Step2_3_4#15](../ide/codesnippet/VisualBasic/step-3-assign-a-random-icon-to-each-label_5.vb)]

7. Menü çubuğunda, **Tümünü Kaydet** düğmesini seçerek programınızı kaydedin ve çalıştırın. Simgelerin kaybolduğu görülür ve yalnızca mavi bir arka plan görüntülenir. Bununla birlikte simgeler rasgele atanırlar ve halen oradadırlar. Simgeler arka plan ile aynı renkte olduğundan, oyuncudan gizlenmiş olurlar. Sonuçta, oyuncu simgelerin tümünü doğrudan görebilseydi hiç de zorlayıcı bir oyun olmazdı!

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 4. Adım: Her etikete](../ide/step-4-add-a-click-event-handler-to-each-label.md)bir tıklama olayı işleyicisi ekleyin.

- Önceki öğretici adımına dönmek için bkz [. 2. Adım: Rastgele bir nesne ve simge](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)listesi ekleyin.
