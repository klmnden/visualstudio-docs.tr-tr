---
title: 'Öğretici: Hata ayıklama C# ve C++ kodu (karışık mod)'
description: Yerel bir DLL karışık mod hata ayıklaması'nı kullanarak bir .NET Core veya .NET Framework uygulamasında hata ayıklama hakkında bilgi edinin
ms.custom: seodec18
ms.date: 11/02/2018
ms.topic: tutorial
dev_langs:
- CSharp
- C++
helpviewer_keywords:
- mixed mode debugging
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
- cplusplus
ms.openlocfilehash: 3dfdc230a4dc873cc9a068e2f641da022018aff3
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65679390"
---
# <a name="tutorial-debug-c-and-c-in-the-same-debugging-session"></a>Öğretici: Hata ayıklama C# ve aynı C++ hata ayıklama oturumu

Visual Studio, birden fazla hata ayıklayıcı türü karışık mod hata ayıklama çağrılan hata ayıklama oturumunda, etkinleştirmenize olanak tanır. Bu öğreticide, tek bir hata ayıklama oturumunda hem yönetilen hem de yerel kod hatalarını ayıklamak öğrenin.

Bu öğreticide, yönetilen yerel kod hatalarını ayıklamak gösterilir, ancak ayrıca [yönetilen koddan yerel bir uygulama hata ayıklama](../debugger/how-to-debug-in-mixed-mode.md). Hata ayıklayıcı ayrıca diğer tür karışık mod hata ayıklama gibi hata ayıklamayı destekler [Python ve yerel kod](../python/debugging-mixed-mode-c-cpp-python-in-visual-studio.md)ve ASP.NET gibi uygulama türlerinde betik hata ayıklayıcıyı kullanma.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Basit bir yerel DLL oluşturma
> * DLL çağırmak için basit bir .NET Core veya .NET Framework uygulaması oluşturma
> * Karışık mod hata ayıklama yapılandırma
> * Hata ayıklayıcıyı başlatın
> * Yönetilen bir uygulama içinde bir kesme noktasına isabet
> * Yerel kod içine adımla

## <a name="prerequisites"></a>Önkoşullar

Visual Studio, aşağıdaki iş yükleri ile yüklü olması gerekir:
- **C++ ile masaüstü geliştirme**
- Her iki **.NET masaüstü geliştirme** veya **.NET Core çoklu platform geliştirme**oluşturmak istediğiniz uygulama türünü bağlı olarak.

Visual Studio sahip değilseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/) ücretsiz yüklemek için sayfa.

Visual Studio yüklü, ancak seçtiğiniz iş yüklerine sahip değilseniz **açık Visual Studio yükleyicisi** Visual Studio'nun sol bölmede **yeni proje** iletişim kutusu. Visual Studio yükleyicisinde gerekir ve ardından iş yükleri seçin **Değiştir**.

## <a name="create-a-simple-native-dll"></a>Basit bir yerel DLL oluşturma

**DLL proje dosyalarını oluşturmak için:**

1. Visual Studio'yu açın ve bir proje oluşturun.

    ::: moniker range=">=vs-2019"
    Tuşuna **Esc** başlangıç penceresini kapatın. Tür **Ctrl + Q** arama kutusunu açmak için şunu yazın **boş proje**, seçin **şablonları**, ardından **yeni boş proje proje oluştur** c ++. Görünen iletişim kutusunda **Oluştur**. Gibi bir ad yazın **Mixed_Mode_Debugging** tıklatıp **Oluştur**.
    ::: moniker-end
    ::: moniker range="vs-2017"
    Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**. Sol bölmesinde **yeni proje** iletişim kutusunun **Visual C++**, seçin **diğer**seçip Ortadaki bölmeden **boş proje**. Gibi bir ad yazın **Mixed_Mode_Debugging** tıklatıp **Tamam**.
    ::: moniker-end

    Görmüyorsanız **boş proje** proje şablonu, Git **Araçları** > **araçları ve özellikleri Al...** , Visual Studio yükleyicisi açılır. Visual Studio Yükleyicisi'ni başlatır. Seçin **C++ ile masaüstü geliştirme** iş yükü, ardından **Değiştir**.

    Visual Studio projesi oluşturur.

