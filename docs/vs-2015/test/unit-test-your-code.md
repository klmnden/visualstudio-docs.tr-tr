---
title: Birim testi kod | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio, unit tests
- unit tests, verifying code with
- testing code, automated tests
ms.assetid: c191de3e-3f3b-471e-b828-29ec24e80e2c
caps.latest.revision: 64
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2dfde0684e721b1ed4834d23fb9fc56363f9fb0b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782714"
---
# <a name="unit-test-your-code"></a>Kodunuza Birim Testi Uygulama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Birim testleri, sınıfların yöntemlerinde mantık hataları aramak için hızlı bir şekilde geliştiricilere ve test edicilere vermek [!INCLUDE[csharp_current_short](../includes/csharp-current-short-md.md)], [!INCLUDE[vb_current_short](../includes/vb-current-short-md.md)], ve [!INCLUDE[cpp_current_short](../includes/cpp-current-short-md.md)] projeleri.  
  
 Birim testi araçları şunları içerir:  
  
1. **Test Gezgini.** Test Gezgini, birim testleri çalıştırmanıza ve sonuçları görüntülemenize izin verir. Test Gezgini, üçüncü taraf çerçeve dahil, Gezgin için bağdaştırıcısı olan herhangi bir test çerçevesini kullanabilir.  
  
2. **Microsoft birim testi çerçevesi için yönetilen kod.** Yönetilen kod için Microsoft birim testi çerçevesi Visual Studio ile yüklenir ve .NET kodunu test etmek için bir çerçeve sağlar.  
  
3. **C++ için Microsoft birim testi çerçevesi.** C++ için Microsoft birim testi çerçevesi Visual Studio ile yüklenir ve yerel kodu test etmek için bir çerçeve sağlar.  
  
4. **Kod kapsamı araçları.** Test Gezgini'nde bir tek komuttan birim testlerinizin çalıştıracağı ürün kodu miktarını belirleyebilirsiniz.  
  
5. **Microsoft Fakes yalıtım çerçevesi.** Microsoft Fakes yalıtım çerçevesi, test edilen kodda bağımlılıklar oluşturan üretim ve sistem kodunun yerine geçecek sınıflar ve yöntemler oluşturabilir. Bir işlev için sahte temsilciler uygulayarak, bağımlılık nesnesinin davranışını ve çıkışını denetlersiniz.  
  
   Ayrıca [Intellitest](../test/generate-unit-tests-for-your-code-with-intellitest.md) test verileri ve birim testleri paketi oluşturmak için .NET kodunuzu keşfedin. Koddaki her ifade için bir test girişi oluşturulur o ifadeyi yürütecek. Koddaki her koşullu şube için bir vaka analizi yapılır.  
  
## <a name="key-tasks"></a>Ana görevler  
 Birim testlerini anlamaya ve oluşturmaya yardımcı olmaları için aşağıdaki konuları kullanın:  
  
