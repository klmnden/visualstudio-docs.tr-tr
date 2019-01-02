---
title: '8. Adım: Testi özelleştirme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: dc8edb13-1b23-47d7-b859-8c6f7888c1a9
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f2b2f9d46b623f63d216ce530cd283bf799a3a73
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53842362"
---
# <a name="step-8-customize-the-quiz"></a>8. Adım: Testi özelleştirme
Öğreticinin son bölümünde testi özelleştirme ve zaten öğrendiklerinizi üzerinde genişletmek için bazı yollar hakkında bilgi edineceksiniz. Örneğin, programın yanıt hiçbir zaman bir kesir olduğu rastgele bölme problemleri nasıl oluşturduğunu hakkında düşünün. Daha fazla bilgi için kapatma `timeLabel` farklı bir renkte denetlemek ve sınava giren bir ipucu verir.  

## <a name="to-customize-the-quiz"></a>Test özelleştirmek için  

-   Yalnızca beş saniyede bir sınavda kalan zaman **timeLabel** denetiminde kırmızı renkte ayarlayarak onun **BackColor** özelliği (`timeLabel.BackColor = Color.Red;`). Test bittiğinde rengi sıfırlayın.  
  
-   Sınava halinde doğru yanıtı girildiğinde ses çalma bir ipucu verir. bir <xref:System.Windows.Forms.NumericUpDown> denetimi. (Her denetim için bir olay işleyicisi yazmanız gereken <xref:System.Windows.Forms.NumericUpDown.ValueChanged> sınava denetimin değeri değiştiğinde harekete olayı,.)  
  
## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için  
  
-   Sınavın tamamlanmış bir sürümünü indirmek için bkz [tam matematik sınavı öğretici örneği](https://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).  
  
-   Sonraki eğitime gitmek için bkz: [Tutorial 3: Eşleşen bir oluşturma oyun](../ide/tutorial-3-create-a-matching-game.md).  
  
-   Önceki öğretici adımına dönmek için bkz: [adım 7: Çarpma ve bölme soruları ekleyin](../ide/step-7-add-multiplication-and-division-problems.md).
