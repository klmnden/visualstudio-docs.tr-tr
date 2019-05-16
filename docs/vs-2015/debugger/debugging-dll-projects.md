---
title: DLL projelerinde hata ayıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging DLLs
- templates, debugging DLLs
- DLLs, debugging
- debugging [Visual Studio], DLLs
ms.assetid: 433cab30-d191-460b-96f7-90d2530ca243
caps.latest.revision: 41
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4a4533c304f84d9dc59ec6b05328528870e49655
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65691393"
---
# <a name="debugging-dll-projects"></a>DLL Projelerinde Hata Ayıklama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aşağıdaki şablonlar DLL'ler oluşturur:  
  
- (C++, C# ve Visual Basic) Sınıf kitaplığı  
  
- (C++, C#ve Visual Basic): Windows Forms Denetim Kitaplığı  
  
   Bir Windows Denetim Kitaplığı hata ayıklama, bir sınıf kitaplığı projesinin hatalarının ayıklanmasına benzer. Çoğu durumda, Windows denetimini başka bir projeden çağıracaksınız. Arama projesinde hata ayıklaması yaparken, Windows denetiminizin koduna adım, kesme noktaları ayarlayın ve diğer hata ayıklama işlemlerini gerçekleştirebilirsiniz. Daha fazla bilgi için [Windows Forms denetimleri](https://msdn.microsoft.com/library/f050de8f-4ebd-4042-94b8-edf9a1dbd52a).  
  
- (C# ve Visual Basic): Web Denetim Kitaplığı  
  
   Daha fazla bilgi için [Web denetim kitaplığı (yönetilen kod)](../debugger/web-control-library-managed-code.md).  
  
- (C++): MFC ActiveX denetimi ve MFC akıllı cihaz ActiveX denetimi  
  
   ActiveX denetimleri, bir istemci bilgisayara Internet üzerinden indirilebilir ve görüntülenen ve Web sayfalarında etkinleştirilmiş denetimlerdir.  
  
   ActiveX denetimlerinin hatalarının ayıklanması, çünkü bunlar bağımsız olarak çalıştırılamaz, ancak bir HTML Web sayfasına gömülmesi diğer denetim türlerinin hatalarının ayıklanmasına benzer. Daha fazla bilgi için [nasıl yapılır: Bir ActiveX denetiminde hata ayıklama](../debugger/how-to-debug-an-activex-control.md).  
  
- (C++): MFC akıllı cihaz DLL  
  
   Daha fazla bilgi için [MFC hata ayıklama teknikleri](../debugger/mfc-debugging-techniques.md).  
  
  Bu bölüm aşağıdaki konular hakkında bilgi de içerir:  
  
- [Nasıl yapılır: DLL Projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md)  
  
- [Nasıl yapılır: Karışık Modda Hata Ayıklama](../debugger/how-to-debug-in-mixed-mode.md)  
  
  Bu konu, hata ayıklama sınıf kitaplıklarının hazırlanması hakkında dikkat edilecek noktalar sağlayan aşağıdaki bölümleri içerir:  
  
- [Hata ayıklama sürümü oluşturma](#vxtskdebuggingdllprojectsbuildingadebugversion)  
  
- [Karışık mod hata ayıklama](#vxtskdebuggingdllprojectsmixedmodedebugging)  
  
- [Varsayılan yapılandırmaları değiştirme](#vxtskdebuggingdllprojectschangingdefaultconfigurations)  
  
- [DLL hatalarını ayıklamanın yolları](#vxtskdebuggingdllprojectswaystodebugthedll)  
  
- [Arama uygulaması](#vxtskdebuggingdllprojectsthecallingapplication)  
  
- [Bir Web sayfasındaki denetimler](#vxtskdebuggingdllprojectscontrolsonawebpage)  
  
- [Komut penceresi](#vxtskdebuggingdllprojectstheimmediatewindow)  
  
## <a name="vxtskdebuggingdllprojectsbuildingadebugversion"></a> Hata ayıklama sürümü oluşturma  
 Nasıl hata ayıklamaya başladığınızda ne olursa olsun, DLL hata ayıklama sürümünü derlediğinizden ve hata ayıklama sürümü burada uygulama onu bulmayı beklediği konumda olduğundan emin olun emin olun. Bu belirgin görünebilir, ancak bu adımı unutursanız, uygulama farklı bir DLL sürümünü bulup ve yükleyebilir. Program neden kesme noktasına hiç isabet edilmediğini düşünürsünüz çalışmaya devam eder. Hata ayıklama, hangi DLL'lerin hata ayıklayıcı'nın açarak, programınızın yüklediğini doğrulayabilirsiniz **modülleri** penceresi. **Modülleri** penceresi, her bir DLL veya EXE ayıkladığınız işlemde yüklü listeler. Daha fazla bilgi için [nasıl yapılır: Modüller penceresini kullanma](../debugger/how-to-use-the-modules-window.md).  
  
 C++ programında yazılan koda eklenmesi hata ayıklayıcı için kod yaymalıdır `DebuggableAttribute`. Bu, kodunuzu otomatik olarak ile bağlayarak ekleyebileceğiniz [assemblydebug](https://msdn.microsoft.com/library/94443af3-470c-41d7-83a0-7434563d7982) bağlayıcı seçeneği.  
  
## <a name="vxtskdebuggingdllprojectsmixedmodedebugging"></a> Karışık mod hata ayıklama  
 DLL'nizi çağıran arama uygulaması yönetilen kod veya yerel kodda yazılabilir. Yönetilen DLL'niz yerel kodla çağrılır ve her ikisi de hata ayıklamak istediğiniz yönetilen ve yerel hata ayıklayıcılarının her ikisi de etkinleştirilmelidir. Bu konuda seçebileceğiniz  **\<Proje > özellik sayfaları** iletişim kutusu ya da pencere. Bunu nasıl yapacağınız mı DLL projesi veya çağıran uygulama projesinden hata ayıklamaya başladığınızda üzerinde bağlıdır. Daha fazla bilgi için [nasıl yapılır: Karışık modda hata ayıklama](../debugger/how-to-debug-in-mixed-mode.md).  
  
## <a name="vxtskdebuggingdllprojectschangingdefaultconfigurations"></a> Varsayılan yapılandırmaları değiştirme  
 Proje şablonuyla bir konsol uygulama projesi oluşturduğunuzda [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] hata ayıklama ve yayın yapılandırmaları için gereken ayarları otomatik olarak oluşturur. Gerekirse, bu ayarları değiştirebilirsiniz. Daha fazla bilgi için [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md), [proje ayarları C# hata ayıklama yapılandırmaları](../debugger/project-settings-for-csharp-debug-configurations.md), [Visual Basic hata ayıklama proje ayarları Yapılandırma](../debugger/project-settings-for-a-visual-basic-debug-configuration.md), ve [nasıl yapılır: Küme hata ayıklama ve yayın yapılandırmaları](../debugger/how-to-set-debug-and-release-configurations.md).  
  
## <a name="vxtskdebuggingdllprojectswaystodebugthedll"></a> DLL hatalarını ayıklamanın yolları  
 Bu bölümdeki projelerin her biri bir DLL oluşturur. Bir DLL'yi doğrudan çalıştıramazsınız; genellikle bir EXE bir uygulama tarafından çağrılmalıdır. Daha fazla bilgi için [oluşturma ve yönetme, Visual C++ projeleri](https://msdn.microsoft.com/library/11003cd8-9046-4630-a189-a32bf3b88047). Arama uygulaması aşağıdaki ölçütlerden herhangi bir uygun olmayabilir:  
  
- Başka bir projede aynı oluşturulmuş bir uygulamada [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] sınıf kitaplığını içeren çözüm.  
  
- Zaten bir test veya üretim bilgisayarına dağıtılmış var olan bir uygulama.  
  
- Web'de bulundu ve bir URL yoluyla erişildi.  
  
- DLL'yi gömen bir Web sayfasını içeren bir Web uygulaması.  
  
### <a name="vxtskdebuggingdllprojectsthecallingapplication"></a> Çağıran uygulamanın hatalarını ayıklama  
 Bir DLL'de hata ayıklamak için çağıran uygulama, genellikle bir EXE veya bir Web uygulaması hata ayıklayarak başlayın. Hata ayıklamanın birkaç yolu vardır.  
  
- Çağıran uygulama için bir proje varsa, bu projeyi açmak ve yürütmeyi başlatabilirsiniz **hata ayıklama** menüsü. Daha fazla bilgi için [nasıl yapılır: Yürütme işlemini başlatmadan](https://msdn.microsoft.com/b0fe0ce5-900e-421f-a4c6-aa44ddae453c).  
  
- Çağıran uygulama zaten bir test veya üretim bilgisayarına dağıtılmış var olan bir programsa ve zaten çalışıyorsa buna ekleyebilirsiniz. DLL, Internet Explorer tarafından barındırılan denetimse veya Web sayfası denetiminde ise bu yöntemi kullanın. Daha fazla bilgi için [nasıl yapılır: Bir çalışan işleme ekleme](https://msdn.microsoft.com/636d0a52-4bfd-48d2-89ad-d7b9ca4dc4f4).  
  
- DLL projesinden ayıklayabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Bir DLL projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md).  
  
- Buradan hata ayıklama [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] **hemen** penceresi. Bu durumda, **hemen** penceresi uygulamanın uygulamanın rolünü üstlenir.  
  
  Çağıran uygulamanın hatalarını ayıklamaya başlamadan önce genellikle sınıf kitaplığında bir kesme noktası ayarlamak istersiniz. Daha fazla bilgi için [kesme noktaları ve izleme noktaları](https://msdn.microsoft.com/fe4eedc1-71aa-4928-962f-0912c334d583). Kesme noktası isabet edildiğinde sorunu yalıtana kadar her bir satırdaki eylemi gözleme kodda adım adım. Daha fazla bilgi için [kodu Adımlama genel bakış](https://msdn.microsoft.com/8791dac9-64d1-4bb9-b59e-8d59af1833f9).  
  
### <a name="vxtskdebuggingdllprojectscontrolsonawebpage"></a> Bir Web sayfasındaki denetimler  
 Bir Web sayfası denetiminde hata ayıklamak için oluşturun bir [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] böyle bir sayfa zaten mevcut değilse, onu katıştıran bir sayfa. Denetim kodunun yanı sıra Web sayfasının koduna ardından kesme noktaları yerleştirin. Daha sonra Web sayfasından çağırmanız [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
 Çağıran uygulamanın hatalarını ayıklamaya başlamadan önce genellikle DLL'de bir kesme noktası ayarlamak istersiniz. Kesme noktası isabet edildiğinde sorunu yalıtana kadar her bir satırdaki eylemi gözleme kodda adım adım. Daha fazla bilgi için [kesme noktaları ve izleme noktaları](https://msdn.microsoft.com/fe4eedc1-71aa-4928-962f-0912c334d583).  
  
### <a name="vxtskdebuggingdllprojectstheimmediatewindow"></a> Komut penceresi  
 Çağıran uygulama olmadan DLL'de işlevleri veya değerlendirebilirsiniz. Tasarım zamanı hata ayıklama yapın ve kullandığınız **hemen** penceresi. DLL projesi açıkken bu şekilde hata ayıklamak için aşağıdaki adımları izleyin:  
  
1. Hata ayıklayıcı açın **hemen** penceresi.  
  
2. Adlı bir yöntem test etmek için `Test` sınıfında `Class1`, türünde bir nesne örneği `Class1` aşağıdaki C# kodunu hemen penceresine yazarak. Bu yönetilen kod Visual Basic ve C++ için uygun sözdizimini değişikliklerle birlikte çalışır:  
  
    ```  
    Class1 obj = new Class1();  
    ```  
  
     C# seçeneğinde tüm adlar tam olarak nitelenmiş olmalıdır. Ayrıca, yöntemlerin veya değişkenlerin geçerli kapsamda ve hata ayıklama oturumu bağlamında olması gerekir.  
  
3. Varsayarak `Test` alır `int` parametresi değerlendirmek `Test` kullanarak **hemen** penceresi:  
  
    ```  
    ?obj.Test(10)  
    ```  
  
     Sonuç yazdırılır **hemen** penceresi.  
  
4. Hata ayıklamaya devam edebilirsiniz `Test` içine bir kesme noktası yerleştirerek ve sonra işlevi yeniden değerlendirerek tarafından:  
  
    ```  
    ?obj.Test(10);  
    ```  
  
     Kesme noktasına isabet edilir ve adım adım olacaktır `Test`. Yürütme ayrıldıktan sonra `Test`, hata ayıklayıcı, Tasarım modunda olur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Visual C++ proje türleri](../debugger/debugging-preparation-visual-cpp-project-types.md)   
 [C#, F#ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)   
 [Hata ayıklama yapılandırması proje ayarları C#](../debugger/project-settings-for-csharp-debug-configurations.md)   
 [Hata ayıklama yapılandırması proje ayarları bir Visual Basic](../debugger/project-settings-for-a-visual-basic-debug-configuration.md)   
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
