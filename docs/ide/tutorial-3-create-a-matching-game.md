---
title: 'Öğretici 3: Eşleşen bir oluşturma oyun'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 525815c8-2845-45e8-be96-100d1f144725
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 151b9be68b82f2b9fdcb20cd105890914333a2b6
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60111772"
---
# <a name="tutorial-3-create-a-matching-game"></a>Öğretici 3: Eşleşen bir oluşturma oyun

Bu öğreticide, oyuncunun gizli simge çiftlerini eşleştirmesi gereken bir eşleştirme oyunu oluşturuyorsunuz. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:

- Store simgeler gibi nesneleri bir <xref:System.Collections.Generic.List%601> nesne.

- Kullanım bir `foreach` döngü Visual C# veya `For Each` bir listedeki öğeler arasında yineleme yapmak için Visual Basic'te döngü.

- Başvuru değişkenlerini kullanarak bir formun durumunu takip edin.

- Birden fazla nesneyle kullanabileceğiniz olaylara yanıt vermek için bir olay işleyicisi oluşturun.

- Geriye doğru sayan ve başlatılmasının ardından bir olayı kesin olarak tetikleyen bir zamanlayıcı hazırlayın.

Bu öğreticiyi tamamladığınızda, programınız aşağıdaki resim gibi görünecektir:

![Bu öğreticide oluşturduğunuz oyun](../ide/media/express_finishedgame.png)

## <a name="tutorial-links"></a>Öğretici bağlantıları

Örnek tamamlanmış bir sürümünü indirmek için bkz [eksiksiz eşleştirme oyunu Öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).

> [!NOTE]
> Bu öğreticide, hem Visual C# hem de Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.

Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz: [Visual Basic Forumu](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=vbgeneral) ve [Visual C# Forumu](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=csharpgeneral). Ayrıca, yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic'te programlama hakkında daha fazla bilgi için bkz: [Visual Basic temelleri: Yeni başlayanlar için geliştirme](https://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners). Görselde programlama hakkında daha fazla bilgi edinmek için C#, bkz: [ C# temelleri: Yeni başlayanlar için geliştirme](https://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners).

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[1. Adım: Proje oluşturma ve formunuza tablo ekleme](../ide/step-1-create-a-project-and-add-a-table-to-your-form.md)|Proje oluşturma ve ekleyerek başlayın bir `TableLayoutPanel` düzgün hizalanmasını denetimleri korumak için denetimi.|
|[2. Adım: Rasgele nesne ve simge listesi ekleme](../ide/step-2-add-a-random-object-and-a-list-of-icons.md)|Ekleme bir `Random` nesnesi ve bir `List` simge listesini oluşturmak için nesne.|
|[3. Adım: Her etikete rasgele simge atama](../ide/step-3-assign-a-random-icon-to-each-label.md)|Rasgele simgeleri atayın `Label` her oyunun farklı olması denetler.|
|[4. Adım: Her etikete click olay işleyicisi ekleme](../ide/step-4-add-a-click-event-handler-to-each-label.md)|Ekleme bir `Click` tıklanan etiketin rengini değiştiren olay işleyicisi.|
|[5. Adım: Etiket başvuruları ekleme](../ide/step-5-add-label-references.md)|Hangi etiketlere tıklandığını takip etmek için başvuru değişkenleri ekleyin.|
|[6. Adım: Zamanlayıcı ekleme](../ide/step-6-add-a-timer.md)|Oyunda geçen süreyi takip etmek için forma bir zamanlayıcı ekleyin.|
|[7. Adım: Çiftleri görünür kılma](../ide/step-7-keep-pairs-visible.md)|Eşleşen bir çift seçilirse, simge çiftlerini görünür durumda tutun.|
|[8. Adım: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md)|Ekleme bir `CheckForWinner()` oyuncunun kazanıp kazanmadığını doğrulamak için yöntem.|
|[9. Adım: Diğer özellikleri deneme](../ide/step-9-try-other-features.md)|Simgeleri ve renkleri değiştirme, kılavuz ekleme ve ses ekleme gibi diğer özellikleri deneyin. Tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.|
