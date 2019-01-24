---
title: 'Öğretici 3: Bir eşleştirme oyunu oluşturun | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 525815c8-2845-45e8-be96-100d1f144725
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 44c9b6578085ee49796078976b30d78f1656e58f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54792719"
---
# <a name="tutorial-3-create-a-matching-game"></a>Öğretici 3: Eşleme oyunu oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu öğreticide, oyuncunun gizli simge çiftlerini eşleştirmesi gereken bir eşleştirme oyunu oluşturuyorsunuz. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:  
  
- Store simgeler gibi nesneleri bir `List` nesne.  
  
- Kullanım bir `foreach` döngü Visual C# veya `For Each` bir listedeki öğeler arasında yineleme yapmak için Visual Basic'te döngü.  
  
- Başvuru değişkenlerini kullanarak bir formun durumunu takip edin.  
  
- Birden fazla nesneyle kullanabileceğiniz olaylara yanıt vermek için bir olay işleyicisi oluşturun.  
  
- Geriye doğru sayan ve başlatılmasının ardından bir olayı kesin olarak tetikleyen bir zamanlayıcı hazırlayın.  
  
  Bu öğreticiyi bitirdiğinizde, programınız aşağıdaki resim gibi görünecektir.  
  
  ![Bu öğreticide oluşturduğunuz oyun](../ide/media/express-finishedgame.png "Express_FinishedGame")  
  Bu öğreticide oluşturduğunuz oyun  
  
  Örnek tamamlanmış bir sürümünü indirmek için bkz [eksiksiz eşleştirme oyunu Öğreticisi örneği](http://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).  
  
> [!NOTE]
>  Bu öğreticide, hem Visual C# hem de Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.  
  
 Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz: [Visual Basic Forumu](http://social.msdn.microsoft.com/Forums/home?forum=vbgeneral) ve [Visual C# Forumu](http://social.msdn.microsoft.com/Forums/home?forum=csharpgeneral). Ayrıca, yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic'te programlama hakkında daha fazla bilgi için bkz: [Visual Basic temelleri: Yeni başlayanlar için geliştirme](http://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners). Görselde programlama hakkında daha fazla bilgi edinmek için C#, bkz: [ C# temelleri: Yeni başlayanlar için geliştirme](http://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners).  
  
## <a name="related-topics"></a>İlgili Konular  
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[1. adım: Proje oluşturma ve formunuza tablo ekleme](../ide/step-1-create-a-project-and-add-a-table-to-your-form.md)|Proje oluşturma ve ekleyerek başlayın bir `TableLayoutPanel` düzgün hizalanmasını denetimleri korumak için denetimi.|  
|[2. adım: Rasgele nesne ve simge listesi ekleme](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)|Ekleme bir `Random` nesnesi ve bir `List` simge listesini oluşturmak için nesne.|  
|[3. adım: Her etikete rasgele simge atama](../ide/step-3-assign-a-random-icon-to-each-label.md)|Rasgele simgeleri atayın `Label` her oyunun farklı olması denetler.|  
|[4. adım: Her etikete Click olay işleyicisi ekleme](../ide/step-4-add-a-click-event-handler-to-each-label.md)|Tıklanan etiketin rengini değiştiren bir Click olayı işleyicisi ekleyin.|  
|[5. adım: Etiket başvuruları ekleme](../ide/step-5-add-label-references.md)|Hangi etiketlere tıklandığını takip etmek için başvuru değişkenleri ekleyin.|  
|[6. adım: Zamanlayıcı ekleme](../ide/step-6-add-a-timer.md)|Oyunda geçen süreyi takip etmek için forma bir zamanlayıcı ekleyin.|  
|[7. adım: Çiftleri görünür kılma](../ide/step-7-keep-pairs-visible.md)|Eşleşen bir çift seçilirse, simge çiftlerini görünür durumda tutun.|  
|[8. adım: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md)|Ekleme bir `CheckForWinner()` oyuncunun kazanıp kazanmadığını doğrulamak için yöntem.|  
|[9. adım: Diğer özellikleri deneme](../ide/step-9-try-other-features.md)|Simgeleri ve renkleri değiştirme, kılavuz ekleme ve ses ekleme gibi diğer özellikleri deneyin. Tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.|