1. İçinde **yeni proje** iletişim kutusunun **Visual C++** seçin **diğer**ve ardından **boş proje** orta bölmesinde.

1. İçinde **adı** alanına **Mixed_Mode_Debugging**ve ardından **Tamam**.

   Visual Studio, boş bir proje oluşturur ve görüntüler **Çözüm Gezgini**.

1. İçinde **Çözüm Gezgini**seçin **kaynak dosyaları**ve ardından **proje** > **Yeni Öğe Ekle**. Ya da sağ **kaynak dosyaları** seçip **Ekle** > **yeni öğe**.

1. İçinde **yeni öğe** iletişim kutusunda **C++ dosyası (.cpp)**. Tür **Mixed_Mode.cpp** içinde **adı** alan ve ardından **Ekle**.

    Visual Studio için yeni C++ dosyası ekler **Çözüm Gezgini**.

1. Aşağıdaki kodu kopyalayın *Mixed_Mode.cpp*:

    ```cpp
    #include "Mixed_Mode.h"
    ```

1. İçinde **Çözüm Gezgini**seçin **üst bilgi dosyaları**ve ardından **proje** > **Yeni Öğe Ekle**. Ya da sağ **üst bilgi dosyaları** seçip **Ekle** > **yeni öğe**.

1. İçinde **yeni öğe** iletişim kutusunda **üst bilgi dosyası (.h)**. Tür **Mixed_Mode.h** içinde **adı** alan ve ardından **Ekle**.

   Visual Studio yeni üstbilgi dosyasına ekler **Çözüm Gezgini**.

1. Aşağıdaki kodu kopyalayın *Mixed_Mode.h*:

    ```cpp
    #ifndef MIXED_MODE_MULTIPLY_HPP
    #define MIXED_MODE_MULTIPLY_HPP

    extern "C"
    {
      __declspec(dllexport) int __stdcall mixed_mode_multiply(int a, int b) {
        return a * b;
      }
    }
    #endif
    ```

1. Seçin **dosya** > **Tümünü Kaydet** veya basın **Ctrl**+**Shift**+**S**  dosyaları kaydetmek için.

**DLL projesi oluşturmak ve yapılandırmak için:**

1. Visual Studio araç çubuğunda, seçin **hata ayıklama** yapılandırma ve **x86** veya **x64** platform. Arama uygulamanız her zaman 64 bit modunda çalıştırır, .NET Core olacaksa seçin **x64** platformu olarak.

1. İçinde **Çözüm Gezgini**seçin **Mixed_Mode_Debugging** proje düğümünü seçip alt **özellikleri** simgesini veya proje düğümünü sağ tıklayıp **Özellikleri**.

1. Üst kısmındaki **özellikleri** bölmesinde emin olun **yapılandırma** ayarlanır **Active(Debug)** ve **Platform** ne aynıdır araç çubuğunda ayarlayın: **x64**, veya **Win32** x86 için platform.

   > [!IMPORTANT]
   > Bir platformdan diğerine geçtiğinizde **x86** için **x64** veya bunun tersini yapmak, yeni platform özelliklerini yapılandırın.

1. Altında **yapılandırma özellikleri** seçin sol bölmede **bağlayıcı** > **Gelişmiş**ve yanındaki açılan menüdeki **Hayır giriş noktası**seçin **Hayır**. Değiştirilmesi olsaydı **Hayır**seçin **Uygula**.

1. Altında **yapılandırma özellikleri**seçin **genel**ve yanındaki açılan menüdeki **yapılandırma türü**seçin **dinamik kitaplık (.dll)**. Seçin **Uygula**ve ardından **Tamam**.

   ![Yerel bir DLL için geçiş](../debugger/media/mixed-mode-set-as-native-dll.png)

1. Projede seçin **Çözüm Gezgini** seçip **derleme** > **Çözümü Derle**, basın **F7**, ya da sağ tıklayın seçin ve proje **yapı**.

   Projenin hatasız oluşturması gerekir.

## <a name="create-a-simple-managed-app-to-call-the-dll"></a>DLL çağırmak için basit bir yönetilen uygulama oluşturma

