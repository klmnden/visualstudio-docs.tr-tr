---
title: Doğrulama ve SharePoint kod hata ayıklama | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- unit testing [SharePoint development in Visual Studio]
- IntelliTrace [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, IntelliTrace
- SharePoint development in Visual Studio, unit testing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7b57e07245631d37594d66ea7907b16efd817b2b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63008271"
---
# <a name="verify-and-debug-sharepoint-code"></a>Doğrulayın ve SharePoint kodu hatalarını ayıklama
IntelliTrace ve birim testi kullanarak daha kolay hata ayıklama, SharePoint çözümleri ve her bir yöntemde düzgün çalıştığından emin olun. Bu özellikler, diğer proje türleri için aynı yordamları izleyerek Visual Studio'da SharePoint projeleri için kullanabilirsiniz.

## <a name="intellitrace"></a>IntelliTrace
IntelliTrace kullanarak, yalnızca geçerli durumu, SharePoint çözüm aynı zamanda geçmiş ve gerçekleşen bağlam içinde oluşan olaylar belirleyebilirsiniz. Çeşitli noktalara sürede SharePoint çözümünüzü nerede olaylarının kaydedilmiş geri ve İleri gidin ve durumları ve her noktasında değişkenlerin değerlerini gözden geçirin. Bu dinamik Gezinti kullanarak, daha hızlı ve kolay bir şekilde, SharePoint çözümleri çok sayıda kesme noktaları ayarlamak zorunda kalmadan ayıklayabilirsiniz. Hata ayıklama oturumunu bir IntelliTrace günlüğüne kaydedebilirsiniz (*.iTrace*) dosya, daha sonra Visual Studio Enterprise'da açın ve sonrası kilitlenme hata ayıklama gerçekleştirin. *.İTrace* dosyası hatalara neden kullanıma daha kolay anlayabilir, ne zaman ve nerede belirli SharePoint hatalar oluştu hakkında ayrıntılı bilgi içerir. Bilgileri *.iTrace* dosya birleşik günlük kaydetme sistemi (ULS) SharePoint oluşturan tam hata günlüğü bir alt kümesidir. Bu bilgiler, bir kullanıcı profili ne zaman açılacakları veya gibi ve özelliklerini bir SharePoint Proje yüklenir, okuma, veya değiştirildiğinde SharePoint için belirli olayları içerir. Intellitrace'in kaydettiği olayları yapılandırabilirsiniz. Daha fazla bilgi için [kayıtlı IntelliTrace verilerini kullanma](../debugger/using-saved-intellitrace-data.md).

SharePoint'te bir hata oluştuğunda, hata iletişim kutusu "bağıntı kimliği" tanımlayıcısı için belirli bir hata görüntüler. Bağıntı kimlikleri listelenen olaylardan alabilirsiniz *.iTrace* dosya. Tüm belirtilen bağıntı kimliği ile gerçekleşen olayların listesini görüntülemek için Kimliğini girebilirsiniz **analiz** IntelliTrace Özet sayfasının bölümü. Bu bölümde, yalnızca oluşan olaylar adlarını veya işlev adı, çıkış ve giriş noktaları, parametreler ve dönüş değerleri gibi çağrı bilgileri ile birlikte olayları adlarını görüntülenip görüntülenmeyeceğini seçebilirsiniz.

IntelliTrace in Visual Studio olayları seçerek alabilirsiniz **F5** anahtarı. SharePoint'e özgü olaylar almak için ancak SharePoint çözümlerinde IntelliTrace verilerini Microsoft Monitoring Agent'ı kullanarak topladığınız gerekir. Bu araç, IntelliTrace verilerini toplar ve oluşturur *.iTrace* dosyaları Visual Studio'nun dışında dağıtılan uygulamalar için. Daha fazla bilgi için [IntelliTrace özellikleri](../debugger/intellitrace-features.md) ve [IntelliTrace collector kullanarak](../debugger/using-the-intellitrace-stand-alone-collector.md).

## <a name="unit-test"></a>Birim testi
Kodunuzda, yazma ve test kodu içinde test yöntemleri çalıştırmak birim testi, gerçekleştirerek, hataları daha kolay bulabilirsiniz. Bu yöntemler, boş değişkenleri ve mantık ve projenizin SharePoint nesne modelini temel işlevselliğini doğrulamak için kullanabileceğiniz bir onay deyimi içerir. Daha fazla bilgi için [Birim Test kodunuzu](../test/unit-test-your-code.md).

### <a name="support-for-microsoft-fakes-framework"></a>Microsoft Fakes framework desteği
Temsilci tabanlı oluşturabilirsiniz bir yalıtım çerçevesi olan Microsoft Fakes, SharePoint projeleri desteği, .NET Framework tabanlı uygulamalarda saptamalar ve dolgular sınayın. Fakes Çerçevesi'ni kullanarak, oluşturmak, korumak ve birim testlerinizi işlevsiz uygulamaları ekleme. Bu saptamalar ve dolgular ortamından birim testlerini yalıtmak. Geçersiz kılınabilir yönteme sahip arabirimleri veya Mühürlü olmayan sınıflar kullanan kodu test etmek için saplamalar oluşturabilirsiniz. Sealed sınıfları statik veya kılınamaz yöntemleriyle sabit kodlanmış çağrısına bir alternatif dolgu uygulamasına yeniden yönlendirmek için dolgular oluşturabilirsiniz. Temsilciler Shim/dolgu türlerini ve Koçan türleri ile dinamik olarak tek bir saplama üyeleri davranışını özelleştirmek için kullanabilirsiniz. Daha fazla bilgi için [yalıtma kod altında Microsoft Fakes ile Test](../test/isolating-code-under-test-with-microsoft-fakes.md).

## <a name="related-articles"></a>İlgili makaleler

|Başlık|Açıklama|
|-----------|-----------------|
|[IntelliTrace](../debugger/intellitrace.md)|IntelliTrace kullanarak Visual Studio çözümleri daha kolay hata ayıklama işlemini açıklamaktadır.|
|[İzlenecek yol: IntelliTrace'i kullanarak SharePoint uygulamasında hata ayıklama](../sharepoint/walkthrough-debugging-a-sharepoint-application-by-using-intellitrace.md)|Nasıl bulunacağını gösterir IntelliTrace'i kullanarak SharePoint projesindeki hataları kodlama.|
|[Kodunuza Birim Testi Uygulama](../test/unit-test-your-code.md)|Birim testler kullanılarak kodunuzda mantık hataları bulmak açıklar.|

## <a name="see-also"></a>Ayrıca bkz.

- [Kod Kalitesini Geliştirme](../test/improve-code-quality.md)