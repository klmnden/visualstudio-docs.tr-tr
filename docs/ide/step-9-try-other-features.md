---
title: '9\. Adım: Diğer özellikleri deneme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
ms.assetid: 1b0c5c80-e5a6-4f69-a4a4-0e89a82d4de0
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6745b320d7f8c2d4d0434bf2410dc2ab37a288aa
ms.sourcegitcommit: 541a0556958201ad6626bc8638406ad02640f764
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2019
ms.locfileid: "71079335"
---
# <a name="step-9-try-other-features"></a>9\. Adım: Diğer özellikleri deneme
Daha fazla bilgi edinmek için simgeleri ve renkleri değiştirmeyi, oyun zamanlayıcısı ve sesler eklemeyi deneyin. Oyunu daha zorlu hale getirmek için tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.

Örneğin tamamlanmış bir sürümünü indirmek için, bkz. [tüm eşleşen oyun öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).

## <a name="to-try-other-features"></a>Diğer özellikleri denemek için

- Simgelerin ve renklerin yerine kendi tercih ettiklerinizi kullanın.

    > [!TIP]
    > Etiketin [ForeColor](<xref:System.Windows.Forms.Control.ForeColor%2A>) özelliğine bakmaya çalışın.

- Oyuncunun oyunu kazanmasının ne kadar sürdüğünü izleyen bir oyun zamanlayıcısı ekleyin.

    > [!TIP]
    > Bunu yapmak için, yukarıdaki <xref:System.Windows.Forms.TableLayoutPanel>formda geçen süreyi görüntüleyecek bir etiket ekleyebilirsiniz ve saati izlemek için forma başka bir zamanlayıcı ekleyebilirsiniz. Oyuncu oyuna başladığında zamanlayıcıyı başlatmak ve son iki simgeyi eşleştirdikten sonra zamanlayıcıyı durdurmak için kod kullanın.

- Oyuncu bir eşleşme bulduğunda çalacak bir ses, eşleşmeyen iki simgeyi açtığında çalacak başka bir ses ve program simgeleri yeniden gizlediğinde çalacak üçüncü bir ses ekleyin.

    > [!TIP]
    > Ses çalmak için <xref:System.Media> ad alanını kullanabilirsiniz. Daha fazla bilgi için bkz. [Windows FormsC#uygulamasında ses yürütme ()](http://youtu.be/qOh4ooHg1UU) veya [Visual Basic ses yürütme](http://youtu.be/-4oPDeQrtMs) .

- Oyun tahtasını büyüterek oyunu zorlaştırın.

    > [!TIP]
    > TableLayoutPanel 'e satırlar ve sütunlar eklemeniz yeterlidir. Ayrıca, oluşturduğunuz simge sayısını göz önünde bulundurmanız gerekir.

- Oyuncunun tepki verirken çok yavaş davranması ve belirli bir süre dolmadan önce ikinci simgeyi seçmemesi durumunda ilk simgeyi gizleyerek oyunu daha zorlu hale getirin.

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz. forum ve [görsel C# forumuna](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=csharpgeneral) [Visual Basic](https://social.msdn.microsoft.com/Forums/vstudio/home?forum=vbgeneral) .

- Yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic programlama hakkında daha fazla bilgi için bkz [. Visual Basic temelleri: Mutlak yeni başlayanlar](https://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners)için geliştirme. Görselde C#programlama hakkında daha fazla bilgi edinmek için [ bkz C# . temel bilgiler: Mutlak yeni başlayanlar](https://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners)için geliştirme.

- Önceki öğretici adımına dönmek için bkz [. 8. Adım: Oyuncunun kazanıp kazanılmadığını](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md)doğrulamak için bir yöntem ekleyin.
