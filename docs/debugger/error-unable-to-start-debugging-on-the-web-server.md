---
title: 'Hata: Web sunucusunda hata ayıklama başlatılamıyor. | Microsoft Docs'
ms.date: 05/23/2017
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.http
- vwd.nonadmin.error.
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- IIS, debugging DLLs
- debugger, Web application errors
- unable to start debugging error
- security [debugger], Web applications
- debugging [Visual Studio], errors
- HTTP servers, debugging error
- security settings, checking for default Web sites
- errors [debugger], unable to start debugging
- debugging ASP.NET Web applications, unable to start debugging error
- remote debugging, errors
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 804249700ff813de5a45e44787af4f39d4a82ad2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53856689"
---
# <a name="error-unable-to-start-debugging-on-the-web-server"></a>Hata: Web sunucusunda hata ayıklama başlatılamıyor

Bir Web sunucusunda çalışan bir ASP.NET uygulamasında hata ayıklama kaydetmeye çalıştığında bu hata iletisini alabilirsiniz: `Unable to start debugging on the Web server`.

Genellikle, uygulama havuzları, IIS sıfırlama veya her ikisi de bir güncelleştirme gerektiren bir hata veya yapılandırma değişiklik oluştuğundan bu hata oluşur. Yükseltilmiş bir komut istemi'ni açıp yazarak IIS'yi sıfırlayın `iisreset`. 

## <a name="specificerrors"></a>Ayrıntılı hata iletisini nedir?

`Unable to start debugging on the Web server` İleti geneldir. Genellikle, daha belirli bir ileti hata dizesi içinde bulunur ve sorun veya arama için daha kesin düzeltme nedenini belirlemenize yardımcı olabilir. Birkaç ana hata iletisi eklenir daha yaygın hata iletileri şunlardır:

