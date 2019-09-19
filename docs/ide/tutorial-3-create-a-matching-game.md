---
title: 'Öğretici 3: Eşleşen bir oyun oluşturun'
ms.date: 11/04/2016
ms.assetid: 525815c8-2845-45e8-be96-100d1f144725
ms.topic: tutorial
ms.technology: vs-ide-general
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f8fafd46561b6a3628989b675b14c493b60da6fe
ms.sourcegitcommit: 6eed0372976c0167b9a6d42ba443f9a474b8bb91
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71118709"
---
# <a name="tutorial-3-create-a-matching-game"></a>Öğretici 3: Eşleşen bir oyun oluşturun

Bu öğreticide, oyuncunun gizli simge çiftlerini eşleştirmesi gereken bir eşleştirme oyunu oluşturuyorsunuz. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:

- Simgeler gibi nesneleri bir <xref:System.Collections.Generic.List%601> nesnede depolayın.

- Bir listedeki öğeler arasında ilerlemek C# için görsel `For Each` veya Visual Basic döngüsünde bir döngükullanın.`foreach`

- Başvuru değişkenlerini kullanarak bir formun durumunu takip edin.

- Birden fazla nesneyle kullanabileceğiniz olaylara yanıt vermek için bir olay işleyicisi oluşturun.

- Geriye doğru sayan ve başlatılmasının ardından bir olayı kesin olarak tetikleyen bir zamanlayıcı hazırlayın.

Bu öğreticiyi tamamladığınızda, programınız aşağıdaki resme benzer şekilde görünür:

![Bu öğreticide oluşturduğunuz oyun](../ide/media/express_finishedgame.png)

## <a name="tutorial-links"></a>Öğretici bağlantıları

Örneğin tamamlanmış bir sürümünü indirmek için, bkz. [tüm eşleşen oyun öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).

> [!NOTE]
> Bu öğreticide, hem Visual C# hem de Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.

Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz. forum ve [görsel C# forumuna](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=csharpgeneral) [Visual Basic](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=vbgeneral) . Ayrıca, yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic programlama hakkında daha fazla bilgi için bkz [. Visual Basic temelleri: Mutlak yeni başlayanlar](https://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners)için geliştirme. Görselde C#programlama hakkında daha fazla bilgi edinmek için [ bkz C# . temel bilgiler: Mutlak yeni başlayanlar](https://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners)için geliştirme.

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[1. Adım: Bir proje oluşturma ve formunuza tablo ekleme](../ide/step-1-create-a-project-and-add-a-table-to-your-form.md)|Projeyi oluşturarak ve denetimleri doğru hizalı tutmak için `TableLayoutPanel` bir denetim ekleyerek başlayın.|
|[2. Adım: Rastgele bir nesne ve simge listesi ekleme](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)|Bir simge listesi oluşturmak için `List` bir nesnevenesneekleyin.`Random`|
|[3. Adım: Her etikete rastgele bir simge ata](../ide/step-3-assign-a-random-icon-to-each-label.md)|Her oyunun farklı olması için `Label` simgeleri denetimlere rastgele atayın.|
|[4. Adım: Her etikete bir tıklama olayı işleyicisi ekleyin](../ide/step-4-add-a-click-event-handler-to-each-label.md)|Tıklanan `Click` etiketin rengini değiştiren bir olay işleyicisi ekleyin.|
|[5. Adım: Etiket başvuruları Ekle](../ide/step-5-add-label-references.md)|Hangi etiketlere tıklandığını takip etmek için başvuru değişkenleri ekleyin.|
|[6. Adım: Süreölçer ekleme](../ide/step-6-add-a-timer.md)|Oyunda geçen süreyi takip etmek için forma bir zamanlayıcı ekleyin.|
|[7. Adım: Çiftleri görünür tut](../ide/step-7-keep-pairs-visible.md)|Eşleşen bir çift seçilirse, simge çiftlerini görünür durumda tutun.|
|[8. Adım: Oyuncunun kazanıp kazanılmadığını doğrulamak için bir yöntem ekleyin](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md)|Oyuncunun kazanıp kazanılmadığını doğrulamak için bir `CheckForWinner()` yöntem ekleyin.|
|[9. Adım: Diğer özellikleri deneyin](../ide/step-9-try-other-features.md)|Simgeleri ve renkleri değiştirme, kılavuz ekleme ve ses ekleme gibi diğer özellikleri deneyin. Tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.|
