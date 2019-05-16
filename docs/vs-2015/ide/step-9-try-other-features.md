---
title: '9. Adım: Diğer özellikleri deneyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 1b0c5c80-e5a6-4f69-a4a4-0e89a82d4de0
caps.latest.revision: 13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 495d98f4061c258c78b2b74929428aec4eb3ec0c
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65678938"
---
# <a name="step-9-try-other-features"></a>9. Adım: Diğer Özellikleri Deneme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Daha fazla bilgi edinmek için simgeleri ve renkleri değiştirmeyi, oyun zamanlayıcısı ve sesler eklemeyi deneyin. Oyunu daha zorlu hale getirmek için tahtayı büyütmeyi ve zamanlayıcıyı ayarlamayı deneyin.  
  
 Örnek tamamlanmış bir sürümünü indirmek için bkz [eksiksiz eşleştirme oyunu Öğreticisi örneği](http://code.msdn.microsoft.com/Complete-Matching-Game-4cffddba).  
  
### <a name="to-try-other-features"></a>Diğer özellikleri denemek için  
  
- Simgelerin ve renklerin yerine kendi tercih ettiklerinizi kullanın.  
  
    > [!TIP]
    > Etiketin bakmayın deneyin [Forecolor](https://msdn.microsoft.com/library/system.windows.forms.control.forecolor%28v=vs.110%29.aspx) özelliği.  
  
- Oyuncunun oyunu kazanmasının ne kadar sürdüğünü izleyen bir oyun zamanlayıcısı ekleyin.  
  
    > [!TIP]
    > Bunun için, TableLayoutPanel üzerindeki forma geçen süreyi gösterecek bir etiket ekleyebilir ve süreyi izlemek için de forma bir diğer zamanlayıcı ekleyebilirsiniz. Oyuncu oyuna başladığında zamanlayıcıyı başlatmak ve son iki simgeyi eşleştirdikten sonra zamanlayıcıyı durdurmak için kod kullanın.  
  
- Oyuncu bir eşleşme bulduğunda çalacak bir ses, eşleşmeyen iki simgeyi açtığında çalacak başka bir ses ve program simgeleri yeniden gizlediğinde çalacak üçüncü bir ses ekleyin.  
  
    > [!TIP]
    > Sesleri çalmak için System.media ad alanını kullanabilirsiniz. Bkz: [Play Sounds in Windows Forms uygulaması (C# .NET)](http://youtu.be/qOh4ooHg1UU) veya [nasıl için Play Audio ın Visual Basic](http://youtu.be/-4oPDeQrtMs) daha fazla bilgi için.  
  
- Oyun tahtasını büyüterek oyunu zorlaştırın.  
  
    > [!TIP]
    > TableLayoutPanel denetimine satır ve sütunları eklemekten fazlasını yapmanız ve oluşturduğunuz simge sayısını da düşünmeniz gerekir.  
  
- Oyuncunun tepki verirken çok yavaş davranması ve belirli bir süre dolmadan önce ikinci simgeyi seçmemesi durumunda ilk simgeyi gizleyerek oyunu daha zorlu hale getirin.  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
- Bir yerde tıkanıp kalırsanız veya programlamayla ilgili sorularınız olursa, MSDN forumlarından birinde sorunuzu göndermeyi deneyin. Bkz: [Visual Basic Forumu](http://social.msdn.microsoft.com/Forums/home?forum=vbgeneral) ve [Visual C# Forumu](http://social.msdn.microsoft.com/Forums/home?forum=csharpgeneral).  
  
- Yararlanabileceğiniz harika ve ücretsiz video öğrenme kaynakları vardır. Visual Basic'te programlama hakkında daha fazla bilgi için bkz: [Visual Basic temelleri: Yeni başlayanlar için geliştirme](http://channel9.msdn.com/Series/Visual-Basic-Development-for-Absolute-Beginners). Görselde programlama hakkında daha fazla bilgi edinmek için C#, bkz: [ C# temelleri: Yeni başlayanlar için geliştirme](http://channel9.msdn.com/Series/C-Sharp-Fundamentals-Development-for-Absolute-Beginners).  
  
- Önceki öğretici adımına dönmek için bkz: [adım 8: Oyuncunun kazanıp kazanmadığını doğrulamak için yöntem ekleme](../ide/step-8-add-a-method-to-verify-whether-the-player-won.md).
