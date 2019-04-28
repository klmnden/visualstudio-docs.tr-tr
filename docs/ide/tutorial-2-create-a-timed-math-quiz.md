---
title: 'Öğretici 2: Zamanlı matematik testi oluşturma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d7165d08-ace3-457d-b57d-fb8f80760a6f
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4ececa58d04ea7cfebe6178faae724038e353f06
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62821636"
---
# <a name="tutorial-2-create-a-timed-math-quiz"></a>Öğretici 2: Zamanlı matematik testi oluşturma

Bu öğreticide, sınava giren belirli bir süre içinde dört rastgele aritmetik sorusuna yanıtlamalısınız bir test oluşturun. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:

- Kullanarak rastgele sayılar üretin <xref:System.Random> sınıfı.

- Kullanarak belirli bir zamanda oluşacak olayları tetikleme bir <xref:System.Windows.Forms.Timer> denetimi.

- Kullanarak program akışını denetleme `if else` deyimleri.

- Kodda temel aritmetik işlemleri gerçekleştirin.

İşiniz bittiğinde, sınav aşağıdaki resim gibi dışında sayıların farklı görünecektir:

![Dört Sorulu matematik sınavı](../ide/media/express_finishedquiz.png)

## <a name="tutorial-links"></a>Öğretici bağlantıları

Sınavın tamamlanmış bir sürümünü indirmek için bkz [tam matematik sınavı öğretici örneği](https://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).

> [!NOTE]
> Bu öğreticide hem Visual C# ve Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[1. Adım: Proje oluşturma ve formunuza etiketler ekleme](../ide/step-1-create-a-project-and-add-labels-to-your-form.md)|Başlangıç projesi oluşturma özelliklerini değiştirme ve ekleme `Label` kontrol eder.|
|[2. Adım: Rasgele bir toplama problemi oluşturma](../ide/step-2-create-a-random-addition-problem.md)|Bir toplama problemi oluşturma ve kullanma `Random` sınıfını kullanarak rastgele sayılar üretin.|
|[3. Adım: Bir geri sayım Zamanlayıcısı ekleme](../ide/step-3-add-a-countdown-timer.md)|Sınav zamanlanabilir geri sayım Zamanlayıcısı ekleyin.|
|[4. Adım: CheckTheAnswer() yöntemi ekleme](../ide/step-4-add-the-checktheanswer-parens-method.md)|Sınava sorun için doğru yanıtı girilen olup olmadığını denetlemek için bir yöntem ekleyin.|
|[5. Adım: ENTER NumericUpDown denetimleri için olay işleyicileri ekleme](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)|Sınav olması daha kolay hale getirmek olay işleyicileri ekleyin.|
|[6. Adım: Çıkarma problemi ekleme](../ide/step-6-add-a-subtraction-problem.md)|Rastgele sayılar üreten, Zamanlayıcı kullanan ve doğru yanıtları denetleyen bir çıkarma sorusu ekleyin.|
|[7. Adım: Çarpma ve bölme soruları ekleyin](../ide/step-7-add-multiplication-and-division-problems.md)|Rastgele sayılar üretin, Zamanlayıcı kullanan ve doğru yanıtları denetleyen çarpma ve bölme soruları ekleyin.|
|[8. Adım: Testi özelleştirme](../ide/step-8-customize-the-quiz.md)|Renkleri değiştirme ve ipucu ekleme gibi diğer özellikleri deneyin.|
