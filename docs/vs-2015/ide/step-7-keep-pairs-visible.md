---
title: '7\. Adım: Çiftleri görünür kılma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 42e1d08c-7b2e-4efd-9f47-85d6206afe35
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4f0c0b7b3e1edb367db6a49987a67e8a6dfdc17c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68178592"
---
# <a name="step-7-keep-pairs-visible"></a>7\. Adım: Çiftleri Görünür Durumda Tutma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Oyuncu yalnızca eşleşmeyen simge çiftlerini seçtiği sürece oyun düzgün çalışır. Ancak oyuncu eşleşen bir çift seçtiğinde ne olması gerektiğini bir düşünün. Zamanlayıcıyı açarak yerine simgelerin kaybolmasını (kullanarak `Start()` yöntemi), böylece, artık kullanarak etiketleri izlemek oyun kendisini sıfırlamalı `firstClicked` ve `secondClicked` başvuru değişkenlerini sıfırlamadan Seçilen iki etiketlerinin renk.  
  
### <a name="to-keep-pairs-visible"></a>Çiftleri görünür durumda tutmak için  
  
1. Aşağıdaki `if` ifadesine `label_Click()` olay işleyicisi yönteminde, Zamanlayıcıyı başladığı deyimi yalnızca yukarıdaki kodu sonuna yakın. Kodu programa eklerken yakından inceleyin. Kodun nasıl çalıştığını bir düşünün.  
  
     [!code-csharp[VbExpressTutorial4Step7#9](../snippets/csharp/VS_Snippets_VBCSharp/vbexpresstutorial4step7/cs/form1.cs#9)]
     [!code-vb[VbExpressTutorial4Step7#9](../snippets/visualbasic/VS_Snippets_VBCSharp/vbexpresstutorial4step7/vb/form1.vb#9)]  
  
     İlk satırı `if` deyimi eklemiş simgesi oyuncunun seçtiği ilk etiketteki simgenin ikinci etiketi ile aynı olup olmadığını denetler. Simgeler aynıysa, program C# veya içindeki üç deyimi ortamında kaşlı ayraçlar arasındaki üç deyimi yürütür `if` Visual Basic'te deyimi. İlk iki deyim `firstClicked` ve `secondClicked` başvuru değişkenlerini böylece bunlar artık herhangi bir etiket izler. (Bu iki deyim, zamanlayıcının Tick olay işleyicisinden size tanıdık gelebilir.) Üçüncü deyim bir `return` deyimi programın deyimlerin geri kalanını yürütmeden atlamasını söyler.  
  
     Visual C# ortamında, bazı kodları kullandığı tek bir eşittir işareti fark etmiş (`=`), diğer deyimler iki eşittir işareti kullanırken (`==`). Neden göz önünde bulundurun `=` bazı yerlerde kullanılır ancak `==` diğer yerlerde kullanılır.  
  
     Bu örnek, aradaki farkı gösteren güzel bir örnektir. Parantezler arasındaki koda dikkatlice bir bakın ele `if` deyimi.  
  
    ```vb  
    firstClicked.Text = secondClicked.Text  
    ```  
  
    ```csharp  
    firstClicked.Text == secondClicked.Text  
    ```  
  
     En sonra kod bloğundaki ilk deyimi yakından bakın `if` deyimi.  
  
    ```vb  
    firstClicked = Nothing  
    ```  
  
    ```csharp  
    firstClicked = null;  
    ```  
  
     Bu deyimlerden birincisi iki simgenin aynı olup olmadığını denetler. İki değer karşılaştırıldığı için Visual C# programı kullanan `==` eşitlik işleci. İkinci deyim aslında değeri değiştirir (adlı *atama*) ayarını `firstClicked` başvuru değişkenini eşit `null` sıfırlamak için. İşte bu kullandığı `=` atama işleci bunun yerine. Visual C# kullanan `=` değerleri ayarlamak için ve `==` bunları karşılaştırmak için. Visual Basic kullanan `=` hem değişken ataması hem de karşılaştırma için.  
  
2. Programı kaydedip çalıştırın ve sonra formdaki simgeleri seçmeye başlayın. Eşleşmeyen bir çift seçerseniz, zamanlayıcının Tick olayı tetiklenir ve iki simge de kaybolur. Eşleşen bir çift seçerseniz yeni `if` deyimi yürütür ve return deyiminin yöntemi aşağıdaki resimde gösterildiği gibi simgeler görünür durumda kalır, böylece Zamanlayıcıyı başlatan kodu atlamasına neden olur.  
  
     ![Bu öğreticide oluşturduğunuz oyun](../ide/media/express-finishedgame.png "Express_FinishedGame")  
Eşleştirme oyunu ve görünür simge çiftleri  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
- Sonraki öğretici adımına gitmek için bkz: [adım 8: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md).  
  
- Önceki öğretici adımına dönmek için bkz: [adım 6: Bir zamanlayıcı ekleyin](../ide/step-6-add-a-timer.md).
