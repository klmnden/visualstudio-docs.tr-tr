---
title: Android ve iOS üzerinde OpenGL ES uygulaması derleme | Microsoft Docs
ms.custom: ''
ms.date: 05/16/2019
ms.technology: vs-ide-mobile
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 76a67886-df57-4a81-accb-2e3c2eaf607b
author: corob-msft
ms.author: corob
manager: jillfra
ms.workload:
- xplat-cplusplus
ms.openlocfilehash: aa8ffe308f8a1181ed18af52ba7537c46007de94
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66317646"
---
# <a name="build-an-opengl-es-application-on-android-and-ios"></a>Android ve iOS üzerinde OpenGL ES uygulaması oluşturma

Visual Studio çözümleri ve iOS uygulamaları ve ortak kod paylaşma Android uygulamaları için projeler oluşturabilirsiniz. Bu makalede, bir basit bir iOS uygulamasının hem Android yerel etkinlik uygulaması oluşturan bir çözüm şablonu aracılığıyla size yol gösterir. C++ kodu, uygulamalar her platformda aynı animasyonlu döndürme küpünü görüntülemek için OpenGL ES kullanan ortak sahiptir. OpenGL ES (Embedded Systems veya GLES için OpenGL) bir 2D ve 3D grafikler mobil cihazlarda desteklenen API ' dir.

## <a name="requirements"></a>Gereksinimler

İOS ve Android için OpenGL ES uygulama oluşturabilmeniz için önce tüm sistem gereksinimlerini karşılamanızın emin olun. Henüz yapmadıysanız, mobil uygulama geliştirme ile yükleme C++ Visual Studio Yükleyicisi'nde iş yükü. İOS için oluşturmak için isteğe bağlı dahil C++ iOS geliştirme araçları. Android için tasarlayabilmek üzere yükleme C++ Android geliştirme araçları ve gerekli üçüncü taraf araçları: Yürütme Yöneticisi Android NDK, Apache Ant, Google Android öykünücüsü ve Intel donanım hızlandırılmış. Ardından, Intel HAXM ve sisteminizde çalıştırmak için Android öykünücüsü yapılandırın. Daha fazla bilgi ve ayrıntılı yönergeler için bkz. [platformlar arası Mobil Geliştirme için Visual C++ yükleme](../cross-platform/install-visual-cpp-for-cross-platform-mobile-development.md). Yapı ve test iOS uygulaması için bir Mac ihtiyaç duyarsınız bilgisayar, yükleme yönergelerine göre ayarlayın. İOS geliştirme için ayarlama hakkında daha fazla bilgi için bkz: [yükleme ve yapılandırma araçları kullanarak iOS oluşturmak için](../cross-platform/install-and-configure-tools-to-build-using-ios.md)

## <a name="create-a-new-opengles-application-project"></a>Yeni bir OpenGLES uygulaması projesi oluşturma

Bu öğreticide, ardından oluşturabilir ve varsayılan uygulamasını Android için Visual Studio öykünücüsü'nün içinde çalıştırmak önce yeni bir OpenGL ES uygulaması projesi oluşturun. Ardından iOS için uygulama oluşturun ve uygulamayı bir iOS cihazında çalıştırın.

1. Visual Studio'da **dosya** > **yeni** > **proje**.

1. İçinde **yeni proje** iletişim kutusunun **şablonları**, seçin **Visual C++**  > **Çoklu Platform**seçin **OpenGLES uygulaması (Android, iOS)** şablonu.

