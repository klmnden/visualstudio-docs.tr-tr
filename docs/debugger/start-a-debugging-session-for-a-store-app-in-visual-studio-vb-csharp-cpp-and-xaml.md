---
title: Visual Studio'da bir UWP uygulaması için hata ayıklama oturumu başlatma | Microsoft Docs
ms.custom: ''
ms.date: 01/04/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- VC.Project.IVCAppHostRemoteDebugPageObject.MachineName
- VC.Project.IVCAppHostRemoteDebugPageObject.BreakpointBehavior
- VC.Project.IVCAppHostLocalDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCAppHostTetheredDebugPageObject.DebuggerType
- VC.Project.IVCAppHostLocalDebugPageObject.BreakpointBehavior
- VC.Project.IVCAppHostRemoteDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostRemoteDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCAppHostLocalDebugPageObject.DebuggerType
- VC.Project.IVCAppHostSimulatorDebugPageObject.DebuggerType
- ImmersiveProjects.Properties.Debug
- VC.Project.IVCAppHostTetheredDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostSimulatorDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostSimulatorDebugPageObject.GPUDebuggerTargetType
- VC.Project.IVCAppHostLocalDebugPageObject.LaunchApplication
- VC.Project.IVCAppHostLocalDebugPageObject.AllowLocalNetworkLoopback
- AppPackage.Properties.Debug
- VC.Project.IVCAppHostRemoteDebugPageObject.Authentication
- VC.Project.IVCAppHostRemoteDebugPageObject.DebuggerType
- VC.Project.IVCAppHostSimulatorDebugPageObject.BreakpointBehavior
- vs.debug.installedapppackagelauncher
- vs.debug.error.wwahost_scriptdebuggingdisabled
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- uwp
ms.openlocfilehash: a7a9f74450ccf2cb493e44fa1fecef0630a27569
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49818790"
---
# <a name="start-a-debugging-session-for-a-uwp-app-in-visual-studio"></a>Visual Studio'da bir UWP uygulaması için hata ayıklama oturumu başlatma
  
 Bu konu, XAML ve Visual C++, Visual yazılmış UWP uygulamaları için hata ayıklama oturumu başlatmak açıklar C#, veya Visual Basic ve HTML ve JavaScript yazılmış UWP uygulamaları için. Uygulama hata ayıklama, hem hata ayıklama oturumu yapılandırma ve uygulamayı başlatmak için yol seçme içerir.  
  
##  <a name="BKMK_The_easy_way_to_start_debugging"></a> Hata ayıklama başlamanın en kolay yolu  
  
1. Uygulama çözümünü Visual Studio'da açın.  
  
2. F5'i seçin.  
  
   Visual Studio, yapıları ve hata ayıklayıcısı ekli uygulamayı başlatır. Yürütme bir kesme noktasına ulaşıldığında, işlenmeyen bir özel durum oluşur, el ile yürütme askıya veya uygulama sona kadar devam eder.  
  
##  <a name="BKMK_Choose_the_build_configuration_options"></a> Yapı yapılandırma seçenekleri'ni seçin.  
  
1.   Açılan listeden listesinde yanındaki **hata ayıklamayı Başlat** hata ayıklayıcı düğmesine **standart** araç seçin **hata ayıklama**.  
  
2.  Gelen **Platform** liste oluşturmak için hedef platformu seçin.  
  
##  <a name="BKMK_Choose_the_deployment_target"></a> Dağıtım hedefi seçin  
  
Dağıtın ve Visual Studio makinesine bağlı cihaza, yerel makine, bir uzak cihaz veya öykünücü üzerinde Visual Studio simulator bir UWP uygulamasında hata ayıklama. Dağıtım hedefi sağındaki aşağı açılan listeden seçin **Platform** hedef hata ayıklayıcı **standart** araç çubuğu.
  
![Dağıtım hedefi seçin](../debugger/media/vsrun_select_target_device.png)  
  
Bu seçeneklerden birini seçin:  
  
