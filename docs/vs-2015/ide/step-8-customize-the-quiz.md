---
title: '8. Adım: Testi özelleştirme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: dc8edb13-1b23-47d7-b859-8c6f7888c1a9
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 413a0cb2f1445f166f1a5c9e541b2a4268ff2e31
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54776091"
---
# <a name="step-8-customize-the-quiz"></a>8. Adım: Testi Özelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Öğreticinin son bölümünde testi özelleştirme ve zaten öğrendiklerinizi üzerinde genişletmek için bazı yollar hakkında bilgi edineceksiniz. Örneğin, programın yanıt hiçbir zaman bir kesir olduğu rastgele bölme problemleri nasıl oluşturduğunu hakkında düşünün. Daha fazla bilgi için kapatma `timeLabel` farklı bir renkte denetlemek ve sınava giren bir ipucu verir.  
  
### <a name="to-customize-the-quiz"></a>Test özelleştirmek için  
  
-   Yalnızca beş saniyede bir sınavda kalan zaman **timeLabel** denetiminde kırmızı renkte ayarlayarak onun **BackColor** özelliği (`timeLabel.BackColor = Color.Red;`). Test bittiğinde rengi sıfırlayın.  
  
-   Sınava giren bir NumericUpDown denetimine doğru yanıtı girildiğinde ses çalma bir ipucu verir. (Her denetim için bir olay işleyicisi yazmanız gereken `ValueChanged()` sınava denetimin değeri değiştiğinde harekete olayı,.)  
  
### <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
-   Sınavın tamamlanmış bir sürümünü indirmek için bkz [matematik sınavı öğretici örneği](http://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).  
  
-   Sonraki eğitime gitmek için bkz: [Tutorial 3: Bir eşleştirme oyunu oluşturmak](../ide/tutorial-3-create-a-matching-game.md).  
  
-   Önceki öğretici adımına dönmek için bkz: [adım 7: Çarpma ve bölme problemleri ekleme](../ide/step-7-add-multiplication-and-division-problems.md).