1. Uygulama gibi bir ad verin `MyOpenGLESApp`ve ardından **Tamam**.

   ![Yeni bir OpenGLES uygulaması projesi](../cross-platform/media/cppmdd_opengles_newproj.PNG "CPPMDD_OpenGLES_NewProj")

   Visual Studio, yeni bir çözüm oluşturur ve Çözüm Gezgini açılır.

   ![Çözüm Gezgini'nde MyOpenGLESApp](../cross-platform/media/cppmdd_opengles_solexpl.PNG "CPPMDD_OpenGLES_SolExpl")

   Yeni bir OpenGL ES uygulaması çözümü, üç kitaplık projeleri ve iki uygulama projeleri içerir. Kitaplık klasörüne bir paylaşılan kod projesi ve Paylaşılan koda başvuran iki platforma özgü projeler içerir:

- `MyOpenGLESApp.Android.NativeActivity` Uygulamanızı yerel bir Android etkinliği olarak uygulayan basitleştirin ve başvurular içerir. Giriş noktaları tutkal kodun uygulanan *Main.cpp öğesi*, ortak paylaşılan kodu içeren `MyOpenGLESApp.Shared`. Önceden derlenmiş üst bilgiler bulunduğunuz *pch.h*. Bu yerel etkinlik uygulaması projesi paylaşılan kitaplığa derlenir ( *.so*) tarafından teslim dosyasını `MyOpenGLESApp.Android.Packaging` proje.

- `MyOpenGLESApp.iOS.StaticLibrary` bir iOS statik kitaplık oluşturur ( *.a*) paylaşılan kodu içeren dosya `MyOpenGLESApp.Shared`. Tarafından oluşturulan uygulama için bağlı `MyOpenGLESApp.iOS.Application` proje.

- `MyOpenGLESApp.Shared` platformlar arasında çalışır paylaşılan kodu içerir. Önişlemci makroları platforma özgü kod koşullu derleme için kullanır. Her iki proje başvurusu tarafından paylaşılan kod teslim `MyOpenGLESApp.Android.NativeActivity` ve `MyOpenGLESApp.iOS.StaticLibrary`.

Çözüm, Android ve iOS platformlara yönelik uygulamalar oluşturmak için iki proje vardır:

- `MyOpenGLESApp.Android.Packaging` oluşturur *.apk* dosyası dağıtım için bir Android cihaz veya öykünücü. Bu dosya, kaynakları ve bildirim özelliklerini ayarladığınız yerdir AndroidManifest.xml dosyası içerir. Ayrıca içerdiği *build.xml* Ant denetleyen dosya oluşturma işlemi. Dağıtılan ve doğrudan Visual Studio'dan çalıştırma varsayılan olarak, başlangıç projesi olarak ayarlanır.

- **MyOpenGLESApp.iOS.Application** C++ statik kitaplık kodu bağlanan bir iOS uygulaması oluşturmak için Objective-C basitleştirin ve kaynakları içeren `MyOpenGLESApp.iOS.StaticLibrary`. Bu proje, Mac için Visual Studio ve uzak aracı tarafından aktarılan bir derleme paketi oluşturur. Bu proje oluşturduğunuzda, Visual Studio Mac uygulamanızı oluşturup komutları ve dosya gönderir.

## <a name="build-and-run-the-android-app"></a>Android uygulaması derleyebilir ve çalıştırabilirsiniz

Şablon tarafından oluşturulan çözüm Android uygulamasını varsayılan proje olarak ayarlar.  Derleme ve yükleme ve Kurulum doğrulamak için bu uygulamayı çalıştırın. İlk test için Android için öykünücüsü tarafından yüklenen cihaz profilleri bir uygulamayı çalıştırın. Başka bir hedef uygulamanızı test etmek isterseniz, hedef öykünücü yükleyin veya cihazı bilgisayarınıza bağlayın.

### <a name="to-build-and-run-the-android-native-activity-app"></a>Derleme ve Android yerel etkinlik uygulaması çalıştırmak için

1. Zaten seçili değilse, seçin **x86** gelen **çözüm platformları** aşağı açılan listesi.

   ![Çözüm Platformu ayarlamak için x86](../cross-platform/media/cppmdd_opengles_solutionplat.png "CPPMDD_OpenGLES_SolutionPlat")

   X86 öykünücüsünü hedeflemek için kullanın. Bir cihazı hedeflemeniz için cihaz işlemci üzerinde çözüm platformu seçin. Varsa **çözüm platformları** seçin, listeyi görüntülenmiyorsa **çözüm platformları** gelen **Ekle/Kaldır düğmeleri** listeleyin ve ardından platformunuzu seçin.

1. İçinde **Çözüm Gezgini**, kısayol menüsünü açın `MyOpenGLESApp.Android.Packaging` proje ve ardından **yapı**.

   ![Android paketleme projesi derleme](../cross-platform/media/cppmdd_opengles_andbuild.png "CPPMDD_OpenGLES_AndBuild")

   Android kitaplığı ve Android uygulamasını paylaşılan için çıkış penceresine yapı işleminin çıkış görüntüler.

   ![Android projeleri için derleme çıkışı](../cross-platform/media/cppmdd_opengles_andoutput.png "CPPMDD_OpenGLES_AndOutput")

1. Benzetilmiş bir Android cihaz profilleri, dağıtım hedefi seçin.

   ![Dağıtım hedefini seçin](../cross-platform/media/cppmdd_opengles_pickemulator.png "CPPMDD_OpenGLES_PickEmulator")

   Diğer öykünücü yüklü veya bir Android cihazına bağlı, dağıtım hedef açılan listeden seçebilirsiniz. Uygulamayı çalıştırmak için yerleşik Çözüm Platformu hedef cihaz platformunu eşleşmesi gerekir.

1. Hata ayıklamayı başlatmak için F5'e veya hata ayıklama olmadan Başlat için Shift + F5 tuşlarına basın.

   Visual Studio öykünücü, yüklemek ve kodunuzu dağıtmak için birkaç saniye sürer başlatır. Uygulamayı öykünücüde nasıl göründüğü aşağıda gösterilmiştir:

   ![Android öykünücüsünde çalışan uygulama](../cross-platform/media/cppmdd_opengles_andemulator.png "CPPMDD_OpenGLES_AndEmulator")

   Uygulama başlatıldıktan sonra kesme noktaları ayarlayın ve hata ayıklayıcı kodunuz içinde adım adım, Yereller inceleyin ve izlemek için kullanın.

1. Tuşuna **Shift**+**F5** hata ayıklamayı durdurmak için.

   Öykünücüyü çalıştırmak için devam eden ayrı bir işlemdir. Düzenleme, derleme ve kodunuzun birden çok kez aynı öykünücüye dağıtmak. Uygulamanızı öykünücü uygulama Koleksiyonu'na görünür ve bunu doğrudan buradan başlatılabilir.

   C++ put oluşturulan Android yerel etkinlik uygulaması ve kitaplık projeleri Android platformu ile arabirim oluşturmak için "Yapıştırıcı" kod içeren bir dinamik kitaplık kodu paylaşılan. Çoğu uygulama kodu, kitaplık ve bildirimi, kaynakları ve derleme yönergeleri paketleme projesi içerisine olmasıdır. Paylaşılan kodun NativeActivity projedeki Main.cpp olarak çağrılır. Android NDK Geliştirici programına Android yerel etkinlik hakkında daha fazla bilgi için bkz [kavramları](https://developer.android.com/ndk/guides/concepts.html) sayfası.

   Visual Studio Android platform araç takımını Clang kullanan NDK, kullanarak Android yerel etkinlik projeleri derler. Visual Studio derle, bağlama ve hedef platformda hata ayıklama için kullanılan seçeneklerini NativeActivity proje özelliklerinde eşleştirir. Ayrıntılar için açık **özellik sayfaları** MyOpenGLESApp.Android.NativeActivity proje için iletişim kutusu. Komut satırı anahtarları hakkında daha fazla bilgi için bkz. [Clang derleyici kullanıcının el ile](http://clang.llvm.org/docs/UsersManual.html).

## <a name="build-and-run-the-ios-app-on-an-ios-device"></a>Bir iOS cihazında iOS uygulaması derleyebilir ve

İOS uygulama projesi oluşturulur ve Visual Studio'da düzenlenemez, ancak lisans kısıtlamaları nedeniyle, oluşturulan ve gerekir bir Mac'ten dağıtılan Visual Studio, proje dosyaları aktarmak ve derleme, dağıtım ve hata ayıklama komutları yürütmek için Mac bilgisayarda çalışan uzak bir aracı ile iletişim kurar. Ayarlama ve Visual Studio ve Mac kullanarak iOS uygulaması oluşturmadan önce iletişim kurmak için yapılandırma. Ayrıntılı yönergeler için bkz. [yükleme ve yapılandırma araçları kullanarak iOS derleme](../cross-platform/install-and-configure-tools-to-build-using-ios.md). Uzak Aracı, Mac üzerinde çalışan ve Visual Studio ile eşleştirilmiş sonra oluşturun ve yükleme ve Kurulum doğrulamak üzere iOS uygulamasını çalıştırın.

Bir iOS uygulamasını iOS cihazına dağıtmak için de otomatik Mac'te Xcode üzerinde kaydolma ayarlamanız gerekir Otomatik imzalama otomatik olarak uygulama imzalama yönetir ve uygulamanın bir derlemeyi imzalamak için bir sağlama profili oluşturur.

### <a name="to-set-up-automatic-signing-on-xcode"></a>Üzerinde Xcode otomatik imzalama ayarlamak için

1. Henüz yapmadıysanız, yükleme [Xcode](https://developer.apple.com/xcode/downloads/) Mac'inizde 10.2.1 sürümü veya sonraki bir sürümü

1. Mac'te Xcode uygulamasını açın.

1. Yeni bir **tek görünüm uygulaması** Xcode projesi. Proje oluşturma sırasında gerekli alanları doldurun. Projeyi yalnızca daha sonra uygulamanın bir derlemeyi imzalamak için kullanılan bir sağlama profili oluşturmak için kullanılan rastgele, değerler de olabilir.

1. İçinde kayıtlı, Apple kimliği Ekle bir [Apple Developer Program](https://developer.apple.com/programs/) hesap için Xcode. Apple Kimliğinizi, uygulamaları imzalamak için imzalama kimliği kullanılır. Xcode'da imzalama kimliğinizi eklemek için açın **Xcode** menüsünü seçip **tercihleri**. Seçin **hesapları** ve Apple kimliğinizi eklemek için Ekle düğmesini (+) tıklayın. Ayrıntılı yönergeler için bkz. [Apple kimliği hesabınızı eklemek](https://help.apple.com/xcode/mac/current/#/devaf282080a).

1. Xcode proje "Genel" ayarlarından değiştirin **paket grubu tanımlayıcısı** için `com.<NameOfVSProject>`burada `<NameOfVSProject>` oluşturduğunuz Visual Studio çözüm projesi olarak aynı adı. Örneğin, adlı bir proje oluşturduğunuz `MyOpenGLESApp` Visual Studio, ardından ayarlayın **paket grubu tanımlayıcısı** için `com.MyOpenGLESApp`.

   ![Xcode paket grubu tanımlayıcısı](../cross-platform/media/cppmdd-opengles-iosxcodeid.png "CPPMDD_OpenGLES_iOSXcodeId")

1. Otomatik imzalamayı etkinleştirmek için işaretleyin. Otomatik olarak imzalanmasını yönetmek **.

   ![Xcode otomatik imzalama](../cross-platform/media/cppmdd-opengles-iosxcodesign.png "CPPMDD_OpenGLES_iOSXcodeSign")

1. Apple kimliği geliştirme eklediğiniz takım adını seçin **takım**.

   ![Xcode takım](../cross-platform/media/cppmdd-opengles-iosxcodeteam.png "CPPMDD_OpenGLES_iOSXcodeTeam")

### <a name="to-build-and-run-the-ios-app-on-an-ios-device"></a>Derlemek ve bir iOS cihazında iOS uygulamasını çalıştırmak için

1. Mac'inizde uzak Aracısı'nı çalıştırın ve Visual Studio için Uzak Aracı eşleştirilir doğrulayın. Uzak Aracı başlatmak için bir Terminal uygulamasını penceresi açın ve girin `vcremote`. Daha fazla bilgi için [Visual Studio'da uzak aracı yapılandırma](../cross-platform/install-and-configure-tools-to-build-using-ios.md#ConfigureVS).

   ![Vcremote çalıştıran Mac Terminal penceresi](../cross-platform/media/cppmdd_common_vcremote.png "CPPMDD_common_vcremote")

1. Mac için bir iOS cihazı bağlayın İlk kez bir bilgisayara aygıtınızı eklediğinizde, bir uyarı cihazınıza erişmek için bilgisayar güvenip güvenmediğini ister. Cihazın Mac bilgisayara güven etkinleştirin.

1. Zaten seçili değilse, Visual Studio çözüm platformdan seçin **çözüm platformları** açılır listede, cihaz işlemci üzerinde temel. Bu örnekte, bu bir **ARM64** işlemci.

   ![ARM64 için çözüm platformu kümesi](../cross-platform/media/cppmdd-opengles-pickplatformarm64.png "CPPMDD_OpenGLES_SolutionPlatARM64")

1. Çözüm Gezgini'nde MyOpenGLESApp.iOS.Application proje için kısayol menüsünü açın ve seçin **projeyi** da projeyi kaldırmak için.

1. Yeniden yüklenmemiş MyOpenGLESApp.iOS.Application proje için kısayol menüsünü açın ve seçin **project.pbxproj Düzenle** proje dosyasını düzenlemek için. İçinde `project.pbxproj` dosya, Ara `buildSettings` ekleyin ve özniteliği `DEVELOPMENT_TEAM` takım Apple kimliğinizi kullanarak Bir örnek değeri aşağıdaki ekran gösterilir `123456ABC` Apple takım kimliği Xcode'dan Apple takım kimliği değerini bulabilirsiniz. Git **Build Settings** ve geliştirme ekibi adınız bir araç ipucunu göstermek üzerine gelin. Takım kimliğinizi araç ipucunu gösterir

   ![Geliştirme ekibi ayarlamak](../cross-platform/media/cppmdd-opengles-iosdevelopmentteam.png "CPPMDD_OpenGLES_iOSDevelopmentTeam")

1. Kapat `project.pbxproj` dosya, ardından yüklenmemiş MyOpenGLESApp.iOS.Application proje için kısayol menüsünü açın ve seçin **projeyi** için projeyi yeniden yükleyin.

1. Artık proje için kısayol menüsünü açarak ve MyOpenGLESApp.iOS.Application projeyi derleyin **yapı**.

   ![İOS uygulaması projesi oluşturmak](../cross-platform/media/cppmdd_opengles_iosbuild.png "CPPMDD_OpenGLES_iOSBuild")

   Çıkış penceresi iOS statik kitaplık ve iOS uygulaması için yapı işleminin çıkış görüntüler. Mac bilgisayarlarda, uzak aracı gösterir çalıştıran Terminal penceresinde, komut ve dosya etkinlik aktarın.

   Mac bilgisayarınızda, kod imzalama, anahtar zinciri erişim izin vermek için istenebilir. Seçin **izin** devam etmek için.

1. İOS cihazınıza bağlı Mac için Cihazınızda uygulamayı çalıştırmak için araç seçin Uygulama başlatılmazsa, cihazın cihaza yürütmek dağıtılan uygulamanız için izin verdiğini doğrulayın. Bu izne giderek ayarlanabilir **ayarları** > **genel** > **cihaz Yönetimi** cihazda. Uygulama geliştirici hesabınızı seçin, hesabınızı güven ve uygulamayı doğrulayın. Uygulamayı Visual Studio'dan tekrar çalıştırmayı deneyin.

   ![iOS cihazında iOS app](../cross-platform/media/cppmdd-opengles-iosdevice.png "CPPMDD_OpenGLES_iOSDevice")
   
   Uygulama başlatıldıktan sonra kesme noktaları ayarlayın ve Visual Studio hata ayıklayıcısını Yereller inceleyin, çağrı yığını görmek ve izlemek için kullanın.

   ![İOS uygulama içinde kesme noktasında hata ayıklayıcı](../cross-platform/media/cppmdd_opengles_iosdebug.png "CPPMDD_OpenGLES_iOSDebug")

1. Tuşuna **Shift**+**F5** hata ayıklamayı durdurmak için.

   Oluşturulan bir iOS uygulaması ve kitaplık projeleri yalnızca paylaşılan kod uygulayan bir statik kitaplıkta C++ kodu yerleştirin. Çoğu uygulama kodu olan `Application` proje. Bu şablon projede paylaşılan kitaplık kodu çağrıları içinde yapılan *GameViewController.m* dosya. İOS uygulamanızı oluşturmak için Visual Studio ile bir Mac üzerinde çalışan bir uzak istemci iletişimi gerektiren Xcode platform araç takımını kullanır

   Visual Studio proje dosyalarını aktarır ve komutları Xcode kullanarak uygulamayı oluşturmak için uzak istemciye gönderir. Uzak istemci gönderir yapı durumu bilgileri Visual Studio dönün. Uygulama başarıyla oluşturdu, çalıştırın ve uygulamanın hatalarını ayıklamak için komutları göndermek için Visual Studio kullanabilirsiniz. Visual Studio hata ayıklayıcıda Mac'iniz için bağlı iOS cihazında çalışan uygulama denetimleri Visual Studio derle, bağlama ve hedef iOS platformunda hata ayıklama için kullanılan seçeneklerini StaticLibrary proje özelliklerinde eşleştirir. Derleyici komut satırı seçeneği ayrıntılarını açın **özellik sayfaları** MyOpenGLESApp.iOS.StaticLibrary proje için iletişim kutusu.

## <a name="customize-your-apps"></a>Uygulamalarınızı özelleştirin

Paylaşılan C++ koduna eklemek veya ortak işlevselliği değiştirmek için değiştirebilirsiniz. Paylaşılan kod çağrıları değiştirmeli `MyOpenGLESApp.Android.NativeActivity` ve `MyOpenGLESApp.iOS.Application` projeler ile eşleştirilecek. Önişlemci makroları, platforma özgü bölümler ortak kodunuzda belirtmek için kullanabilirsiniz. Önişlemci makrosu `__ANDROID__` Android için oluşturduğunuzda önceden tanımlanmış. Önişlemci makrosu `__APPLE__` iOS için oluşturduğunuzda önceden tanımlanmış.

Belirli proje platformu için IntelliSense görmek için bağlam değiştiricisi açılan Düzenleyicisi penceresinin üst gezinti çubuğunda projeyi seçin.

![Proje bağlamı değiştiricisi açılan kutusunda Düzenleyicisi](../cross-platform/media/cppmdd_opengles_contextswitcher.png)

Geçerli proje tarafından kullanılan bir koddaki IntelliSense sorunlarını kırmızı dalgalı çizgi ile işaretlenir. Diğer projelerde sorunları mor dalgalı çizgi ile işaretlenir. Visual Studio kod renklendirme veya IntelliSense için Java veya Objective-C dosyaları desteklemez. Ancak, yine de kaynak dosyaları değiştirebilir ve uygulama adınız, simge ve diğer uygulama ayrıntılarını ayarlamak için kaynakları değiştirin.