- [IIS başlatma eşleşen bir Web sitesi listesinde değil URL'si](#IISlist)
- [Web sunucusu doğru yapılandırılmamış](#web_server_config)
- [Web sunucusu için bağlantı kurulamıyor](#unabletoconnect)
- [Web sunucusu zamanında yanıt vermedi](#webservertimeout)
- [Microsoft visual studio uzaktan hata ayıklama monitor(msvsmon.exe) uzak bilgisayar üzerinde çalışıyor görünmüyor](#msvsmon)
- [Uzak sunucu bir hata döndürdü](#server_error)
- [ASP.NET hata ayıklama başlatılamadı](#aspnet)
- [Hata ayıklayıcı uzak bilgisayara bağlanamıyor](#cannot_connect)
- [Bkz: genel yapılandırma hataları için Yardım. Web sayfasını hata ayıklayıcının dışında çalıştırmak daha fazla bilgi sağlayabilir.](#see_help)

## <a name="IISlist"></a> IIS başlatma eşleşen bir Web sitesi listesinde değil URL'si

- Yönetici olarak Visual Studio'yu yeniden başlatın ve hata ayıklamayı yeniden deneyin. (Bazı ASP.NET hata ayıklama senaryoları yükseltilmiş ayrıcalıklar gerektirir.)

    Her zaman Visual Studio simgeyi sağ tıklayarak yönetici olarak çalıştırmak için Visual Studio yapılandırabileceğiniz seçme **özellikleri > Gelişmiş**ve her zaman bir yönetici olarak çalıştır seçme.

## <a name="web_server_config"></a> Web sunucusu doğru yapılandırılmamış

- Bkz: [hata: Web sunucusu doğru yapılandırılmamış](../debugger/error-the-web-server-is-not-configured-correctly.md).

## <a name="unabletoconnect"></a> Web sunucusu için bağlantı kurulamıyor

- Visual Studio ve Web sunucusu aynı makine üzerinde çalışan ve kullanarak hata ayıklama olduğunuz **F5** (yerine **iliştirme**)? Proje özelliklerini açın ve proje doğru Web sunucusuna bağlanıp başlatılacak URL için yapılandırıldığından emin olun. (Açık **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama** proje türüne bağlı olarak. Bir Web formları projesi için açık **özellik sayfaları > Başlat Seçenekleri > sunucu**.)

- Aksi takdirde, uygulama havuzu yeniden başlatın ve ardından IIS'yi sıfırlayın. Daha fazla bilgi için [IIS yapılandırmanızı denetleyin](#vxtbshttpservererrorsthingstocheck).

## <a name="webservertimeout"></a> Web sunucusu zamanında yanıt vermedi

- IIS'yi sıfırlayın ve hata ayıklamayı yeniden deneyin. Hata ayıklayıcı birden fazla IIS işleme bağlı olabilir; sıfırlama bunları sonlandırır. Daha fazla bilgi için [IIS yapılandırmanızı denetleyin](#vxtbshttpservererrorsthingstocheck).

## <a name="msvsmon"></a> Microsoft visual studio uzaktan hata ayıklama monitor(msvsmon.exe) uzak bilgisayar üzerinde çalışıyor görünmüyor

- Uzak makinede hata ayıklaması yapıyorsanız olduğundan emin olun [yüklenir ve uzaktan hata ayıklayıcıyı çalıştıran](../debugger/remote-debugging.md). İleti bir güvenlik duvarı bahsetmeleri, emin [güvenlik duvarı bağlantı noktaları düzeltmek](../debugger/remote-debugger-port-assignments.md) özellikle bir üçüncü taraf güvenlik duvarı kullanıyorsanız, açık olan.
- HOSTS dosyası kullanıyorsanız, doğru yapılandırıldığından emin olun. Örneğin kullanarak hata ayıklama, **F5** (yerine **iliştirme**), proje özelliklerinizden olduğu gibi aynı proje URL'si içermesi gerekir HOSTS dosyasını **özellikleri > Web > sunucuları**  veya **özellikleri > hata ayıklama**proje türüne bağlı olarak.

## <a name="server_error"></a> Uzak sunucu bir hata döndürdü

Denetleme, [IIS günlük dosyası](https://support.microsoft.com/help/943891/the-http-status-code-in-iis-7-0--iis-7-5--and-iis-8-0) hata kodlarını ve ek bilgiler ve bu IIS 7 için [blog gönderisi](https://blogs.iis.net/tomkmvp/troubleshoot-a-403).

Ayrıca, bazı yaygın hata kodlarını ve bazı öneriler şunlardır.
- (403) Yasak. Bu hata birçok olası nedenleri vardır, bu nedenle, günlük dosyası ve web sitesi için IIS güvenlik ayarlarını denetleyin. Sunucunun web.config içerdiğinden emin olun `debug=true` derleme öğesinde. Web uygulama klasörünüzdeki doğru izinlere sahip olduğunu ve uygulama havuzu yapılandırmanızı (parola değiştirmiş olabilir) doğru olduğundan emin olun. Bkz: [IIS yapılandırmanızı denetleyin](#vxtbshttpservererrorsthingstocheck). Bu ayarları zaten doğru olduğundan ve yerel olarak hata ayıklama, ayrıca doğru sunucu türü ve URL bağlandığınızı doğrulayın (içinde **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama**, proje türüne bağlı olarak).
- (503) sunucusu kullanılamıyor. Bir hata veya yapılandırma değişikliği nedeniyle uygulama havuzu durdurulmuş. Uygulama havuzu yeniden başlatın.
- (404) bulunamadı. Uygulama havuzu ASP.NET sürümü için doğru yapılandırıldığından emin olun.

## <a name="aspnet"></a> ASP.NET hata ayıklama başlatılamadı

- Uygulama havuzu yeniden başlatın ve IIS'yi sıfırlayın. Daha fazla bilgi için [IIS yapılandırmanızı denetleyin](#vxtbshttpservererrorsthingstocheck).
- URL yeniden yazma işlemleri yapıyorsanız, temel bir web.config hiçbir URL yeniden yazma işlemleri ile test edin. Bkz: **Not** hakkında URL yeniden yazma Modülü [IIS yapılandırmanızı denetleyin](#vxtbshttpservererrorsthingstocheck).

## <a name="cannot_connect"></a> Hata ayıklayıcı uzak bilgisayara bağlanamıyor

Yerel olarak hata ayıklaması yapıyorsanız, Visual Studio uzaktan hata ayıklayıcı 64-bit sürümü 64-bit uygulamalarında hata ayıklamak için kullandığı için 32 bitlik bir uygulama olduğundan, bu hata ortaya çıkabilir. Proje özelliklerini açın ve proje doğru Web sunucusu ve URL bağlanmak için yapılandırıldığından emin olun. (Açık **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama** proje türüne bağlı olarak.)

Ayrıca, HOSTS dosyası kullanıyorsanız, doğru yapılandırıldığından emin olun. Örneğin, ana proje özelliklerinizi olduğu gibi aynı proje URL'si içermesi gerekir dosya **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama**proje türüne bağlı olarak.

## <a name="see_help"></a> Bkz: genel yapılandırma hataları için Yardım. Web sayfasını hata ayıklayıcının dışında çalıştırmak daha fazla bilgi sağlayabilir.

- Visual Studio ve Web sunucusu aynı makinede kullanıyorsunuz? Proje özelliklerini açın ve proje doğru Web sunucusuna bağlanıp başlatılacak URL için yapılandırıldığından emin olun. (Açık **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama** proje türüne bağlı olarak.)

- İzleyeceğiniz adımlar, çalışmaz veya uzaktan hata ayıklama, [IIS yapılandırmanızı denetleyin](#vxtbshttpservererrorsthingstocheck).

##  <a name="vxtbshttpservererrorsthingstocheck"></a> IIS yapılandırmanızı denetleyin

Bu sorunu çözmek için burada ayrıntıları verilen adımlar aldıktan sonra ve hata ayıklamak yeniden denemeden önce IIS'yi sıfırlayın gerekebilir. Yükseltilmiş bir komut istemi'ni açıp yazarak bunu yapabilirsiniz `iisreset`. 

* Durdur ve, IIS uygulama havuzları yeniden başlatın ve sonra yeniden deneyin. 

    Bir hata nedeniyle uygulama havuzu durdurulmuş. Veya, yaptığınız başka bir yapılandırma değişikliği durdurun ve, uygulama havuzunu yeniden başlatmak gerekebilir.
    
    > [!NOTE]
    > Uygulama havuzu durduruluyor tutar, Denetim Masası'ndan URL yeniden yazma modülü kaldırmanız gerekebilir. Web Platformu Yükleyicisi (Webpı) kullanarak yeniden yükleyebilirsiniz. Önemli sistem yükseltme sonrasında bu sorun oluşabilir.

* Uygulama havuzu yapılandırmanızı denetleyin, gerekiyorsa düzeltin ve sonra yeniden deneyin.

    Uygulama havuzu bir Visual Studio projenize eşleşmeyen ASP.NET sürümü için yapılandırılabilir. Verze technologie ASP.NET uygulama havuzundaki güncelleştirin ve yeniden başlatın. Ayrıntılı bilgi için bkz. [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45).

    Ayrıca, parola kimlik bilgileri değiştiyse, uygulama havuzunu veya Web sitesi güncelleştirmeniz gerekebilir.  Uygulama havuzu kimlik bilgilerini güncelleştirme **Gelişmiş Ayarlar > işlem modeli > kimlik**. Web sitesi için kimlik bilgilerini güncelleştirme **temel ayarları > Farklı Bağlan...** . Uygulama havuzu yeniden başlatın.
    
* Web uygulama klasörünüzdeki doğru izinlere sahip olduğunu denetleyin.

    IIS_IUSRS, IUSR, size veya belirli bir kullanıcı ile ilişkili olduğundan emin olun [uygulama havuzu](/iis/manage/configuring-security/application-pool-identities) okuma ve yürütme hakları Web uygulaması klasörü için. Sorunu düzeltip, uygulama havuzu yeniden başlatın.

* IIS üzerinde ASP.NET doğru sürümünün yüklü olduğundan emin olun.

    ASP.NET IIS ve Visual Studio projenize eşleşmeyen sürümleri, bu soruna neden olabilir. Framework sürümü web.config dosyasında ayarlamanız gerekebilir. IIS üzerinde ASP.NET yüklemek için kullanın [Web Platformu Yükleyicisi (Webpı)](https://www.microsoft.com/web/downloads/platform.aspx). Ayrıca bkz [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45) veya ASP.NET Core [IIS ile Windows Konağında](https://docs.asp.net/en/latest/publishing/iis.html).
  
* Yalnızca IP adresi kullanıyorsanız, kimlik doğrulama hatalarını çözümleme

     Varsayılan olarak, IP adreslerinin İnternet'e bir parçası olarak kabul edilir ve NTLM kimlik doğrulaması Internet üzerinden yapılmaz. Web sitenizi IIS kimlik doğrulaması gerektirecek şekilde yapılandırıldıysa, bu kimlik doğrulaması başarısız olur. Bu sorunu düzeltmek için IP adresi yerine uzak bilgisayarın adını belirtebilirsiniz.
     
## <a name="other-causes"></a>Yol açabilecek diğer nedenler

IIS yapılandırma sorunu neden, aşağıdaki adımları deneyin:

- Yönetici ayrıcalıklarıyla Visual Studio'yu yeniden başlatın ve yeniden deneyin.

    Web dağıtımı kullanarak gibi bazı ASP.NET hata ayıklama senaryoları Visual Studio için yükseltilmiş ayrıcalıklar gerektirir.
    
- Visual Studio birden çok örneğini kullanıyorsanız, projenize (yönetici ayrıcalıklarıyla) Visual Studio'nun bir örneğinde yeniden açın ve yeniden deneyin.

- İle yerel adresler HOSTS dosyası kullanıyorsanız, makinenin IP adresi yerine geri döngü adresi kullanarak deneyin.

    Yerel adresler kullanmıyorsanız, HOSTS dosyası, proje özellikleri olduğu gibi aynı proje URL'si içerdiğinden emin olun **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama**bağlı olarak, Proje türü.

## <a name="more-troubleshooting-steps"></a>Daha fazla sorun giderme adımları

* Sunucu üzerindeki tarayıcıda localhost sayfa yukarı taşıyın.

     IIS doğru yüklü değilse, yazarken hatalar almalısınız `http://localhost` bir tarayıcıda.
     
     IIS'ye dağıtma ile ilgili daha fazla bilgi için bkz: [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45) ve ASP.NET Core [IIS ile Windows Konağında](https://docs.asp.net/en/latest/publishing/iis.html).

* Sunucuda temel bir ASP.NET uygulaması oluşturun (veya bir temel web.config dosyasını kullanın).

    Hata ayıklayıcısı ile çalışmak için uygulamanızı alınamıyor, temel bir ASP.NET uygulaması sunucu üzerinde yerel olarak oluşturmayı deneyin ve temel uygulama hatalarını ayıklamayı deneyin. (Varsayılan ASP.NET MVC şablonu kullanmak isteyebilirsiniz.) Temel bir uygulama hatalarını ayıklayabilir, bu iki yapılandırma arasında farklıdır belirlemenize yardımcı olabilir. URL yeniden yazma kuralları gibi ayarları farklılıkları web.config dosyasında arayın.

## <a name="see-also"></a>Ayrıca Bkz.  
 [Web uygulamalarında hata ayıklama: Hatalar ve sorun giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)