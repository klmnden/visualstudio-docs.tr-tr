---
title: Dağıtılmış yük testi için bir Test ayarı oluşturun
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- test settings, for distributed load tests
ms.assetid: b63d4b71-3b74-4872-b2d1-f0bd1a9a8544
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0f947d8a4994c8a515a707f34a07065358194e09
ms.sourcegitcommit: 5b34052a1c7d86179d7898ed532babb2d9dad4a3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2019
ms.locfileid: "69490682"
---
# <a name="how-to-create-a-test-settings-file-for-a-distributed-load-test"></a>Nasıl yapılır: Dağıtılmış yük testi için test ayarları dosyası oluşturma

Yapılandırma *test ayarları* bu testleri test aracıları kullanarak birden çok makine arasında dağıtmak ve test denetleyicilerine yük testleri için. Kullanılacak test ayarlarını da yapılandırabilirsiniz *tanılama veri bağdaştırıcıları*, toplamak istediğiniz veri türlerini belirtmek veya Visual Studio'dan yük testlerinizi çalıştırdığınızda test makinelerini nasıl etkileyeceğinizi.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

Örneğin, kodun performans dökümünü toplamak için ASP.NET Profiler tanılama veri bağdaştırıcısı kullanabilirsiniz. Buna ek olarak, tanılama veri bağdaştırıcıları test makinaları üzerinde olası sorunların benzetimini yapmak veya kullanılabilir sistem belleğini azaltmak için kullanılabilir.

Visual Studio için test ayarları bir dosyada depolanır. Test ayarları, her rolle ilgili aşağıdaki bilgileri tanımlayın:

- Test altındaki uygulamanız için gerekli olan roller kümesi

- Testlerinizi çalıştırmak için kullanılacak rolü

- Her rol için tanılama veri bağdaştırıcıları

Testlerinizi çalıştırdığınızda, test çalışması için gerekli bağlı olarak etkin test ayarlarını kullanmak için test ayarlarını seçin. Test ayarları dosyası çözümünüzün bir parçası olarak depolanır. Dosya adı uzantısına sahip *.testsettings*.

Bir çözüme web performansı ve yük testi eklediğinizde bir *varsayılan Local.testsettings* dosyası oluşturulur. Dosya altında çözüme otomatik olarak eklenir **çözüm öğeleri** klasör. Bu dosya, testlerinizi tanılama veri bağdaştırıcısı olmadan yerel olarak çalışır. Başka bir ekleyebilirsiniz *.testsettings* düzenlemek veya dosya bir *.testsettings* ve test denetleyicilerini tanılama veri bağdaştırıcıları belirtmek için dosya.

Test denetleyicisi test ayarlarınızda her rol için kullanılabilen aracılara sahip olacaktır. Test denetleyicileri ve test aracıları hakkında daha fazla bilgi için bkz. [test denetleyicileri ve test aracıları Visual Studio ile yönetme](../test/manage-test-controllers-and-test-agents.md).

Oluşturun ve Visual Studio'dan çalıştırmayı planladığınız yük testleri için çözümünüzdeki test ayarlarını kaldırmak için aşağıdaki adımları izleyin.

## <a name="create-a-test-settings-file"></a>Test ayarları dosyası oluşturma

1. İçinde **Çözüm Gezgini**, sağ **çözüm öğeleri**, işaret **Ekle**ve ardından **yeni öğe**.

     **Yeni Öğe Ekle** iletişim kutusu görüntülenir.

2. İçinde **yüklü şablonlar** bölmesinde seçin **Test ayarları**.

3. (İsteğe bağlı) İçinde **adı** kutusunda, test ayarları dosyasının adıyla değiştirin.

4. Seçin **ekleme**.

     Yeni test ayarları dosyası görünür **Çözüm Gezgini**altında **çözüm öğeleri** klasör.

5. **Test ayarları** iletişim kutusu görüntülenir. **Genel** sayfası seçili.

     Şimdi, düzenleme ve test ayarları değerlerini kaydedin.

6. Altında **adı**, test ayarları adını yazın.

7. (İsteğe bağlı) Altında **açıklama**, diğer takım üyelerinin ne işe yaradıklarını bilmesi için test ayarında bir açıklama yazın.

