---
title: 'Öğretici 2: Süreli matematik testi oluşturma'
ms.date: 11/04/2016
ms.assetid: d7165d08-ace3-457d-b57d-fb8f80760a6f
ms.topic: tutorial
ms.technology: vs-ide-general
ms.devlang:
- csharp
- vb
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c0c7f3695be87f6cb4081b3aa02fc7a129869a4c
ms.sourcegitcommit: 9c07ae6fb18204ea080c8248994a683fa12e5c82
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2019
ms.locfileid: "70293690"
---
# <a name="tutorial-2-create-a-timed-math-quiz"></a>Öğretici 2: Süreli matematik testi oluşturma

Bu öğreticide, bir sınavın belirli bir süre içinde dört rastgele aritmetik sorunu yanıtlaması gereken bir test oluşturacaksınız. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:

- <xref:System.Random> Sınıfını kullanarak rastgele sayılar üretin.

- Olayları bir <xref:System.Windows.Forms.Timer> denetim kullanarak belirli bir zamanda gerçekleşecek şekilde tetikleyin.

- Deyimlerini kullanarak `if else` program akışını denetleme.

- Kodda temel aritmetik işlemler gerçekleştirin.

Bitirdiğinizde, test, farklı sayılar dışında aşağıdaki resme benzer şekilde görünür:

![Dört problemle matematik sınavından](../ide/media/express_finishedquiz.png)

## <a name="tutorial-links"></a>Öğretici bağlantıları

Sınavın tamamlanmış bir sürümünü indirmek için bkz. [tüm matematik testi öğreticisi örneği](https://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).

> [!NOTE]
> Bu öğreticide hem görsel C# hem de Visual Basic ele alınmaktadır, bu nedenle kullandığınız programlama diline özgü bilgilere odaklanırsınız.

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[1. Adım: Formunuza bir proje oluşturun ve Etiketler ekleyin](../ide/step-1-create-a-project-and-add-labels-to-your-form.md)|Projeyi oluşturarak, özellikleri değiştirerek ve denetimler ekleyerek `Label` başlayın.|
|[2. Adım: Rastgele bir ek sorun oluşturma](../ide/step-2-create-a-random-addition-problem.md)|Ek bir sorun oluşturun ve rastgele sayılar oluşturmak `Random` için sınıfını kullanın.|
|[3. Adım: Geri sayım ekleme süreölçeri](../ide/step-3-add-a-countdown-timer.md)|Sınavın zaman aşımına uğraabilmesi için bir geri sayım Zamanlayıcısı ekleyin.|
|[4. Adım: CheckTheAnswer () yöntemini ekleyin](../ide/step-4-add-the-checktheanswer-parens-method.md)|Sınavın sorun için doğru bir yanıt girmediğini denetlemek için bir yöntem ekleyin.|
|[5. Adım: NumericUpDown denetimleri için Enter Olay işleyicileri ekleme](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)|Sınavını daha kolay hale getirmek için olay işleyicileri ekleyin.|
|[6. Adım: Çıkarma sorunu ekleme](../ide/step-6-add-a-subtraction-problem.md)|Rastgele sayılar üreten, Zamanlayıcı kullanan ve doğru yanıtları denetleyen bir çıkarma sorunu ekleyin.|
|[7. Adım: Çarpma ve bölme sorunları ekleme](../ide/step-7-add-multiplication-and-division-problems.md)|Rastgele sayılar üreten çarpma ve bölme sorunları ekleyin, zamanlayıcıyı kullanın ve doğru yanıtları denetleyin.|
|[8. Adım: Testi özelleştirme](../ide/step-8-customize-the-quiz.md)|Renkleri değiştirme ve ipucu ekleme gibi diğer özellikleri deneyin.|