1. Visual Studio'yu açın ve yeni bir proje oluşturun.

    ::: moniker range=">=vs-2019"
    Tuşuna **Esc** başlangıç penceresini kapatın. Tür **Ctrl + Q** arama kutusunu açmak için şunu yazın **konsol**, seçin **şablonları**ve ardından **oluştur yeni konsol uygulaması (.NET Framework) projesi** için C#. Görünen iletişim kutusunda **Oluştur**.

    Gibi bir ad yazın **Mixed_Mode_Calling_App** tıklatıp **Oluştur**.
    ::: moniker-end
    ::: moniker range="vs-2017"
    Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**. Sol bölmesinde **yeni proje** iletişim kutusunun **Visual C#** , seçin **Windows Masaüstü**seçip Ortadaki bölmeden **konsol uygulaması (. NET Framework)** veya **konsol uygulaması (.NET Core)**.

    Gibi bir ad yazın **Mixed_Mode_Calling_App** tıklatıp **Tamam**.
    ::: moniker-end

    Görmüyorsanız **konsol uygulaması** proje şablonu, Git **Araçları** > **araçları ve özellikleri Al...** , Visual Studio yükleyicisi açılır. Seçin **.NET masaüstü geliştirme** iş yükü, ardından **Değiştir**.

    > [!NOTE]
    > Var olan C++ çözümünüze yeni yönetilen proje de ekleyebilirsiniz, ancak yeni çözüm oluşturmaya daha fazla hata ayıklama senaryoları destekler.

   Visual Studio, boş bir proje oluşturur ve görüntüler **Çözüm Gezgini**.

1. Tüm kodu değiştirin *Program.cs* aşağıdaki kod ile:

    ```csharp
    using System;
    using System.Runtime.InteropServices;

    namespace Mixed_Mode_Calling_App
    {
        public class Program
        {
            // Replace the file path shown here with the
            // file path on your computer. For .NET Core, the typical (default) path
            // for a 64-bit DLL might look like this:
            // C:\Users\username\source\repos\Mixed_Mode_Debugging\x64\Debug\Mixed_Mode_Debugging.dll
            // Here, we show a typical path for a DLL targeting the **x86** option.
            [DllImport(@"C:\Users\username\source\repos\Mixed_Mode_Debugging\Debug\Mixed_Mode_Debugging.dll", EntryPoint =
            "mixed_mode_multiply", CallingConvention = CallingConvention.StdCall)]
            public static extern int Multiply(int x, int y);
            public static void Main(string[] args)
            {
                int result = Multiply(7, 7);
                Console.WriteLine("The answer is {0}", result);
                Console.ReadKey();
            }
        }
    }
    ```

1. Dosya yolunda yeni kodu değiştirin `[DllImport]` dosya yolunuzla *Mixed_Mode_Debugging.dll* oluşturdunuz. Kod açıklaması ipuçları için bkz. Değiştirdiğinizden emin olun *kullanıcıadı* yer tutucu.

1. Seçin **dosya** > **Kaydet Program.cs** veya basın **Ctrl**+**S** dosyayı kaydetmek için.

## <a name="configure-mixed-mode-debugging"></a>Karışık mod hata ayıklama yapılandırma

### <a name="to-configure-mixed-mode-debugging-for-a-net-framework-app"></a>Karışık mod hata ayıklama için .NET Framework uygulamasını yapılandırmak için

1. İçinde **Çözüm Gezgini**seçin **Mixed_Mode_Calling_App** proje düğümünü seçip alt **özellikleri** simgesini veya proje düğümünü sağ tıklayıp **Özellikleri**.

1. Seçin **hata ayıklama** seçin sol bölmede **yerel kod hata ayıklamayı** onay kutusunu işaretleyin ve ardından değişiklikleri kaydetmek için Özellikler sayfasını kapatın.

    ![Karışık modda hata ayıklama etkinleştirme](../debugger/media/mixed-mode-enable-native-code-debugging.png)

### <a name="to-configure-mixed-mode-debugging-for-a-net-core-app"></a>Karışık mod hata ayıklama için .NET Core uygulamasını yapılandırmak için

