---
title: Kodlanmış web performans testleri
ms.date: 10/03/2016
ms.topic: conceptual
helpviewer_keywords:
- Web performance tests, walkthroughs
- Web performance tests, creating
- code, Web performance tests
- Web performance tests, coded
ms.assetid: 169e48f9-52fd-4d0b-83d9-54913bde506b
dev_langs:
- CSharp
- VB
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: a6f1c524b879d5d5476491a8979d86449f3d43c0
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60086409"
---
# <a name="generate-and-run-a-coded-web-performance-test"></a>Kodlanmış web performans testi oluşturma

Web performans testleri, web uygulamanızla göz atarak kaydedilir. Testler, birden çok kullanıcının baskısı altındaki web uygulamanızın performansını ölçmek için yük testlerinde dahil edilir. Web performans testini düzenleme ve özelleştirme gibi başka bir kaynak kodu bir kod tabanlı betiğe dönüştürülebilir. Örneğin, döngü ve dal oluşturma yapıları ekleyebilirsiniz.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="generate-a-coded-web-performance-test"></a>Kodlanmış web performans testi üret

1. Web performans testi oluşturmadıysanız bkz [web performans testi](/azure/devops/test/load-test/run-performance-tests-app-before-release#create-a-web-performance-and-load-test-project).

2. Kodlanmış test üretin.

     ![Kodlanmış web performans testi üret](../test/media/web_test_coded_generate.png)

3. Testi adlandırın.

     ![Kodlanmış web performans testi için bir ad girin](../test/media/web_test_coded_generate_nametest.png)

     Yeni kodlanmış test kod düzenleyicisinde açılır.

     Hangi web performansı ve yük testi proje şablonunu, çözümünüze eklediğiniz bağlı olarak, kod Visual Basic, veya Visual C# içinde oluşturulur.

     ![Yeni kodlanmış test kod düzenleyicisinde açılır.](../test/media/web_test_coded_generate_opencodeeditor.png)

     Kodda, GetRequestEnumerator() yönteminde C# veya Visual Basic uygulamasındaki Run() yönteminde yönteminde olduğu her doğrulama kuralının ve web isteğinin bulunduğunu görebilirsiniz.

4. Bazı basit kod eklemenin nasıl yapılacağını göstermek için yöntemin ve son web isteğine ilişkin koddan sonra aşağı kaydırın ve aşağıdaki kodu ekleyin:

    ```c#
    if (DateTime.Today.DayOfWeek == DayOfWeek.Wednesday)
    {
        WebTestRequest customRequest = new WebTestRequest("http://weather.msn.com/");
        yield return customRequest;
    }
    else
    {
        WebTestRequest customRequest = new WebTestRequest("https://msdn.microsoft.com/");
        yield return customRequest;
    }
    ```

    ```vb
    If DateTime.Today.DayOfWeek = DayOfWeek.Wednesday Then
        Dim customRequest As WebTestRequest = New WebTestRequest("http://weather.msn.com/")
        MyBase.Send(customRequest)
    Else
        Dim customRequest As WebTestRequest = New WebTestRequest("https://msdn.microsoft.com/")
        MyBase.Send(customRequest)
    End If
    ```

5. Özel kodunuzun derlendiğinden emin doğrulamak için çözümü oluşturun.

6. Testi çalıştırın.

     ![Kodlanmış web performans testini çalıştırma](../test/media/web_test_coded_generate_run.png)

     Ve bunun çalıştırıldığı gün Çarşamba olduğundan...

     ![Kodlanmış web performans test sonuçları](../test/media/web_test_coded_generate_results.png)

## <a name="qa"></a>SORU- CEVAP

### <a name="q-can-i-run-more-than-one-test-at-a-time"></a>S: Aynı anda birden fazla test çalıştırabilir miyim?
 **Y:** Evet, (bağlam) sağ tıklama menüsünde kullanmak **Çözüm Gezgini**.

### <a name="q-should-i-add-a-data-source-before-or-after-i-generate-a-coded-test"></a>S: Bir veri kaynağı miyim kodlanmış test üretmeden önce veya sonra eklemeniz gerekir?
 **Y:** Eklemek daha kolay bir [veri kaynağı](../test/add-a-data-source-to-a-web-performance-test.md) kodu otomatik olarak sizin için oluşturulacağından Kodlanmış testi oluşturmadan önce.

 Bir veri kaynağı ile kodlanmış bir test çalıştırdığınızda, aşağıdaki hata iletisini görebilirsiniz:

 **Test çalıştırılamadı \<Test adı > aracıdaki \<bilgisayar adı >: Nesne başvurusu bir nesnenin örneğine ayarlı değil.**

 Bu, karşılık gelen bir DataBindingAttribute olmadan test sınıfı için tanımlanan DataSourceAttribute öğesine sahip olduğundan ortaya çıkabilir. Bu hatayı gidermek için uygun bir DataBindingAttribute ekleyin, silin veya açıklama olarak kodun dışına.

### <a name="q-should-i-add-validation-and-extraction-rules-before-or-after-i-generate-a-coded-test"></a>S: Ben bir kodlanmış test üretmeden önce veya sonra doğrulama ve ayıklama kuralları eklemeliyim?
 **Y:** Kodlanmış testi oluşturmadan önce doğrulama kuralları ve ayıklama kuralları eklemek kolaydır; Ancak, kullanmanızı öneririz [kodlanmış UI testleri](../test/use-ui-automation-to-test-your-code.md) doğrulama amacıyla.