|Görevler|İlişkili Konular|  
|-----------|-----------------------|  
|**Hızlı başlangıçlar ve izlenecek yollar:** Birim kod örneklerini kullanarak Visual Studio'da testi gerçekleştirmeyi öğrenmek için aşağıdaki konulara bakın.|-   [İzlenecek yol: Oluşturma ve yönetilen kod için birim testleri çalıştırma](../test/walkthrough-creating-and-running-unit-tests-for-managed-code.md)<br />-   [Hızlı Başlangıç: Test Gezgini ile test güdümlü geliştirme](../test/quick-start-test-driven-development-with-test-explorer.md)<br />-   [Mevcut C++ uygulamalarına birim testleri ekleme](../test/unit-testing-existing-cpp-applications-with-test-explorer.md)<br />-   [Yerel kod Test Gezgini ile birim testi](http://msdn.microsoft.com/8a09d6d8-3613-49d8-9ffe-11375ac4736c)|  
|**Test Gezgini ile birim testi:** Test Gezgini'nin daha üretken ve verimli birim testleri oluşturma nasıl yardımcı olabileceğini öğrenin.|-   [Birim testi temel bilgileri](../test/unit-test-basics.md)<br />-   [Bir birim testi projesi oluşturma](../test/create-a-unit-test-project.md)<br />-   [Test Gezgini ile birim testleri çalıştırma](../test/run-unit-tests-with-test-explorer.md)<br />-   [Üçüncü taraf birim testi çerçevelerini yükleme](../test/install-third-party-unit-test-frameworks.md)<br />-   [Visual Studio 2010'dan birim testlerini yükseltme](http://msdn.microsoft.com/9bb75856-f68a-4de2-a084-b08a947a1172)|  
|**Birim testleri yönetilen kodu:**|-   [Yönetilen kod için Microsoft birim testi çerçevesi ile .NET Framework için birim testleri yazma](../test/writing-unit-tests-for-the-dotnet-framework-with-the-microsoft-unit-test-framework-for-managed-code.md)|  
|**Birim testleri C++ kodu**|-   [C++ için Microsoft birim testi çerçevesi ile C/C++ için birim testleri yazma](../test/writing-unit-tests-for-c-cpp-with-the-microsoft-unit-testing-framework-for-cpp.md)|  
|**Birim testlerini yalıtma**|-   [Microsoft Fakes ile Test edilen kodu yalıtma](../test/isolating-code-under-test-with-microsoft-fakes.md)|  
|**Birim testleriyle ne oranda proje kodunuzun edildiğini belirlemek için kod kapsamı kullanın:** Kod kapsamı özelliği hakkında bilgi edinin [!INCLUDE[vsprvsts](../includes/vsprvsts-md.md)] test araçları.|-   [Edildiğini belirlemek ne kadar kodun için kod kapsamını kullanma](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md)|  
|**Birim testleriniz için yük testlerini kullanarak stres ve performans analizleri gerçekleştirin:** Yük testi oluşturma ve performans yalıtmak ve stres sorularınızın gidermek için birim testleri ekleyin. **Not:**  Oluşturma ve yük testlerini kullanarak Visual Studio Enterprise'ı gerektirir.|-   [Yük testleri oluşturma ve düzenleme](http://msdn.microsoft.com/e2985d15-60a7-4177-93b4-f986c2936337)<br />-   [Nasıl Yapılır: Bir yük testi senaryosu için Web performans testleri ve birim testleri ekleme](http://msdn.microsoft.com/03cc073e-9bdf-4530-ae46-504a51884594)<br />-   [Nasıl Yapılır: Web testleri ve birim testleri yük testi senaryodan Kaldır](http://msdn.microsoft.com/3d6128d2-82b0-42fc-bda2-23a8aa03be07)|  
|**Ayarlama ve kalite kapıları:** Testleri kod kodun kalitesini sağlamaya yardımcı olmak için iade edilmeden önce çalışmaya zorlamak için kalite kapıları oluşturabilirsiniz.|-   [Ayarlama ve kalite kapıları](http://msdn.microsoft.com/library/bdc5666e-6cf0-45b2-a0a1-133c3f61e852)|  
|**Birim test türünü genişletin:** Testlerinize Birim Test çerçevesinde bulunmayan olmayabilir işlevler ekleyebilirsiniz. Örneğin, bir testin normal kullanıcı olarak çalışıp çalışmayacağını belirten bir test özelliği ekleyebilirsiniz. Veya çerçeveyi, bir yönteme satır öznitelikleri eklemek ve bu satırda bulunan verileri testin içinde kullanmak üzere genişletebilirsiniz.|Birim testi çerçevesinin nasıl genişletileceğine örnek kod için aşağıdakilere bakın [Microsoft Web sitesine](http://go.microsoft.com/fwlink/?LinkId=185591).|  
|**Test seçeneklerini belirleyin:** Örneğin, test sonuçlarının nerede depolanacağını belirtebilirsiniz.|[.runsettings dosyasını kullanarak birim testlerini yapılandırma](../test/configure-unit-tests-by-using-a-dot-runsettings-file.md)|  
  
## <a name="related-tasks"></a>İlişkili görevler  
 [Microsoft Test Yöneticisi'nde test sonuçlarını gözden geçirme](http://msdn.microsoft.com/9fb3e429-78df-4fe2-89ed-0ad1db0738f4)  
  
 Test sonuçları ve nasıl görüntülendiği, kaydedildiği ve silindiği de dahil bunlarla çalışma yollarını açıklar.  
  
 [Microsoft Visual Studio kullanarak sistem testleri çalıştırma](http://msdn.microsoft.com/library/19fae5c4-5798-4c4c-b531-3e8f901b1130)  
  
 Karşı Visual Studio'yu kullanma hakkındaki bilgilerin bağlantılarını sağlar [!INCLUDE[TCMext](../includes/tcmext-md.md)] otomatikleştirilmiş testler çalıştırılacak.  
  
## <a name="reference"></a>Başvuru  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting>  
 Öznitelikler, özel durumlar, bildirimler ve birim testini destekleyen diğer sınıfları sağlayan UnitTesting ad alanını açıklar.  
  
 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Web>  
 Destek sağlayan UnitTesting ad alanını genişleten ad alanını UnitTesting.Web ad alanını açıklar [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] ve Web hizmeti birim testleri.  
  
## <a name="external-resources"></a>Dış kaynaklar  
  
### <a name="videos"></a>Videolar  
 [Kanal 9: Birim testi XAML kullanılarak oluşturulan, Windows Store uygulamaları](http://go.microsoft.com/fwlink/?LinkId=226285)  
  
### <a name="forums"></a>Forumlar  
 [Visual Studio birim testi](http://go.microsoft.com/fwlink/?LinkId=224477)  
  
### <a name="guidance"></a>Kılavuz  
 [Visual Studio 2012 – bölüm 2 ile sürekli teslimat testi: Birim testi: İç testler](http://go.microsoft.com/fwlink/?LinkID=255188)  
  
### <a name="reference"></a>Başvuru  
 [Birim testleri için içerik dizini](http://go.microsoft.com/fwlink/?LinkID=254719)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kod kalitesini geliştirme](http://msdn.microsoft.com/library/73baa961-c21f-43fe-bb92-3f59ae9b5945)   
 [Uygulamayı test etme](http://msdn.microsoft.com/library/796b7d6d-ad45-4772-9719-55eaf5490dac)