Çoğu Visual Studio 2017'den itibaren Visual Studio sürümlerinde kullanmalısınız *launchSettings.json* dosya yerine bir .NET Core uygulaması yerel kod için karışık mod hata ayıklamayı etkinleştirmek için proje özellikleri. Bu özellik için kullanıcı Arabirimi güncelleştirmeleri izlemek için bkz [GitHub sorunu](https://github.com/dotnet/project-system/issues/1125).

1. İçinde **Çözüm Gezgini**, genişletme **özellikleri**açın *launchSettings.json* dosya.

   >[!NOTE]
   >Varsayılan olarak, *launchSettings.json* bulunduğu *C:\Users\username\source\repos\Mixed_Mode_Calling_App\Properties*. Varsa *launchSettings.json* değil, mevcut seçin **Mixed_Mode_Calling_App** projesi **Çözüm Gezgini** seçip **özellikleri** simgesini veya projeye sağ tıklayıp seçin **özellikleri**. Geçici bir değişiklik yapmak **hata ayıklama** sekme ve projeyi derleyin. Bu oluşturacak bir *launchSettings.json* dosya. Yaptığınız değişikliği geri al **hata ayıklama** sekmesi.

1. İçinde *lauchsettings.json* dosyasında, aşağıdaki satırı ekleyin:

    ```csharp
    "nativeDebugging": true
    ```

    Tam dosya aşağıdaki örnekteki gibi görünür:

    ```csharp
    {
      "profiles": {
        "Mixed_Mode_Calling_App": {
          "commandName": "Project",
          "nativeDebugging": true
        }
      }
    }
    ```

## <a name="set-a-breakpoint-and-start-debugging"></a>Bir kesme noktası ayarlayın ve hata ayıklamayı Başlat

1. İçinde C# projesini açarsanız *Program.cs*. En sol kenar boşluğunu tıklatarak, çizgiyi seçerek ve tuşuna basarak kod satırında bir kesme noktası ayarlamak **F9**, veya satırın sağ tıklayıp **kesme noktası**  >  **Kesme noktası Ekle**.

    ```csharp
    int result = Multiply(7, 7);
    ```

    Kırmızı bir daire Kesme noktasının ayarlandığı sol kenar boşluğunda görünür.

1. Tuşuna **F5**, Visual Studio araç çubuğunda yeşil ok seçin ya da seçin **hata ayıklama** > **hata ayıklamayı Başlat** hata ayıklama başlatılamıyor.

   Hata ayıklayıcı, ayarladığınız kesme noktasına duraklatır. Sarı bir ok, hata ayıklayıcı şu anda duraklatılmış burada gösterir.

## <a name="step-in-and-out-of-native-code"></a>Yerel kod, içeri ve dışarı adım

1. Yönetilen bir uygulamada hata ayıklama durdurulduğunda, basın **F11**, ya da seçin **hata ayıklama** > **içine adımla**.

   *Mixed_Mode.h* yerel üstbilgi dosyası açılır ve burada hata ayıklayıcı duraklatıldı sarı ok görürsünüz.

   ![Yerel kod içine adımla](../debugger/media/mixed-mode-step-into-native-code.png)

1. Şimdi, ayarlayabilir ve kesme noktaları isabet ve yerel veya yönetilen kodda değişkenleri denetleyin.

   - Değerleri görmek için kaynak kodundaki değişkenleri üzerine gelin.

   - Değişkeni ve değerlerini bakın **Otolar** ve **Yereller** windows.

   - Hata ayıklayıcısında duraklatıldıktan olsa da kullanabilirsiniz **Watch** windows ve **çağrı yığını** penceresi.

1. Tuşuna **F11** yeniden hata ayıklayıcı bir satırın ilerlemek için.

1. Tuşuna **Shift**+**F11** ya da seçin **hata ayıklama** > **Step Out** yürütme devam etmek ve yeniden Duraklat yönetilen uygulama.

1. Tuşuna **F5** veya uygulamada hata ayıklamaya devam etmek için yeşil oku seçin.

Tebrikler! Karışık mod hata ayıklama şirket öğreticisini tamamladınız.

## <a name="next-step"></a>Sonraki adım

Bu öğreticide, karma mod hata ayıklama etkinleştirerek yönetilen yerel kod hata ayıklama öğrendiniz. Diğer hata ayıklayıcı özelliklerine genel bakış için bkz:

> [!div class="nextstepaction"]
> [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