|||  
|-|-|  
|**Yerel Makine**|Uygulama geçerli oturumdaki yerel makinenizde hata ayıklayın.|  
|**Simülatör**|UWP uygulamaları için Visual Studio simulator uygulamasında hata ayıklayın. Simülatör hata ayıklama cihazın işlevselliğini sağlayan masaüstü penceredir — dokunma hareketlerini ve cihaz döndürme gibi —, yerel makinede kullanılabilir olmayabilir. Bu seçenek yalnızca kullanılabilir değilse, uygulamanızın **hedef Platform Min. Sürüm** geliştirme yaptığınız makinedeki işletim sistemi küçük veya ona eşit. Bkz: [simulator'da çalıştırmak UWP uygulamaları](../debugger/run-windows-store-apps-in-the-simulator.md).|  
|**Uzak makine**|İntranet üzerindeki yerel makineye bağlı veya bir Ethernet kablosuyla doğrudan bağlı bir cihazda uygulama hatalarını ayıklayın. Uzaktan hata ayıklamak için Visual Studio için Uzak Araçlar yüklü ve uzak cihazda çalışıyor olması gerekir. Bkz: [uzak bir makinede çalıştırmak UWP uygulamaları](../debugger/run-windows-store-apps-on-a-remote-machine.md).|  
|**cihaz**|USB bağlantılı bir cihazda uygulama hatalarını ayıklayın. Cihazın kilidi Geliştirici ve kilidi ekranında olması gerekir.|  
|**Mobile öykünücüsü**|Öykünücü adında belirtilen yapılandırma ile bir öykünücü önyükleme, uygulamayı dağıtma ve hata ayıklamaya başlayın. Öykünücüler, yalnızca Hyper-V etkin makineler üzerinde kullanılabilir.|  

##  <a name="BKMK_Open_the_debugging_property_page_for_the_project"></a> Ek hata ayıklama seçeneklerini seçin  

Hata ayıklama Ek Seçenekler yapılandırmanız gerekiyorsa, projenin özellik sayfasını açın.
  
1.  Çözüm Gezgini'nde projeyi seçin. Kısayol menüsünde **özellikleri**.  
  
2.  Bu proje için hata ayıklama özellik sayfasını açmak için şunları yapın:  
  
    -   Visual C# ve Visual Basic uygulamaları seçin **hata ayıklama**.  
  
         ![C&#35; &#47; VB proje hata ayıklama özellik sayfası](../debugger/media/dbg_csvb_debugpropertypage.png)  
  
    -   Visual C++ ve JavaScript uygulamaları için genişletin **yapılandırma özellikleri** düğümünü seçip **hata ayıklama**.  
  
         ![C&#43; &#43; UWP uygulamasında hata ayıklama özellik sayfası](../debugger/media/dbg_cpp_debugpropertypage.png)  

###  <a name="BKMK_Choose_the_debugger_to_use"></a> Kullanılacak hata ayıklayıcı seçin  
Varsayılan olarak, Visual Studio, C# ve Visual Basic uygulamaları yönetilen kodda hata ayıklamasına. C# ve Visual Basic uygulama hem yönetilen ve yerel C/C++ kodu uygulamanızda hata ayıklamak seçebilirsiniz. C++ uygulamalarında Visual Studio, varsayılan olarak yerel kod hata ayıklamasına. JavaScript uygulamalar, Visual Studio, varsayılan olarak betik hata ayıklamasına. 
  
C++ uygulamaları ve JavaScript için hata ayıklama bileşenleri uygulamanızın yerine veya ek olarak, yerel kod içinde olan belirli kod türlerini seçebilirsiniz. Hata ayıklamak için kod belirttiğiniz **hata ayıklayıcı türü** listesini **hata ayıklama** uygulama projesinin özellik sayfası.  
  
Bu hata ayıklayıcıları birini **uygulama işlemi** listesi:  
  
|||  
|-|-|  
|**Yalnızca yönetilen**|Uygulamanızı yönetilen kodda hata ayıklama. JavaScript kodu ve yerel C/C++ kod göz ardı edilir.|  
|**Yalnızca yerel**|Uygulamanızı yerel C/C++ kodunda hata ayıklayın. Yönetilen kod ve JavaScript kodunu göz ardı edilir.|  
|**(Yönetilen ve yerel) karışık**|Yerel C/C++ kod ve uygulamanızı yönetilen kodda hata ayıklama. JavaScript kodu göz ardı edilir. C++ projelerinde, bu seçenek olarak adlandırılan **(yönetilen ve yerel)**.|  
|**Jenom skript**|Uygulamanızı JavaScript kodunda hata ayıklayın. Yönetilen kod ve yerel koda göz ardı edilir.|  
|**Betik ve yerel**|Yerel C/C++ kod ve uygulamanızı JavaScript kodunda hata ayıklayın. Yönetilen kod yok sayılır. Yalnızca C++ projelerinde kullanılabilir.|  
|**Yalnızca GPU (C++ AMP)**|Grafik işlem birimi (GPU) üzerinde çalışan yerel C++ kod hatalarını ayıklama. Yalnızca C++ projelerinde kullanılabilir.|  

İçinde C# ve Visual Basic uygulamaları da ayarlayabilirsiniz aynı **hata ayıklayıcı türü** projenin bir parçası olan herhangi bir arka plan görevleri için değerler.
  
###  <a name="BKMK__Optional__Delay_starting_the_debug_session"></a> (İsteğe bağlı) Hata ayıklama oturumu başlatma gecikmesi  
 Hata ayıklamaya başladığınızda varsayılan olarak, Visual Studio uygulama hemen başlar. Hata ayıklama oturumunu başlatmada ancak uygulamanızın başlangıç gecikme. Bu seçeneği belirlediğinizde, uygulama başlangıç ekranından veya etkinleştirme sözleşme başlatıldığında veya başka bir işlem veya metodu tarafından başlatıldığında Hata Ayıklayıcısı'nda başlatılır. Uygulama çalışmıyorken bir arka plan görevinin hatalarını ayıklamak istediğiniz zaman aynı zamanda uygulamanızın başlangıç gecikme.  
  
 Uygulamanızın lansmanını geciktirmek için şunları yapabilirsiniz:  
  
-   Visual C# ve Visual Basic uygulamaları için **başlatma, ancak başlatıldığında kodumda Hata Ayıkla** üzerinde **hata ayıklama** özellik sayfası.  
  
-   Visual C++ ve JavaScript uygulamaları seçin **Hayır** gelen **uygulama Başlat** listesini **hata ayıklama** özellik sayfası.  
  
###  <a name="BKMK__Optional__Disable_network_loopbacks"></a> (İsteğe bağlı) Ağ geri döngüler devre dışı bırak  
  
 Güvenlik nedeniyle, standart bir biçimde yüklü bir UWP uygulaması üzerinde yüklü olduğu cihazın ağ çağrı yapmak için izin verilmiyor. Varsayılan olarak, Visual Studio dağıtımı bu kuraldan dağıtılmış uygulama için bir istisna oluşturur. Bu muafiyet iletişim yordamları tek bir makinede test etmenizi sağlar. Uygulamanıza Microsoft Store göndermeden önce uygulamanızı muafiyet olmadan test etmeniz gerekir.  
  
 Ağ geri döngüsüne muafiyetini kaldırmak için:  
  
-   Görsel için C# ve Visual Basic uygulamaları, NET **yerel ağ geri döngüsüne izin ver** onay kutusunu **hata ayıklama** özellik sayfası.  
  
-   Visual C++ ve JavaScript uygulamaları seçin **Hayır** gelen **yerel ağ geri döngüsüne izin** listesini **hata ayıklama** özellik sayfası.  
  
###  <a name="BKMK__Optional__Reinstall_the_app_when_you_start_debugging"></a> (İsteğe bağlı) Hata ayıklamaya başladığınızda uygulamayı yeniden yükleyin.  
 Yükleme ve Visual C# veya Visual Basic uygulamanızın ilk yapılandırma ile ilgili sorunları tanılamak için seçin **Kaldır ve yeniden yükleme paketimle** üzerinde **hata ayıklama** yeniden oluşturmak için özellik sayfası bir hata ayıklamaya başladığınızda özgün yükleme. Bu seçenek, Visual C++ ve JavaScript projeleri için kullanılabilir değildir.  
  
###  <a name="BKMK__Optional__Disable_authentication_requirement_to_start_the_remote_debugger"></a> (İsteğe bağlı) Uzaktan hata ayıklayıcıyı başlatmak için kimlik doğrulama gereksinimini devre dışı bırak  
  
 Varsayılan olarak, uzaktan hata ayıklayıcı seçtiğinizde çalıştırılacak kimlik bilgilerini sağlamanız gerekir **uzak makine** dağıtım hedefi olarak.
  
> [!IMPORTANT]
>  Kimlik doğrulaması ile uzaktan hata ayıklayıcı çalıştırmayı da seçebilirsiniz, ancak bu mod kesinlikle önerilmez. Bu modda çalıştırdığınızda, ağ güvenliği yoktur. Yalnızca ağ kötü amaçlı kod veya tehlikeli trafik risk olmadığından emin olduğunuz kimlik doğrulaması yok'ı seçin.  
  
 Kimlik doğrulama gereksinimini kaldırmak için:  
  
1.  Görsel için C# ve Visual Basic uygulamaları, select **uzak makine** olarak **hedef cihaz** üzerinde **hata ayıklama** özellik sayfası ve ardından **kimlik doğrulaması Modu** için **hiçbiri** veya **Evrensel (şifrelenmemiş Protokolü)**.
  
2.  Visual C++ ve JavaScript uygulamaları için **uzak makine** olarak **hedef cihaz** üzerinde **hata ayıklama** özellik sayfası ve ardından **gerektirir Kimlik doğrulaması** için **hiçbiri** veya **Evrensel (şifrelenmemiş Protokolü)**.  

    **Evrensel (şifrelenmemiş Protokolü)** uzak cihaza dağıtırken kullanım içindir. Şu anda bu IOT cihazları, Xbox cihazları ve HoloLens cihazlar, hem de Creators Update veya daha yeni bilgisayarlar içindir. Evrensel (şifrelenmemiş Protokolü), yalnızca güvenilen ağlarda kullanılmalıdır. Hata ayıklama bağlantıyı kesebilir ve değiştirmek geliştirme ve uzak makine arasında aktarılan veriler kötü amaçlı kullanıcılara savunmasızdır.  
  
##  <a name="BKMK_Start_the_debugging_session"></a> Hata ayıklama oturumu başlatma  
  
###  <a name="BKMK_Start_debugging__F5_"></a> (F5) hata ayıklamayı Başlat  
 Seçeneğini belirlediğinizde **hata ayıklamayı Başlat** (klavye: F5) üzerinde **hata ayıklama** menüsünde, Visual Studio başlatılır uygulamayı hata ayıklayıcısı ekli. Yürütme bir kesme noktasına ulaşıldığında, el ile özel bir durum oluştuğunda, yürütme askıya veya uygulama sona kadar devam eder.  
  
###  <a name="BKMK_Start_debugging__F5__but_delay_the_app_start"></a> Uygulama başlangıcı geciktirmek ancak (F5) hata ayıklamayı Başlat  
 Uygulamayı hata ayıklama modunda çalıştırabilir, ancak start, hata ayıklayıcı dışında bir yöntem için ayarlayabilirsiniz. Örneğin, başlatma Başlat menüsünden uygulamanızın hatalarını ayıklama veya uygulama başlatmadan bir arka plan işlemi uygulamasında hata ayıklamak için isteyebilirsiniz. Uygulama başlangıcı geciktirmek için şunu yapın:  
  
- Üzerinde **hata ayıklama** uygulamasının özellik sayfası (**hata ayıklama** Visual C++ ve JavaScript)  
  
  -   Visual C# ve Visual Basic uygulamaları seçin **başlatma, ancak başlatıldığında kodumda Hata Ayıkla**.  
  
  -   Visual C++ ve JavaScript uygulamaları seçin **Evet** gelen **uygulama Başlat** listesi.  
  
- Seçin **hata ayıklamayı Başlat** üzerinde **hata ayıklama** menü (klavye: F5).  
  
- Başlat menüsünden bir yürütme sözleşme veya başka bir yordam tarafından uygulamanızı başlatın.  
  
  Uygulamayı hata ayıklama modunda başlatır. Yürütme bir kesme noktasına ulaşıldığında, işlenmeyen bir özel durum oluşur, el ile yürütme askıya veya uygulama sona kadar devam eder.  
  
  Arka plan görevleri hata ayıklama hakkında daha fazla bilgi için bkz. [tetikleyici askıya alma, sürdürme ve arka plan olaylarını UWP uygulamaları için)](../debugger/how-to-trigger-suspend-resume-and-background-events-for-windows-store-apps-in-visual-studio.md).  
  
###  <a name="BKMK_Start_an_installed_app_in_the_debugger"></a> Yüklü bir uygulama hata ayıklayıcıda Başlat  
F5'i kullanarak hata ayıklamaya başladığınızda, Visual Studio oluşturur ve uygulamayı dağıtır, hata ayıklama modunda çalıştırmak için uygulama ayarlar ve başladıktan sonra. Bir cihazda zaten yüklü olan bir uygulamayı başlatmak için **yüklenen uygulama paketinin hatalarını ayıklama** iletişim kutusu. Bu yordam, Microsoft Store yüklü olduğu bir uygulamanın hatalarını ayıklamak ihtiyacınız olduğunda veya uygulama için kaynak dosyaları varsa, ancak uygulama için bir Visual Studio projesi yok yararlı olur. Örneğin, Visual Studio projelerinin veya çözümlerinin kullanmayan bir özel yapı sistemi olabilir.  
  
Uygulamayı yerel cihaza yüklenebilir veya uzak bir cihazda olabilir.  Uygulamayı hemen başlayabilir veya başka bir işlem veya yöntem başlatıldığında gibi Başlat menüsünden veya etkinleştirme sözleşme, uygulama, bir arka plan işlemi hata ayıklama istediğinizde, hata ayıklama modunda çalıştırmak için de ayarlayabilirsiniz hata ayıklayıcıda çalışmasını ayarlayabilirsiniz Uygulama başlatmadan. Daha fazla bilgi için [tetikleyici askıya alma, sürdürme ve arka plan olaylarını UWP uygulamaları için)](../debugger/how-to-trigger-suspend-resume-and-background-events-for-windows-store-apps-in-visual-studio.md).  
  
Yüklü bir uygulama hata ayıklayıcıda başlatmak için **hata ayıklama**, ardından **diğer hata ayıklama hedefleri**, ardından **yüklenen uygulama paketinin hatalarını ayıklama**. Ek yönergeler için bkz: [yüklü uygulama paketinin hatalarını ayıklama](../debugger/debug-installed-app-package.md).

###  <a name="BKMK_Attach_the_debugger_to_a_running_app_"></a> Çalışan bir UWP uygulaması için hata ayıklayıcının  

Çalışan bir UWP uygulamasında hata ayıklamak için seçin **hata ayıklama**, ardından **diğer hata ayıklama hedefleri**, ardından **yüklenen uygulama paketinin hatalarını ayıklama**. Ek yönergeler için bkz: [yüklü uygulama paketinin hatalarını ayıklama](../debugger/debug-installed-app-package.md).
  
###  <a name="BKMK_Attach_the_debugger_to_a_running_app_"></a> Hata ayıklayıcıyı çalışan bir Windows 8.x uygulamasına eklemek
 Hata ayıklayıcıyı iliştirmek için bir [!INCLUDE[win8_appname_long](../debugger/includes/win8_appname_long_md.md)] uygulama, hata ayıklama modunda çalışacak şekilde ayarlamak için hata ayıklanabilir Paket Yöneticisi'ni kullanmalıdır. Hata ayıklanabilir Paket Yöneticisi, Visual Studio için Uzak Araçlar ile yüklenir.  
  
 Haya ayıklayıcı bir uygulama için yararlıdır, yüklendiği bir uygulama gibi bir zaten yüklü uygulamanın hatalarını ayıklamak ihtiyacınız olduğunda [!INCLUDE[win8_appstore_long](../debugger/includes/win8_appstore_long_md.md)]. Uygulama için kaynak dosyaları varsa, ancak uygulama için bir Visual Studio projesi yok ekleme gereklidir. Örneğin, Visual Studio projelerinin veya çözümlerinin kullanmayan bir özel yapı sistemi olabilir.  
  
 Hata ayıklayıcı bir uygulamaya ekleme adımları gerektirir:  
  
1.  Uygulama hata ayıklama modunda çalışacak şekilde ayarlayın. Uygulamayı çalışır durumda olduğunda Bunun yapılması gerekir.  
  
2.  Uygulamayı başlatın. Başlangıç ekranında, bir yürütme sözleşme veya başka bir yöntem, uygulamayı başlatabilirsiniz.  
  
3.  Hata ayıklayıcı, çalışan uygulamaya ekleyin.  
  
####  <a name="BKMK_Set_the_app_to_run_in_debug_mode"></a> Hata ayıklama modunda çalıştırmak için uygulamayı Ayarla  
  
1.  Uzak Araçlar, Visual Studio için uygulamanın yüklendiği cihaza yükleyin. Bkz: [uzak araçları yükleme](../debugger/remote-debugging.md).  
  
2.  Başlangıç ekranından arama `Debuggable Package Manager` ve sonra başlatın.  
  
     UygX hata ayıklama cmdlet'i için düzgün yapılandırılmış bir PowerShell penceresi görünür.  
  
3.  Bir uygulamada hata ayıklamayı etkinleştirmek için uygulamanın Pakettamadı tanımlayıcısı belirtmeniz gerekir. Pakettamadı içeren tüm uygulamaların bir listesini görüntülemek için şunu yazın `Get-AppxPackage` PowerShell komut isteminde.  
  
4.  PowerShell komut isteminde, girin `Enable-AppxDebug` *Pakettamadı* burada *Pakettamadı* uygulamanın Pakettamadı tanımlayıcısıdır.  
  
####  <a name="BKMK_Attach_the_debugger"></a> Hata ayıklayıcının  
 Hata ayıklayıcıyı iliştirmek için:  
  
1. Üzerinde **hata ayıklama** menüsünde seçin **iliştirme**.  
  
    **İliştirme** iletişim kutusu görüntülenir.  
  
2. Uzak bir cihazdaki bir uygulamaya eklemek için Uzak cihazı belirtin **niteleyicisi** kutusu. Şunları yapabilirsiniz:  
  
   -   Adı girin **niteleyicisi** kutusu.  
  
   -   Aşağı oku seçin **niteleyicisi** kutusuna ve ardından önce eklenmiş cihazların listesinden bir cihaz seçin.  
  
   -   Seçin **Bul** yerel alt ağınız cihazlarda listesinden bir cihaz seçmek için.  
  
3. Hata ayıklamak istediğiniz kod türünü belirtin **ekleme** kutusu.  
  
    Seçin **seçin** ve ardından aşağıdakilerden birini yapın:  
  
   -   Seçin **otomatik olarak hata ayıklanacak kodun türünü belirleme**  
  
   -   Seçin **bu tür kodlarda hata ayıklama** ve ardından listeden bir veya daha fazla tür seçin.  
  
4. İçinde **kullanılabilir işlemler** listesinde, uygulama işlemini seçin.  

   > [!NOTE]
   >  Diğer uygulama türlerinin aksine, JavaScript uygulamaları wwahost.exe işlem örneğini çalıştırın. Uygulamaya ekleme yaptığınızda diğer JavaScript uygulamaları çalıştırıyorsanız, uygulamanın çalıştığı wwahost.exe sayısal işlem kimliğini (PID) bilmeniz gerekir.  
   >   
   >  Bu durumu düzeltmek için en kolay yolu, tüm diğer JavaScript uygulamaları kapatmak sağlamaktır. Aksi takdirde, uygulamayı başlatın ve wwahost.exe işlemlerin kimlikleri Not önce Windows Görev Yöneticisi'ni açın. Uygulamasındaki eklemek için bir işlem belirttiğinizde **kullanılabilir işlemler** iletişim kutusu, uygulamanın wwahost.exe not almış olanlardan çok farklı bir kimlik olacaktır.  
  
5. Seçin **ekleme**.  
  
   Visual Studio hata ayıklayıcı işleme ekler. Yürütme bir kesme noktasına ulaşıldığında, işlenmeyen bir özel durum oluşur, el ile yürütme askıya veya uygulama sona kadar devam eder.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio’da uygulamaların hatalarını ayıklama](../debugger/debug-store-apps-in-visual-studio.md)   