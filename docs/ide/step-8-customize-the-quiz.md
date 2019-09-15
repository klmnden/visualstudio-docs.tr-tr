---
title: '8\. Adım: Testi özelleştirme'
ms.date: 11/04/2016
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
dev_langs:
- csharp
- vb
ms.assetid: dc8edb13-1b23-47d7-b859-8c6f7888c1a9
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b68d46ad5c585dca9fd48f39a2e47ac95f5a11c8
ms.sourcegitcommit: 0e482cfc15f809b564c3de61646f29ecd7bfcba6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/14/2019
ms.locfileid: "70987854"
---
# <a name="step-8-customize-the-quiz"></a>8\. Adım: Testi özelleştirme

Öğreticinin son bölümünde, testi özelleştirmenin ve daha önce öğrendiklerinizi genişletmenin bazı yollarını keşfedeceksiniz. Örneğin, programın yanıtın hiç bir kesir olmadığı rastgele bölüm sorunları nasıl oluşturduğunu düşünün. Daha fazla bilgi edinmek için, `timeLabel` denetimi farklı bir renk yapın ve sınava ipucu sunun.

> [!NOTE]
> Bu konu, temel kodlama kavramlarıyla ilgili bir öğretici serisinin bir parçasıdır. 
> - Öğreticiye genel bakış için bkz [. öğretici 2: Süreli bir matematik testi](../ide/tutorial-2-create-a-timed-math-quiz.md)oluşturun. 
> - Kodun tamamlanmış bir sürümünü indirmek için bkz. [tüm matematik testi öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).

## <a name="to-customize-the-quiz"></a>Testi özelleştirmek için

- Bir test içinde yalnızca beş saniye kaldığında, **BackColor** özelliğini ayarlayarak **timeLabel** denetimini kırmızıya dönüştürün.

  ```csharp
  timeLabel.BackColor = Color.Red;
  ```

  ```vb
  timeLabel.BackColor = Color.Red
  ```

  > [!IMPORTANT]
  > C# Kod parçacığını veya Visual Basic kod parçacığını görüntülemek için bu sayfanın sağ üst kısmındaki programlama dili denetimini kullanın.<br><br>![Docs.Microsoft.com için programlama dili denetimi](../ide/media/docs-programming-language-control.png)

  Test üzerindeyken rengi sıfırlayın.

- Bir <xref:System.Windows.Forms.NumericUpDown> denetime doğru yanıt girildiğinde, bir sesi oynatarak sınava ipucu sunun. (Her denetim <xref:System.Windows.Forms.NumericUpDown.ValueChanged> olayı için bir olay işleyicisi yazmanız gerekir ve bu, her bir test, denetimin değerini değiştirdiğinde harekete geçirilir.)

## <a name="to-continue-or-review"></a>Devam etmek veya gözden geçirmek için

- Sonraki öğreticiye gitmek için bkz  **[. öğretici 3: Eşleşen bir oyun](../ide/tutorial-3-create-a-matching-game.md)** oluşturun.

- Önceki öğretici adımına dönmek için bkz [. 7. Adım: Çarpma ve bölme sorunları](../ide/step-7-add-multiplication-and-division-problems.md)ekleyin.
