---
title: 'Öğretici 2: Zamanlı matematik testi oluşturma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: d7165d08-ace3-457d-b57d-fb8f80760a6f
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 39d8441620f9df135b2fbee51e2dfbbfc6e2f074
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943266"
---
# <a name="tutorial-2-create-a-timed-math-quiz"></a>Öğretici 2: Zamanlı matematik testi oluşturma

Bu öğreticide, sınava giren belirli bir süre içinde dört rastgele aritmetik sorusuna yanıtlamalısınız bir test oluşturun. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:

-   Kullanarak rastgele sayılar üretin <xref:System.Random> sınıfı.

-   Kullanarak belirli bir zamanda oluşacak olayları tetikleme bir <xref:System.Windows.Forms.Timer> denetimi.

-   Kullanarak program akışını denetleme `if else` deyimleri.

-   Kodda temel aritmetik işlemleri gerçekleştirin.

İşiniz bittiğinde, sınav aşağıdaki resim gibi dışında sayıların farklı görünecektir:

![Dört Sorulu matematik sınavı](../ide/media/express_finishedquiz.png)

## <a name="tutorial-links"></a>Öğretici bağlantıları

Sınavın tamamlanmış bir sürümünü indirmek için bkz [tam matematik sınavı öğretici örneği](https://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).

> [!NOTE]
> Bu öğreticide hem Visual C# ve Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[1. adım: Proje oluşturma ve formunuza etiketler ekleme](../ide/step-1-create-a-project-and-add-labels-to-your-form.md)|Başlangıç projesi oluşturma özelliklerini değiştirme ve ekleme `Label` kontrol eder.|
|[2. adım: Rasgele bir toplama problemi oluşturma](../ide/step-2-create-a-random-addition-problem.md)|Bir toplama problemi oluşturma ve kullanma `Random` sınıfını kullanarak rastgele sayılar üretin.|
|[3. adım: Bir geri sayım Zamanlayıcısı ekleme](../ide/step-3-add-a-countdown-timer.md)|Sınav zamanlanabilir geri sayım Zamanlayıcısı ekleyin.|
|[4. adım: CheckTheAnswer() yöntemi ekleme](../ide/step-4-add-the-checktheanswer-parens-method.md)|Sınava sorun için doğru yanıtı girilen olup olmadığını denetlemek için bir yöntem ekleyin.|
|[5. adım: ENTER NumericUpDown denetimleri için olay işleyicileri ekleme](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)|Sınav olması daha kolay hale getirmek olay işleyicileri ekleyin.|
|[6. adım: Çıkarma problemi ekleme](../ide/step-6-add-a-subtraction-problem.md)|Rastgele sayılar üreten, Zamanlayıcı kullanan ve doğru yanıtları denetleyen bir çıkarma sorusu ekleyin.|
|[7. adım: Çarpma ve bölme soruları ekleyin](../ide/step-7-add-multiplication-and-division-problems.md)|Rastgele sayılar üretin, Zamanlayıcı kullanan ve doğru yanıtları denetleyen çarpma ve bölme soruları ekleyin.|
|[8. adım: Testi özelleştirme](../ide/step-8-customize-the-quiz.md)|Renkleri değiştirme ve ipucu ekleme gibi diğer özellikleri deneyin.|