8. (İsteğe bağlı) Test çalışmalarınız için varsayılan adlandırma şemasını seçmek için **varsayılan adlandırma düzeni**. Kendi adlandırma düzeninizi tanımlamak için seçin **kullanıcı tanımlı Düzen** ve sonra istediğiniz metni yazın **önek metni**. Test çalışması ismine tarih ve saat damgasını eklemek için seçin **ekleme tarih ve saat damgası**.

9. Seçin **rolleri**.

     **Rolleri** sayfası görüntülenir.

     ![Test ayarı rolü](../test/media/load_testtestrole.png)

10. Testlerinizi uzaktan çalıştırmak veya testlerinizi uzaktan çalıştırmak ve uzaktan veri toplamak için kullanın **Test yürütme yöntemi** açılır ve select **uzaktan yürütme**.

11. Kullanım **denetleyicisi** test aracıları için bir test denetleyicisi seçmek için açılan **denetleyicisi** testlerinizi çalıştırmak veya veri toplamak için kullanılır.

    > [!NOTE]
    > Bu ilk kez denetleyici eklediğiniz ise, hiçbir denetleyicileri aşağı açılan listede listelenir. Liste diğer test ayarlarında belirttiğiniz önceki denetleyiciler tarafından doldurulur. Kutuya denetleyicinin adını yazmanız gerekir (örneğin, **TestControllerMachine1**).

12. Altında testleri çalıştırmak ve verileri toplamak için kullanmak istediğiniz rolleri eklemek için **rolleri**, seçin **Ekle**.

13. Rol için bir ad yazın **adı** sütun. Örneğin, rol "Web sunucusu" olabilir.

14. Adım 12 ve 13 ihtiyaç duyduğunuz tüm rolleri eklemek için yineleyin.

     Her rol test denetleyicisi tarafından yönetilen bir test aracısı kullanır.

15. Testlerinizi çalıştırmak ve ardından istediğiniz rolü seçin **testleri çalıştırmak için rol olarak ayarla**.

    > [!IMPORTANT]
    > Oluşturduğunuz ve tanımladığınız diğer roller testleri çalıştırmaz ancak yalnızca veri ve roller için belirttiğiniz tanıya göre veri toplamak için kullanılacak **veri ve tanı** sayfası.

16. Bir rol için kullanılabilecek aracıları sınırlamak için rolü seçin ve ardından **Ekle** araç çubuğunda altında **seçili rol için aracı öznitelikleri**.

     **Aracı seçim kuralı** iletişim kutusu görüntülenir.

     Adı yazın **öznitelik adı** ve değer **öznitelik değeri**ve ardından **Tamam**. Gereksinim duyduğunuz kadar çok sayıda öznitelik ekleyin.

     Örneğin, "RAM > 16"True"veya"False"fazla 16 GB belleğe sahip test aracısı makinelerinde filtrelemek için bir değere sahip GB" adlı özniteliği ekleyebilirsiniz. Aynı özniteliği bir veya daha fazla test aracısına uygulamak için kullandığınız **Test denetleyicisini Yönet** iletişim kutusu. Daha fazla bilgi için [test denetleyicileri ve test aracıları Visual Studio ile yönetme](../test/manage-test-controllers-and-test-agents.md).

17. Seçin **veri ve tanılama**.

     **Veri ve tanılama** sayfası görüntülenir.

     ![Test ayarı veri ve tanılama](../test/media/load_testtest.png)

