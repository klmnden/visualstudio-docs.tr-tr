---
title: DLL projelerinde hata ayıklama | Microsoft Docs
ms.custom: ''
ms.date: 05/23/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging DLLs
- templates, debugging DLLs
- DLLs, debugging
- debugging [Visual Studio], DLLs
ms.assetid: 433cab30-d191-460b-96f7-90d2530ca243
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 04ffdd5d0256ae0fc42b89dfa850fb0ae2d36748
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49818672"
---
# <a name="debugging-dll-projects-from-visual-studio"></a>DLL projelerinde Visual Studio'dan hata ayıklama
Aşağıdaki Visual Studio şablonlar DLL'ler oluşturur:  
  
-   (C++, C# ve Visual Basic) Sınıf kitaplığı   

-   (C++): Win32 konsol DLL projesi
  
     Daha fazla bilgi için [MFC hata ayıklama teknikleri](../debugger/mfc-debugging-techniques.md).

-   (C++, C# ve Visual Basic): Windows Forms Denetim Kitaplığı
  
     Bir Windows Forms Denetim Kitaplığı hata ayıklama, bir sınıf kitaplığı projesinin hatalarının ayıklanmasına benzer. Çoğu durumda, Windows denetimini başka bir projeden çağıracaksınız. Arama projesinde hata ayıklaması yaparken, Windows denetiminizin koduna adım, kesme noktaları ayarlayın ve diğer hata ayıklama işlemlerini gerçekleştirebilirsiniz. Daha fazla bilgi için [Windows Forms denetimleri](/dotnet/framework/winforms/controls/index).  

  
##  <a name="vxtskdebuggingdllprojectsbuildingadebugversion"></a> Hata ayıklama sürümü oluşturma  
 Nasıl hata ayıklamaya başladığınızda ne olursa olsun, DLL hata ayıklama sürümünü derlediğinizden ve hata ayıklama sürümü burada uygulama onu bulmayı beklediği konumda olduğundan emin olun emin olun. Bu belirgin görünebilir, ancak bu adımı unutursanız, uygulama farklı bir DLL sürümünü bulup ve yükleyebilir. Program neden kesme noktasına hiç isabet edilmediğini düşünürsünüz çalışmaya devam eder. Hata ayıklama, hangi DLL'lerin hata ayıklayıcı'nın açarak, programınızın yüklediğini doğrulayabilirsiniz **modülleri** penceresi. **Modülleri** penceresi, her bir DLL veya EXE ayıkladığınız işlemde yüklü listeler. Daha fazla bilgi için [nasıl yapılır: modüller penceresini kullanma](../debugger/how-to-use-the-modules-window.md).  
 C++ programında yazılan koda eklenmesi hata ayıklayıcı için kod yaymalıdır `DebuggableAttribute`. Bu, kodunuzu otomatik olarak ile bağlayarak ekleyebileceğiniz [assemblydebug](/cpp/build/reference/assemblydebug-add-debuggableattribute) bağlayıcı seçeneği.  
  
##  <a name="vxtskdebuggingdllprojectsmixedmodedebugging"></a> Karışık mod hata ayıklama  
 DLL'nizi çağıran arama uygulaması yönetilen kod veya yerel kodda yazılabilir. Yönetilen DLL'niz yerel kodla çağrılır ve her ikisi de hata ayıklamak istediğiniz yönetilen ve yerel hata ayıklayıcılarının her ikisi de etkinleştirilmelidir. Bu konuda seçebileceğiniz  **\<Proje > özellik sayfaları** iletişim kutusu ya da pencere. Bunu nasıl yapacağınız mı DLL projesi veya çağıran uygulama projesinden hata ayıklamaya başladığınızda üzerinde bağlıdır. Daha fazla bilgi için [nasıl yapılır: karışık modda hata ayıklama](../debugger/how-to-debug-in-mixed-mode.md).  
  
##  <a name="vxtskdebuggingdllprojectschangingdefaultconfigurations"></a> Varsayılan yapılandırmaları değiştirme  
 Proje şablonuyla bir konsol uygulama projesi oluşturduğunuzda [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] hata ayıklama ve yayın yapılandırmaları için gereken ayarları otomatik olarak oluşturur. Gerekirse, bu ayarları değiştirebilirsiniz. Daha fazla bilgi için [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md), [C# hata ayıklama yapılandırmaları için proje ayarları](../debugger/project-settings-for-csharp-debug-configurations.md), [Visual Basic hata ayıklama yapılandırması proje ayarları ](../debugger/project-settings-for-a-visual-basic-debug-configuration.md), ve [nasıl yapılır: kümesi hata ayıklama ve yayın yapılandırmaları](../debugger/how-to-set-debug-and-release-configurations.md).  
  
##  <a name="vxtskdebuggingdllprojectswaystodebugthedll"></a> DLL hatalarını ayıklamanın yolları  
 Bu bölümdeki projelerin her biri bir DLL oluşturur. Bir DLL'yi doğrudan çalıştıramazsınız; genellikle bir EXE bir uygulama tarafından çağrılmalıdır. Daha fazla bilgi için [oluşturma ve yönetme, Visual C++ projeleri](/cpp/ide/creating-and-managing-visual-cpp-projects). Arama uygulaması aşağıdaki ölçütlerden herhangi bir uygun olmayabilir:  
  
- Başka bir projede aynı oluşturulmuş bir uygulamada [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] sınıf kitaplığını içeren çözüm.  
  
- Zaten bir test veya üretim bilgisayarına dağıtılmış var olan bir uygulama.  
  
- Web'de bulundu ve bir URL yoluyla erişildi.  
  
- DLL'yi gömen bir Web sayfasını içeren bir Web uygulaması.  
  
###  <a name="vxtskdebuggingdllprojectsthecallingapplication"></a> Çağıran uygulamanın hatalarını ayıklamaya  
Bir DLL'de hata ayıklamak için çağıran uygulama, genellikle bir EXE veya bir Web uygulaması hata ayıklayarak başlayın. Hata ayıklamanın birkaç yolu vardır.  
  
- Çağıran uygulama için bir proje varsa, bu projeyi açmak ve yürütmeyi başlatabilirsiniz **hata ayıklama** menüsü. Daha fazla bilgi için [hata ayıklayıcısını kullanmaya başlama](../debugger/getting-started-with-the-debugger.md).  
  
- Çağıran uygulama zaten bir test veya üretim bilgisayarına dağıtılmış var olan bir programsa ve zaten çalışıyorsa buna ekleyebilirsiniz. DLL, Internet Explorer tarafından barındırılan denetimse veya Web sayfası denetiminde ise bu yöntemi kullanın. Daha fazla bilgi için [nasıl yapılır: çalışan bir işleme eklenme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).  
  
- DLL projesinden ayıklayabilirsiniz. Daha fazla bilgi için [nasıl yapılır: DLL projesinde hata ayıklama](../debugger/how-to-debug-from-a-dll-project.md).  
  
- Buradan hata ayıklama [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] [komut penceresi](#vxtskdebuggingdllprojectstheimmediatewindow). Bu durumda, **hemen** penceresi uygulamanın uygulamanın rolünü üstlenir.  
  
Çağıran uygulamanın hatalarını ayıklamaya başlamadan önce genellikle sınıf kitaplığında bir kesme noktası ayarlamak istersiniz. Daha fazla bilgi için [kullanılarak kesme noktaları](../debugger/using-breakpoints.md). Kesme noktası isabet edildiğinde sorunu yalıtana kadar her bir satırdaki eylemi gözleme kodda adım adım. Daha fazla bilgi için [hata ayıklayıcısı koda gitmek](../debugger/navigating-through-code-with-the-debugger.md).
  
###  <a name="vxtskdebuggingdllprojectstheimmediatewindow"></a> Komut penceresi  
 Çağıran uygulama olmadan DLL'de işlevleri veya değerlendirebilirsiniz. Tasarım zamanı hata ayıklama yapın ve kullandığınız **hemen** penceresi. DLL projesi açıkken bu şekilde hata ayıklamak için aşağıdaki adımları izleyin:  
  
1.  Hata ayıklayıcı açın **hemen** penceresi.  
  
2.  Adlı bir yöntem test etmek için `Test` sınıfında `Class1`, türünde bir nesne örneği `Class1` aşağıdaki C# kodunu hemen penceresine yazarak. Bu yönetilen kod Visual Basic ve C++ için uygun sözdizimini değişikliklerle birlikte çalışır:  
  
    ```cpp
    Class1 obj = new Class1();  
    ```  
  
     C# seçeneğinde tüm adlar tam olarak nitelenmiş olmalıdır. Ayrıca, yöntemlerin veya değişkenlerin geçerli kapsamda ve hata ayıklama oturumu bağlamında olması gerekir.  
  
3.  Varsayarak `Test` alır `int` parametresi değerlendirmek `Test` kullanarak **hemen** penceresi:  
  
    ```cpp
    ?obj.Test(10)  
    ```  
  
     Sonuç yazdırılır **hemen** penceresi.  
  
4.  Hata ayıklamaya devam edebilirsiniz `Test` içine bir kesme noktası yerleştirerek ve sonra işlevi yeniden değerlendirerek tarafından:  
  
    ```cpp
    ?obj.Test(10);  
    ```  
  
     Kesme noktasına isabet edilir ve adım adım olacaktır `Test`. Yürütme ayrıldıktan sonra `Test`, hata ayıklayıcı, Tasarım modunda olur.

## <a name="vxtskdebuggingdllprojectsexternal"></a> Bir C++ projeden harici bir DLL'nin hatasını ayıklayın

Projenize bir DLL dış ayıklıyorsanız, hata ayıklama özellikleri kullanılabilir (kod içerisinde ilerlemeye gibi) bağlı olacaktır [DLL'nin hata ayıklama Yapılandırması](#vxtskdebuggingdllprojectsbuildingadebugversion) derlendiği ve olup olmadığını [.pdbdosyası](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md) ve diğer gerekli dosyaları DLL için kullanılabilir.

Projenizi DLL ve hata ayıklama için kullanılan .pdb dosyasını bulmak yapabilmesi gerekir. Bu dosyaları kopyalamak için bir özel yapı görev oluşturabilirsiniz  **\<proje klasörü > \Debug** çıktı klasörü veya kopyalayabilir dosyaları çıktı klasörüne el ile.

Üst bilgi dosyaları konumlarını kolayca ayarlayabilirsiniz ve <em>özellik sayfalarındaki .lib dosyaları (C++ projesini sağ tıklatın ve seçin ** Görünüm Özellikleri</em><em>ve ardından **tüm yapılandırmaları</em>* ) bunları, çıktı klasörüne kopyalamak zorunda kalmadan:

- C/C++ klasörü (genel kategori) - üst bilgi dosyalarını içeren klasörü belirtin **ek içerik dizinleri** alan.
- Bağlayıcı klasörü (genel kategori) - .lib dosyayı içeren klasörü belirtin **ek kitaplıklar dizinleri** alan. 
- Bağlayıcı klasörü (Giriş kategorisi) - .lib dosyasına için dosya adı ve tam yolunu belirtin **ek bağımlılıklar** alan.

Yapılandırma doğru olduğunda yürütmeyi başlatarak ayıklayabilirsiniz **hata ayıklama** menüsü.

Proje ayarları hakkında daha fazla bilgi için bkz. [özellik sayfaları (Visual C++)](/cpp/ide/property-pages-visual-cpp).
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)   
 [Visual C++ proje türleri](../debugger/debugging-preparation-visual-cpp-project-types.md)   
 [C#, F # ve Visual Basic proje türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [C++ hata ayıklama yapılandırması proje ayarları](../debugger/project-settings-for-a-cpp-debug-configuration.md)   
 [Hata ayıklama yapılandırması proje ayarları C#](../debugger/project-settings-for-csharp-debug-configurations.md)   
 [Hata ayıklama yapılandırması proje ayarları bir Visual Basic](../debugger/project-settings-for-a-visual-basic-debug-configuration.md)   
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
