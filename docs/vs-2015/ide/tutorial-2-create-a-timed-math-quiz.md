---
title: 'Öğretici 2: Zamanlı matematik testi oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: d7165d08-ace3-457d-b57d-fb8f80760a6f
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2a87a192f7a14a4d59a5ca5cff15bc62abbdefc6
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443281"
---
# <a name="tutorial-2-create-a-timed-math-quiz"></a>Öğretici 2: Zamanlı matematik testi oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu öğreticide, sınava giren belirli bir süre içinde dört rastgele aritmetik sorusuna yanıtlamalısınız bir test oluşturun. Aşağıdakilerin nasıl yapıldığını öğreneceksiniz:  
  
- Kullanarak rastgele sayılar üretin `Random` sınıfı.  
  
- Kullanarak belirli bir zamanda oluşacak olayları tetikleme bir **Zamanlayıcı** denetimi.  
  
- Kullanarak program akışını denetleme `if else` deyimleri.  
  
- Kodda temel aritmetik işlemleri gerçekleştirin.  
  
  İşiniz bittiğinde, sınav aşağıdaki resim gibi dışında sayıların farklı görünecektir.  
  
  ![Dört Sorulu matematik sınavı](../ide/media/express-finishedquiz.png "Express_FinishedQuiz")  
  Bu öğreticide oluşturduğunuz sınav  
  
  Sınavın tamamlanmış bir sürümünü indirmek için bkz [matematik sınavı öğretici örneği](http://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).  
  
> [!NOTE]
> Bu öğreticide hem Visual C# ve Visual Basic ele alınmaktadır; bu nedenle kullandığınız programlama diline özgü bilgilere odaklanın.  
  
## <a name="related-topics"></a>İlgili Konular  
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[1. Adım: Proje Oluşturma ve Formunuza Etiketler Ekleme](../ide/step-1-create-a-project-and-add-labels-to-your-form.md)|Başlangıç projesi oluşturma özelliklerini değiştirme ve ekleme `Label` kontrol eder.|  
|[2. Adım: Rastgele Bir Toplama Problemi Oluşturma](../ide/step-2-create-a-random-addition-problem.md)|Bir toplama problemi oluşturma ve kullanma `Random` sınıfını kullanarak rastgele sayılar üretin.|  
|[3. Adım: Geri Sayım Zamanlayıcısı Ekleme](../ide/step-3-add-a-countdown-timer.md)|Sınav zamanlanabilir geri sayım Zamanlayıcısı ekleyin.|  
|[4. Adım: CheckTheAnswer() Yöntemi Ekleme](../ide/step-4-add-the-checktheanswer-parens-method.md)|Sınava sorun için doğru yanıtı girilen olup olmadığını denetlemek için bir yöntem ekleyin.|  
|[5. Adım: NumericUpDown Denetimleri için Giriş Olay İşleyicileri Ekleme](../ide/step-5-add-enter-event-handlers-for-the-numericupdown-controls.md)|Sınav olması daha kolay hale getirmek olay işleyicileri ekleyin.|  
|[6. Adım: Çıkarma Problemi Ekleme](../ide/step-6-add-a-subtraction-problem.md)|Rastgele sayılar üreten, Zamanlayıcı kullanan ve doğru yanıtları denetleyen bir çıkarma sorusu ekleyin.|  
|[7. Adım: Çarpma ve Bölme Problemleri Ekleme](../ide/step-7-add-multiplication-and-division-problems.md)|Rastgele sayılar üretin, Zamanlayıcı kullanan ve doğru yanıtları denetleyen çarpma ve bölme soruları ekleyin.|  
|[8. Adım: Testi Özelleştirme](../ide/step-8-customize-the-quiz.md)|Renkleri değiştirme ve ipucu ekleme gibi diğer özellikleri deneyin.|
