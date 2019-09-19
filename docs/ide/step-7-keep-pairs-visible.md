---
title: '7\. Adım: Çiftleri görünür durumda tutma'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
dev_langs:
- CSharp
- VB
ms.assetid: 42e1d08c-7b2e-4efd-9f47-85d6206afe35
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d0216d778278f02f7fc63630f4ff6ce90c755e3c
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71118657"
---
# <a name="step-7-keep-pairs-visible"></a>7\. Adım: Çiftleri görünür durumda tutma
Oyuncu yalnızca eşleşmeyen simge çiftlerini seçtiği sürece oyun düzgün çalışır. Ancak oyuncu eşleşen bir çift seçtiğinde ne olması gerektiğini bir düşünün. Zamanlayıcıyı etkinleştirerek ( <xref:System.Windows.Forms.Timer.Start> yöntemi kullanarak) simgeleri ortadan kaldırmamak yerine, oyunun kendisini sıfırlaması gerekir; böylece, `firstClicked` ve `secondClicked` başvuru değişkenlerini kullanarak hiçbir etiketi takip etmeden önce Seçilen iki etiket için renkler.

## <a name="to-keep-pairs-visible"></a>Çiftleri görünür durumda tutmak için

1. Aşağıdaki `if` ifadeyi, süreölçer 'i başlattığınız `label_Click()` deyimin hemen üstündeki kodun sonuna yakın şekilde olay işleyicisi yöntemine ekleyin. Kodu programa eklerken yakından inceleyin. Kodun nasıl çalıştığını bir düşünün.

     [!code-csharp[VbExpressTutorial4Step7#9](../ide/codesnippet/CSharp/step-7-keep-pairs-visible_1.cs)]
     [!code-vb[VbExpressTutorial4Step7#9](../ide/codesnippet/VisualBasic/step-7-keep-pairs-visible_1.vb)]

     Az önce eklediğiniz `if` deyimin ilk satırı, Player 'ın seçtiği ilk etiketteki simgenin ikinci etiketteki simgeyle aynı olup olmadığını denetler. Simgeler aynıysa program, içindeki C# küme ayraçları veya `if` Visual Basic içindeki deyimde yer alan üç deyim arasında üç deyimi yürütür. İlk iki deyim, `firstClicked` ve `secondClicked` başvuru değişkenlerini sıfırlar, böylece artık etiketlerden herhangi birini takip etmezsiniz. (Bu iki deyimi zamanlayıcının <xref:System.Windows.Forms.Timer.Tick> olay işleyicisinden ayırt edebilirsiniz.) Üçüncü deyim, programa onları `return` yürütmeden, yöntemi içindeki deyimlerin geri kalanını atlamasını söyleyen bir deyimidir.

     Görselde C#programlama yaparsanız, bazı kodların tek bir eşittir işareti (`=`) kullandığını fark etmiş olabilirsiniz, ancak diğer deyimler iki eşittir işareti (`==`) kullanır. Neden `=` bazı yerlerde kullanıldığına, ancak `==` diğer yerlerde kullanıldığına göz önünde bulundurun.

     Bu örnek, aradaki farkı gösteren güzel bir örnektir. `if` Deyimdeki parantez arasındaki koda dikkatli bir göz atın.

    ```vb
    firstClicked.Text = secondClicked.Text
    ```

    ```csharp
    firstClicked.Text == secondClicked.Text
    ```

     Ardından, `if` deyimden sonra kod bloğundaki ilk ifadeye yakından bakın.

    ```vb
    firstClicked = Nothing
    ```

    ```csharp
    firstClicked = null;
    ```

     Bu deyimlerden birincisi iki simgenin aynı olup olmadığını denetler. İki değer karşılaştırıldığından, görsel C# program `==` eşitlik işlecini kullanır. İkinci ifade gerçekten değeri değiştirir ( *atama*olarak adlandırılır), `firstClicked` başvuru değişkenini sıfırlamak için değerine eşit olarak `null` ayarlar. Bunun yerine `=` atama işlecini kullanmasının nedeni budur. Görsel C# , `=` değerleri ayarlamak ve `==` karşılaştırmak için kullanır. Visual Basic, `=` hem değişken atama hem de karşılaştırma için kullanır.

2. Programı kaydedip çalıştırın ve sonra formdaki simgeleri seçmeye başlayın. Eşleşmeyen bir çift seçerseniz, zamanlayıcının Tick olayı tetiklenir ve iki simge de kaybolur. Eşleşen bir çift seçerseniz, yeni `if` ifade yürütülür ve Return deyimleri, aşağıdaki resimde gösterildiği gibi, simgenin görünür kalması için, bu yöntemin zamanlayıcıyı başlatan kodu atlamasına neden olur.

     ![Bu öğreticide](../ide/media/express_finishedgame.png)
, görünür simge çiftleri ile**eşleşen oyun** ile oluşturduğunuz oyun

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 8. Adım: Oyuncunun kazanıp kazanılmadığını](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md)doğrulamak için bir yöntem ekleyin.

- Önceki öğretici adımına dönmek için bkz [. 6. Adım: Süreölçer](../ide/step-6-add-a-timer.md)ekleyin.
