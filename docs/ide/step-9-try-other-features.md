---
title: '9. Adım: Diğer özellikleri deneme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1b0c5c80-e5a6-4f69-a4a4-0e89a82d4de0
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d2d32a0d2e208b5f8bfd7869c8dfa92f063f1db5
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55925949"
---
# <a name="step-9-try-other-features"></a>9. Adım: Diğer özellikleri deneme
Daha fazla bilgi edinmek için simgeleri ve renkleri değiştirmeyi, oyun zamanlayıcısı ve sesler eklemeyi deneyin. Oyunu daha zorlu hale getirmek için tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.

 Örnek tamamlanmış bir sürümünü indirmek için bkz [eksiksiz eşleştirme oyunu Öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).

## <a name="to-try-other-features"></a>Diğer özellikleri denemek için

-   Simgelerin ve renklerin yerine kendi tercih ettiklerinizi kullanın.

    > [!TIP]
    >  Etiketin bakmayın deneyin [Forecolor](<xref:System.Windows.Forms.Control.ForeColor%2A>) özelliği.

-   Oyuncunun oyunu kazanmasının ne kadar sürdüğünü izleyen bir oyun zamanlayıcısı ekleyin.

    > [!TIP]
    >  Bunu yapmak için yukarıdaki forma geçen süreyi gösterecek bir etiket ekleyebilirsiniz <xref:System.Windows.Forms.TableLayoutPanel>, ve süreyi izlemek için forma bir diğer Zamanlayıcı ekleyin. Oyuncu oyuna başladığında zamanlayıcıyı başlatmak ve son iki simgeyi eşleştirdikten sonra zamanlayıcıyı durdurmak için kod kullanın.

-   Oyuncu bir eşleşme bulduğunda çalacak bir ses, eşleşmeyen iki simgeyi açtığında çalacak başka bir ses ve program simgeleri yeniden gizlediğinde çalacak üçüncü bir ses ekleyin.

    > [!TIP]
    >  Sesleri çalmak için kullanabileceğiniz <xref:System.Media> ad alanı. Bkz: [Windows Forms uygulamasında sesleri çalmak (C#)](http://youtu.be/qOh4ooHg1UU) veya [Visual Basic'te ses kaydını oynatın nasıl](http://youtu.be/-4oPDeQrtMs) daha fazla bilgi için.

-   Oyun tahtasını büyüterek oyunu zorlaştırın.

    > [!TIP]
    >  Daha fazlasını satırları ve sütunları TableLayoutPanel denetimine - eklemeniz gerekir, ayrıca oluşturduğunuz simge sayısını göz önünde bulundurmanız gerekir.

-   Oyuncunun tepki verirken çok yavaş davranması ve belirli bir süre dolmadan önce ikinci simgeyi seçmemesi durumunda ilk simgeyi gizleyerek oyunu daha zorlu hale getirin.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

-   Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz: [Visual Basic Forumu](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=vbgeneral) ve [Visual C# Forumu](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=csharpgeneral).

-   Yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic'te programlama hakkında daha fazla bilgi için bkz: [Visual Basic temelleri: Yeni başlayanlar için geliştirme](https://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners). Görselde programlama hakkında daha fazla bilgi edinmek için C#, bkz: [ C# temelleri: Yeni başlayanlar için geliştirme](https://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners).

-   Önceki öğretici adımına dönmek için bkz: [adım 8: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md).
