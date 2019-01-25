---
title: '5. Adım: Etiket başvuruları ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: d418350c-0396-494e-8149-71fa61b395c5
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: baae597f606b6333f15ba114d31af2cb0cf28836
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54833671"
---
# <a name="step-5-add-label-references"></a>5. Adım: Etiket Başvuruları Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Programın, oyuncunun seçtiği etiket kontrollerini izlemesi gerekir. Şu anda program oyuncunun seçtiği tüm etiketleri göstermektedir. Ancak bunun değişmesini sağlayacağız. İlk etiket seçildikten sonra program etiketin simgesini göstermelidir. İkinci etiket seçildikten sonra iki simgeyi de kısa bir süre göstermeli ve ardından iki simgeyi de tekrar gizlemelidir. Programınız şimdi hangi etiket denetiminin ilk ve kullanarak, ikinci seçilir izlemek *başvuru değişkenlerini*.  
  
### <a name="to-add-label-references"></a>Etiket başvuruları eklemek için  
  
1.  Aşağıdaki kodu kullanarak formunuza etiket başvuruları ekleyin.  
  
     [!code-csharp[VbExpressTutorial4Step5#5](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial4step5/cs/form1.cs#5)]
     [!code-vb[VbExpressTutorial4Step5#5](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial4step5/vb/form1.vb#5)]  
  
     Bu başvuru değişkenleri önceki nesneleri eklemek için kullandığınız deyimlere benzer görünür (gibi `Timer` nesneleri `List` nesneleri ve `Random` nesneleri) formunuza. Ancak, bu deyimler olduğundan form üzerinde gözükmesini fazladan iki etiket denetiminin neden hiç `new` ya da iki deyimde kullanılan anahtar sözcüğü. Olmadan `new` anahtar sözcüğü, hiçbir nesne oluşturulmaz. İşte bu `firstClicked` ve `secondClicked` başvuru değişkenleri olarak adlandırılmasının: Bunlar yalnızca izlerler (veya bakın) `Label` nesneleri.  
  
     Bir değişken bir nesneyi izleyen olduğunda, bir özel bir değere ayarlanır: `null` Visual C# ve `Nothing` Visual Basic'te. Bu nedenle, program başladığında hem `firstClicked` ve `secondClicked` ayarlandığından `null` veya `Nothing`, değişkenleri herhangi bir şey izleyen emin değilseniz anlamına gelir.  
  
2.  Yeni Click olayı işleyicinizi değiştirme `firstClicked` başvuru değişkenini. Son deyimi kaldırın `label_Click()` olay işleyicisi yöntemi (`clickedLabel.ForeColor = Color.Black;`) ile değiştirirsiniz `if` aşağıdaki deyimi. (Açıklamayı ve tüm eklediğinizden emin olun `if` deyimi.)  
  
     [!code-csharp[VbExpressTutorial4Step5#6](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial4step5/cs/form1.cs#6)]
     [!code-vb[VbExpressTutorial4Step5#6](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial4step5/vb/form1.vb#6)]  
  
3.  Programınızı kaydedin ve çalıştırın. Etiket denetimlerinden birini seçtiğinizde ilgili denetimin simgesi görünür.  
  
4.  Bir sonraki etiket denetimini seçin ve hiçbir olay gerçekleşmediğine dikkat edin. Program zaten oyuncunun seçtiği, bunu ilk etiketi izleyen olan `firstClicked` değerine eşit değildir `null` Visual C# veya `Nothing` Visual Basic'te. Olduğunda, `if` deyimi denetimleri `firstClicked` eşit olup olmadığını belirlemek için `null` veya `Nothing`, büyük değildir ve içindeki deyimleri yürütmez bulduğu `if` deyimi. Bu nedenle, aşağıdaki resimde gösterildiği gibi, yalnızca seçilen ilk simgenin rengi siyah olur ve diğer simgeler görünmez.  
  
     ![Bir simgeyi gösteren eşleştirme oyunu](../ide/media/express-tut4step5.png "Express_Tut4Step5")  
Tek bir simgeyi gösteren eşleştirme oyunu  
  
     Öğreticinin sonraki adımda ekleyerek bu durumu çözeceksiniz bir **Zamanlayıcı** denetimi.  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
-   Sonraki öğretici adımına gitmek için bkz: [adım 6: Bir zamanlayıcı ekleyin](../ide/step-6-add-a-timer.md).  
  
-   Önceki öğretici adımına dönmek için bkz: [4. adım: Her etikete Click olay işleyicisi ekleme](../ide/step-4-add-a-click-event-handler-to-each-label.md).
