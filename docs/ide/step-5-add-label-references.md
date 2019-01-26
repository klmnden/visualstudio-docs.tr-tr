---
title: '5. Adım: Etiket başvuruları ekleme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: d418350c-0396-494e-8149-71fa61b395c5
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2368f3f0deff4262ffebca736fc14e6d5bc142a2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55005448"
---
# <a name="step-5-add-label-references"></a>5. Adım: Etiket başvuruları ekleme
Program oyuncunun seçtiği etiket kontrollerini izlemesi gerekir. Şu anda program oyuncunun seçtiği tüm etiketleri göstermektedir. Ancak bunun değişmesini sağlayacağız. İlk etiket seçildikten sonra program etiketin simgesini göstermelidir. İkinci etiket seçildikten sonra iki simgeyi de kısa bir süre göstermeli ve ardından iki simgeyi de tekrar gizlemelidir. Programınız şimdi hangi etiket denetiminin ilk ve kullanarak, ikinci seçilir izlemek *başvuru değişkenlerini*.

## <a name="to-add-label-references"></a>Etiket başvuruları eklemek için

1.  Aşağıdaki kodu kullanarak formunuza etiket başvuruları ekleyin.

     [!code-vb[VbExpressTutorial4Step5#5](../ide/codesnippet/VisualBasic/step-5-add-label-references_1.vb)]
     [!code-csharp[VbExpressTutorial4Step5#5](../ide/codesnippet/CSharp/step-5-add-label-references_1.cs)]

     Bu başvuru değişkenleri önceki nesneleri eklemek için kullandığınız deyimlere benzer görünür (gibi <xref:System.Windows.Forms.Timer> nesneleri <xref:System.Collections.Generic.List%601> nesneleri ve <xref:System.Random> nesneleri) formunuza. Bu deyimler iki ek etiket denetimleri olduğundan form üzerinde gözükmesini neden olmaz ancak hiçbir `new` ya da iki deyimde kullanılan anahtar sözcüğü. Olmadan `new` anahtar sözcüğü, hiçbir nesne oluşturulmaz. İşte bu `firstClicked` ve `secondClicked` başvuru değişkenleri olarak adlandırılmasının: Bunlar yalnızca izlerler (veya bakın) etiket nesneleri.

     Bir değişken bir nesneyi izleyen olduğunda, bir özel bir değere ayarlanır: `null` Visual C# ve `Nothing` Visual Basic'te. Bu nedenle, program başladığında hem `firstClicked` ve `secondClicked` ayarlandığından `null` veya `Nothing`, değişkenleri herhangi bir şey izleyen emin değilseniz anlamına gelir.

2.  Değişiklik, <xref:System.Windows.Forms.Control.Click> yeni olay işleyicisi `firstClicked` başvuru değişkenini. Son deyimi kaldırın `label_Click()` olay işleyicisi yöntemi (`clickedLabel.ForeColor = Color.Black;`) ile değiştirirsiniz `if` aşağıdaki deyimi. (Açıklamayı ve tüm eklediğinizden emin olun `if` deyimi.)

     [!code-vb[VbExpressTutorial4Step5#6](../ide/codesnippet/VisualBasic/step-5-add-label-references_2.vb)]
     [!code-csharp[VbExpressTutorial4Step5#6](../ide/codesnippet/CSharp/step-5-add-label-references_2.cs)]

3.  Programınızı kaydedin ve çalıştırın. Etiket denetimlerinden birini seçtiğinizde ilgili denetimin simgesi görünür.

4.  Bir sonraki etiket denetimini seçin ve hiçbir olay gerçekleşmediğine dikkat edin. Program zaten oyuncunun seçtiği, bunu ilk etiketi izleyen olan `firstClicked` değerine eşit değildir `null` Visual C# veya `Nothing` Visual Basic'te. Olduğunda, `if` deyimi denetimleri `firstClicked` eşit olup olmadığını belirlemek için `null` veya `Nothing`, büyük değildir ve içindeki deyimleri yürütmez bulduğu `if` deyimi. Bu nedenle, aşağıdaki resimde gösterildiği gibi, yalnızca seçilen ilk simgenin rengi siyah olur ve diğer simgeler görünmez.

     ![Tek bir simgeyi gösteren eşleşen oyun](../ide/media/express_tut4step5.png)
**eşleştirme oyunu** bir simge gösteriliyor

     Öğreticinin sonraki adımda ekleyerek bu durumu çözeceksiniz bir **Zamanlayıcı** denetimi.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Sonraki öğretici adımına gitmek için bkz: [adım 6: Bir zamanlayıcı ekleyin](../ide/step-6-add-a-timer.md).

-   Önceki öğretici adımına dönmek için bkz: [4. adım: Her etikete Click olay işleyicisi ekleme](../ide/step-4-add-a-click-event-handler-to-each-label.md).