18. İçinde **veri ve tanı** sayfasında seçerek rol yaptıklarını tanımlamak *tanılama veri bağdaştırıcıları* rolün veri toplamak için kullanacağını. Bu nedenle, bir veya daha fazla veri ve tanılama bağdaştırıcıları rolü için etkinse, test denetleyicisi belirtilen veri ve tanılama bağdaştırıcısı rol için tanımladığınız öznitelikleri temel alan verileri toplamak için bir uygun test aracısı makinesini seçecektir. Veri ve her rol için toplamak istediğiniz tanılama veri bağdaştırıcılarını seçmek için rolü seçin. Her rol için testin ihtiyaçlarına göre tanılama veri bağdaştırıcıları seçin. Her rol için seçtiğiniz her tanılama veri bağdaştırıcısını yapılandırmak için **yapılandırma**.

     **Roller ve tanılama veri bağdaştırıcıları örneği:**

     Örneğin, bir "" True"ve"RAM > 16 GB"olarak ayarlanan öznitelikle" SQL Server"adlı bir sunucu rolü olarak SQL kullanır" özniteliğine sahip "Masaüstü İstemcisi" adlı bir istemci rolü oluşturabilirsiniz. Seçim yaparak "Masaüstü İstemcisi" nin testleri çalıştıracağını belirtirseniz **testleri çalıştırmak için rol olarak ayarla** içinde **rolleri** sayfasında, test denetleyicisi özniteliğini içeren test aracıları bulunan makineleri seçer "" True", testleri çalıştırmak"SQL kullanır. Test denetleyicisi "RAM > 16 yalnızca veri ve rolüne dahil edilen tanılama bağdaştırıcıları tarafından tanımlanan veriyi toplamak için GB" özniteliğini içeren test aracıları olan SQL sunucu makinelerini de seçecektir. "Masaüstü İstemcisi" test aracısı, veri ve tanılama bağdaştırıcıları bu rol için çok seçerseniz, çalıştığı makinelerin veri toplayabilirsiniz.

     Her tanılama veri bağdaştırıcısı ve nasıl yapılandırılacağı hakkında daha fazla ayrıntı için aşağıdaki tabloda ilişkilendirilen konuyu görüntüleyebilirsiniz.

     Tanılama veri bağdaştırıcıları hakkında daha fazla bilgi için bkz. [test ayarlarını kullanarak tanılama bilgi toplayan](../test/collect-diagnostic-information-using-test-settings.md).

     **Yük testleri için tanılama veri bağdaştırıcıları**

    |Tanılama veri bağdaştırıcısı|Yük testlerinde kullanma|İlişkili konu|
    |-|-------------------------|-|
    |**IntelliTrace ve test etkisi için ASP.NET Istemci proxy 'Si:** Bu proxy, IntelliTrace ve test etkisi tanılama veri bağdaştırıcıları için bir istemciden bir Web sunucusuna http çağrıları hakkında bilgi toplamanıza olanak tanır.|![Bilgi simgesi](../test/media/vc364f4.gif)<br /><br /> Test aracısı makinelerden sistem bilgilerini toplamak için özel bir ihtiyacınız yoksa, bu bağdaştırıcıyı dahil etmeyin. **Dikkatli**  Toplanan büyük miktarda veri nedeniyle oluşan sorunlardan dolayı yük testlerinde IntelliTrace bağdaştırıcısının kullanımını önermiyoruz. <br /><br /> Test etkisi verisi, yük testleri kullanılarak toplanmaz.||
    |**IntelliTrace** Bir günlük dosyasında depolanan belirli tanılama izleme bilgilerini yapılandırabilirsiniz. Bir günlük dosyası uzantısına sahip *.tdlog*. Test ve bir test adımı başarısız çalıştırdığınızda, bir hata oluşturabilirsiniz. Tanılama izlemesini içeren günlük dosyası otomatik olarak bu hataya eklenir. Günlük dosyasında toplanan veri, kodda bir hata yeniden oluşturmak için gerekli olan zamanı azaltarak hata ayıklama verimliliğini artırır. Bu günlük dosyasından dosya yerel oturumun başka bir bilgisayarda yeniden oluşturulabilir. Bu hatanın tekrar oluşturulamama riskini azaltır.<br /><br /> Daha fazla bilgi için [toplamak IntelliTrace verilerini](../test/how-to-collect-intellitrace-data-to-help-debug-difficult-issues.md).|![Önemli simgesi](../test/media/vc364f3.gif)<br /><br /> Yük testlerinde IntelliTrace bağdaştırıcısının kullanımını büyük toplanan ve günlüğe kaydedilen veri miktarı nedeniyle oluşan sorunlar nedeniyle önermiyoruz. Çok sayıda test aracısı kullanmayan ve uzun çalıştırmayan yük testlerinde IntelliTrace bağdaştırıcısının kullanılacağını denemelidir.|[Nasıl yapılır: Hata ayıklama zor sorunlarını gidermek için IntelliTrace verilerini toplayın](../test/how-to-collect-intellitrace-data-to-help-debug-difficult-issues.md)|
    |**ASP.NET Profil Oluşturucu:** ASP.NET Web uygulamalarında performans verilerini toplayan ASP.NET profil oluşturmayı içeren bir test ayarı oluşturabilirsiniz.|Bir geliştirme web sunucusuna karşı çalışmaması ASP.NET profiler tanılama veri bağdaştırıcısı Internet Information Services (IIS) işleminin profilini. Yük testinizde Web sitesinin profilini çıkarmak için IIS'in çalıştığı makineye bir test aracısı yüklemek zorunda. Test aracısı yük oluşturmayacak ancak yalnızca koleksiyon aracı olacak. Daha fazla bilgi için [yüklemek ve test denetleyicisilerinin](../test/lab-management/install-configure-test-agents.md).|[Nasıl yapılır: Test ayarlarını kullanarak yük testleri için ASP.NET Profiler 'ı yapılandırma](../test/how-to-configure-aspnet-profiler-for-load-tests-using-test-settings.md)|
    |**Olay günlüğü:** Test sonuçlarına dahil edilecek olay günlüğü toplamayı dahil etmek için bir test ayarı yapılandırabilirsiniz.||[Nasıl yapılır: Test ayarlarını kullanarak olay günlüğü koleksiyonunu yapılandırma](https://msdn.microsoft.com/48d67891-6018-4549-83e3-213d5d824a02)|
    |**Ağ öykünmesi:** Test ayarı kullanarak testinize yapay bir ağ yükü koymak istediğinizi belirtebilirsiniz. Ağ öykünmesi öykünmesi, çevirmeli gibi belirli ağ bağlantı hızı tarafından makine gelen ve giden iletişimi etkiler. **Not:**  Ağ öykünmesi, ağ bağlantısı hızını artırmak için kullanılamaz.|Ağ öykünmesi bağdaştırıcısı yük testleri tarafından yok sayılır. Bunun yerine, yük testleri yük testi senaryosunun ağ karışımında belirtilen ayarları kullanın.<br /><br /> Daha fazla bilgi için [sanal ağ türlerini belirtme](../test/specify-virtual-network-types-in-a-load-test-scenario.md).||
    |**Sistem bilgileri:** Sistem bilgileri tanısı ve veri toplayıcısının çalıştırıldığı makineler hakkındaki sistem bilgilerini içerecek şekilde bir test ayarı ayarlanabilir. Sistem bilgileri, bir test ayarı kullanarak test sonuçlarında belirtilir.|![Bilgi simgesi](../test/media/vc364f4.gif)<br /><br /> Sistem bilgilerini hem yük aracılarından hem de test uygulanan sistemden toplayabilirsiniz.|Yapılandırma, bu bilgileri toplamak için gereklidir.|
    |**Test etkisi:** Bir test çalışması çalıştırıldığında, uygulama kodunuzun hangi yöntemlerinin kullanıldığı hakkında bilgi toplayabilirsiniz. Bu, uygulama koduna değişiklikleri ile hangi testlerin etkilendiğini belirlemek için geliştiriciler tarafından yapılan değişiklikler ile birlikte kullanılabilir.|Test etkisi verisi, yük testleri ile toplanmaz.||
    |**Video kaydedicisi:** Otomatikleştirilmiş bir test çalıştırdığınızda masaüstü oturumunuzun bir video kaydını oluşturabilirsiniz. Bu, bir kodlanmış UI testi için kullanıcı eylemlerini görüntülemek için yararlı olabilir. Videoyu diğer takım üyelerinin yeniden oluşturulması zor olan uygulama sorunlarını yalıtmalarına yardımcı olabilir. **Not:**  Testleri uzaktan çalıştırırken, aracı etkileşimli işlem modunda çalışmadığı sürece video kaydedicisi çalışmaz.|![Önemli simge](../test/media/vc364f3.gif) **uyarısı:**  Yük testleri için video kaydedici bağdaştırıcısının kullanımını önermiyoruz.|[Nasıl yapılır: Test ayarlarını kullanarak testler sırasında ekran ve ses kayıtlarını ekleyin](../test/how-to-include-recordings-of-the-screen-and-voice-during-tests.md)|

19. Seçin **dağıtım**.

     **Dağıtım** sayfası görüntülenir.

20. Testlerinizi çalıştırdığınız her seferde dağıtım için ayrı bir dizin oluşturmak için Seç **etkinleştirme dağıtım**.

    > [!NOTE]
    > Bunu yaparsanız, testlerinizi çalıştırdığınızda uygulamanızı yapılandırmaya devam edebilirsiniz.

21. Testlerinizi çalıştırmak için kullandığınız dizine bir dosya eklemek için **Dosya Ekle**ve sonra eklemek istediğiniz dosyayı seçin.

    > [!NOTE]
    > Bir yük testi çalıştırdığınızda, Eklenti derlemeleri, veri dosyaları ve yüklenen dosyalar otomatik olarak dağıtılır.

22. Testlerinizi çalıştırmak için kullandığınız dizine bir dizin eklemek için **Dizin Ekle** ve ardından eklemek istediğiniz dizini seçin.

23. Betikleri önce ve sonra testlerinizi çalıştırmak için tercih **Kurulum ve temizleme betikleri**.

     **Kurulum ve temizleme betikleri** sayfası görüntülenir.

    1. İçindeki betik dosyasının konumunu yazın **Kurulum betiği** veya üç noktayı seçin ( **...** ) Kurulum betiğini bulmak için.

    2. İçindeki betik dosyasının konumunu yazın **temizleme betiği** veya üç noktayı seçin ( **...** ) temizleme betiğini bulmak için.

24. Testlerinizi farklı bir ana bilgisayar kullanarak çalıştırmak için tercih **konakları**.

    1. İçinde **konak türü**, doğrulayın **varsayılan** seçilir.

        > [!NOTE]
        > **ASP.NET** içinde **konak türü** yük testlerinde desteklenmez.

    2. Kullanım **32 bit veya 64 bit test çalıştırması** işlem 32 bit veya 64-bit işlem çalıştırmak için yük testinizde web başarım ve birim testleri isteyip istemediğinizi seçin için açılır.

        > [!NOTE]
        > Maksimum esneklik için size web performansınızı derlemek ve kullanarak yük **herhangi bir CPU** yapılandırma. Daha sonra hem 32-bit hem de 64 bit aracıların çalıştırabilirsiniz. Derleme web performansı ve yük testi projelerini kullanarak **64-bit** yapılandırma herhangi bir avantaj.

25. (İsteğe bağlı) Her test çalışması ve bireysel testler için süreyi sınırlamak üzere seçin **Test zaman aşımları.**

    1. Bir zaman sınırı aşıldığında bir test durdurmayı seçin **toplam süre aşıldıysa test iptal** ve bu sınır için bir değer yazın.

    2. Bir zaman sınırı aşıldığında belirli bir testi başarısız kılmak için seçin **tek bir testin yürütme zamanı aşılırsa, testi başarısız olarak işaretle**ve bu sınır için bir değer girin.

26. Skip **birim testi**. Yük testleri bu ayarları kullanmayın.

27. Skip **Web Test**. Yük testleri bu ayarları kullanmayın.

28. Test ayarlarını kaydetmek için seçin **Kaydet**. İstediğiniz dosya adını yazın **nesne adı**.

## <a name="remove-a-test-settings-file-from-your-solution"></a>Çözümünüzde bir test ayarları dosyasını kaldırma

Altında **çözüm öğeleri** klasöründe **Çözüm Gezgini**, kaldırın ve ardından istediğiniz test ayarlarını sağ **Kaldır**.

Test ayarları dosyası çözümünüzden kaldırılır.

## <a name="see-also"></a>Ayrıca bkz.

- [Test denetleyicileri ve test aracıları](configure-test-agents-and-controllers-for-load-tests.md)
- [Test ayarlarını kullanarak tanılama bilgileri Topla](../test/collect-diagnostic-information-using-test-settings.md)