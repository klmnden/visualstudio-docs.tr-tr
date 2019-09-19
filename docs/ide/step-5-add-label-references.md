---
title: '5\. Adım: Etiket başvuruları ekleme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
dev_langs:
- CSharp
- VB
ms.assetid: d418350c-0396-494e-8149-71fa61b395c5
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a076c4475b9e65d59aec08eac1774728b42cd77c
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71118971"
---
# <a name="step-5-add-label-references"></a>5\. Adım: Etiket başvuruları ekleme
Programın, Player 'ın seçtiği etiket denetimlerini izlemesi gerekir. Şu anda program oyuncunun seçtiği tüm etiketleri göstermektedir. Ancak bunun değişmesini sağlayacağız. İlk etiket seçildikten sonra program etiketin simgesini göstermelidir. İkinci etiket seçildikten sonra iki simgeyi de kısa bir süre göstermeli ve ardından iki simgeyi de tekrar gizlemelidir. Programınız artık ilk olarak hangi etiket denetiminin seçili olduğunu ve *başvuru değişkenlerini*kullanarak ikinci seçili olduğunu izler.

## <a name="to-add-label-references"></a>Etiket başvuruları eklemek için

1. Aşağıdaki kodu kullanarak formunuza etiket başvuruları ekleyin.

     [!code-vb[VbExpressTutorial4Step5#5](../ide/codesnippet/VisualBasic/step-5-add-label-references_1.vb)]
     [!code-csharp[VbExpressTutorial4Step5#5](../ide/codesnippet/CSharp/step-5-add-label-references_1.cs)]

     Bu başvuru değişkenleri formunuza nesneleri eklemek için (nesneler, <xref:System.Windows.Forms.Timer> <xref:System.Collections.Generic.List%601> nesneler ve <xref:System.Random> nesneler gibi), daha önce kullandığınız deyimlere benzer şekilde görünür. Ancak, iki deyimden birinde `new` anahtar sözcük kullanılmadığından, bu deyimler formda iki ek etiket denetiminin görünmesine neden olmaz. `new` Anahtar sözcüğü olmadan hiçbir nesne oluşturulmaz. Bunun nedeni `firstClicked` ve `secondClicked` başvuru değişkenleri denir: Yalnızca izleme (veya, başvuru) nesnelerini takip eder.

     Bir değişken bir nesneyi izlememediğinde, özel bir ayrılmış değere ayarlanır: `null` görsel C# ve `Nothing` Visual Basic. Bu nedenle, program `firstClicked` başlatıldığında ve `secondClicked` ya `Nothing`da olarak `null` ayarlanır; bu da değişkenlerin herhangi bir şeyi izlememediği anlamına gelir.

2. Olay işleyicinizi <xref:System.Windows.Forms.Control.Click> yeni `firstClicked` başvuru değişkenini kullanacak şekilde değiştirin. `label_Click()` Olay işleyicisi yönteminde (`clickedLabel.ForeColor = Color.Black;`) son ifadeyi kaldırın `if` ve bunu takip eden deyimle değiştirin. (Yorumu ve tüm `if` deyimin dahil ettiğinizden emin olun.)

     [!code-vb[VbExpressTutorial4Step5#6](../ide/codesnippet/VisualBasic/step-5-add-label-references_2.vb)]
     [!code-csharp[VbExpressTutorial4Step5#6](../ide/codesnippet/CSharp/step-5-add-label-references_2.cs)]

3. Programınızı kaydedin ve çalıştırın. Etiket denetimlerinden birini seçtiğinizde ilgili denetimin simgesi görünür.

4. Bir sonraki etiket denetimini seçin ve hiçbir olay gerçekleşmediğine dikkat edin. Program, Player 'ın seçtiği ilk etiketi zaten takip ediyor, `firstClicked` bu nedenle görsel C# veya `Nothing` Visual Basic olarak `null` eşit değil. Deyiminiz `if` `null` veya `if` `firstClicked` 'aeşitolupolmadığınıbelirlemeyidenetlediğinde,olmadığınıbulurvedeyimdekideyimleriyürütmez.`Nothing` Bu nedenle, aşağıdaki resimde gösterildiği gibi, yalnızca seçilen ilk simgenin rengi siyah olur ve diğer simgeler görünmez.

     ![Bir simge ile eşleşen bir](../ide/media/express_tut4step5.png)
**oyun** gösteren bir simge ile eşleşen oyun

     Bu durumu, bir **Zamanlayıcı** denetimi ekleyerek öğreticinin bir sonraki adımında düzeltireceksiniz.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğretici adımına gitmek için bkz [. 6. Adım: Süreölçer](../ide/step-6-add-a-timer.md)ekleyin.

- Önceki öğretici adımına dönmek için bkz [. 4. Adım: Her etikete](../ide/step-4-add-a-click-event-handler-to-each-label.md)bir tıklama olayı işleyicisi ekleyin.
