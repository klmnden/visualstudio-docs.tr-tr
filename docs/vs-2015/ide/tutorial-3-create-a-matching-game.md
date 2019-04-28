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
ms.openlocfilehash: a7887df8a9dd012f1ec812f8bca38c1025ffe8a9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443229"
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
> Bu öğreticide, hem Visual C# hem de Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.  
  
 Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz: [Visual Basic Forumu](http://social.msdn.microsoft.com/Forums/home?forum=vbgeneral) ve [Visual C# Forumu](http://social.msdn.microsoft.com/Forums/home?forum=csharpgeneral). Ayrıca, yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic'te programlama hakkında daha fazla bilgi için bkz: [Visual Basic temelleri: Yeni başlayanlar için geliştirme](http://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners). Görselde programlama hakkında daha fazla bilgi edinmek için C#, bkz: [ C# temelleri: Yeni başlayanlar için geliştirme](http://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners).  
  
## <a name="related-topics"></a>İlgili Konular  
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[1. Adım: Proje Oluşturma ve Formunuza Tablo Ekleme](../ide/step-1-create-a-project-and-add-a-table-to-your-form.md)|Proje oluşturma ve ekleyerek başlayın bir `TableLayoutPanel` düzgün hizalanmasını denetimleri korumak için denetimi.|  
|[2. Adım: Rastgele Nesne ve Simge Listesi Ekleme](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)|Ekleme bir `Random` nesnesi ve bir `List` simge listesini oluşturmak için nesne.|  
|[3. Adım: Her Etikete Rastgele Bir Simge Atama](../ide/step-3-assign-a-random-icon-to-each-label.md)|Rasgele simgeleri atayın `Label` her oyunun farklı olması denetler.|  
|[4. Adım: Her Etikete Bir Tıklama Olayı İşleyicisi Ekleme](../ide/step-4-add-a-click-event-handler-to-each-label.md)|Tıklanan etiketin rengini değiştiren bir Click olayı işleyicisi ekleyin.|  
|[5. Adım: Etiket Başvuruları Ekleme](../ide/step-5-add-label-references.md)|Hangi etiketlere tıklandığını takip etmek için başvuru değişkenleri ekleyin.|  
|[6. Adım: Süreölçer Ekleme](../ide/step-6-add-a-timer.md)|Oyunda geçen süreyi takip etmek için forma bir zamanlayıcı ekleyin.|  
|[7. Adım: Çiftleri Görünür Durumda Tutma](../ide/step-7-keep-pairs-visible.md)|Eşleşen bir çift seçilirse, simge çiftlerini görünür durumda tutun.|  
|[8. Adım: Oyuncunun Kazanıp Kazanmadığını Doğrulamak için Yöntem Ekleme](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md)|Ekleme bir `CheckForWinner()` oyuncunun kazanıp kazanmadığını doğrulamak için yöntem.|  
|[9. Adım: Diğer Özellikleri Deneme](../ide/step-9-try-other-features.md)|Simgeleri ve renkleri değiştirme, kılavuz ekleme ve ses ekleme gibi diğer özellikleri deneyin. Tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.|
