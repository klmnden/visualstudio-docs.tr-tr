---
title: 'Öğretici: yönetilen ve yerel kod (karışık mod) hata ayıklama'
description: Yerel bir DLL karışık modda hata ayıklama kullanarak bir .NET Core veya .NET Framework uygulamasında hata ayıklama hakkında bilgi edinin
ms.custom: ''
ms.date: 10/24/2018
ms.technology: vs-ide-debug
ms.topic: tutorial
dev_langs:
- CSharp
- C++
helpviewer_keywords:
- mixed mode debugging
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
- cplusplus
ms.openlocfilehash: 97ad3b6e112a05db817f7a522c3865893d439fd7
ms.sourcegitcommit: 12d6398c02e818de4fbcb4371bae9e5db6cf9509
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50050332"
---
# <a name="tutorial-debug-managed-and-native-code-in-the-same-debugging-session"></a>Öğretici: aynı hata ayıklama oturumunda yönetilen ve yerel kod hatalarını ayıklama

Visual Studio karışık modda hata ayıklama çağrılan hata ayıklarken birden fazla hata ayıklayıcı türü olanak sağlar. Bu öğreticide, tek bir hata ayıklama oturumunda hem yönetilen hem de yerel kod hatalarını ayıklamak için seçenekleri ayarlayın. Bu öğreticide, yönetilen yerel kod hatalarını ayıklamak gösterilir, ancak bunun tersi de yapabilirsiniz ve [yönetilen koddan yerel bir uygulama hata ayıklama](../debugger/how-to-debug-in-mixed-mode.md). Hata ayıklayıcı ayrıca diğer tür karışık modda hata ayıklama gibi hata ayıklamayı destekler [Python ve yerel kod](../python/debugging-mixed-mode-c-cpp-python-in-visual-studio.md) ve ASP.NET gibi uygulama türlerinde betik hata ayıklayıcıyı kullanma.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Basit bir yerel DLL oluşturma
> * DLL çağırmak için basit bir .NET Core veya .NET Framework uygulaması oluşturma
> * Hata ayıklayıcıyı başlatın
> * Yönetilen bir uygulama içinde bir kesme noktasına isabet
> * Yerel kod içine adımla

## <a name="prerequisites"></a>Önkoşullar

* Visual Studio yüklü olmalıdır ve **C++ ile masaüstü geliştirme** iş yükü.

    Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

    İş yükünü yükleyin, ancak Visual Studio'a tıklayın, zaten gerektiğinde **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu. Visual Studio Yükleyicisi'ni başlatır. Seçin **C++ ile masaüstü geliştirme** iş yükü, ardından **Değiştir**.

* Ya da sahip olmalısınız **.NET masaüstü geliştirme** iş yükü veya **.NET Core çoklu platform geliştirme** iş yükü yüklenmiş, oluşturmak istediğiniz hangi uygulama türü üzerinde bağlı olarak.

## <a name="create-a-simple-native-dll"></a>Basit bir yerel DLL oluşturma

1. Visual Studio'da **dosya** > **yeni** > **proje**.

1. İçinde **yeni proje** iletişim kutusunda **Visual C++**, **diğer** Yüklü Şablonlar bölümünden ve Orta bölmede seçin **boş proje** .

1. İçinde **adı** alanına **Mixed_Mode_Debugging** tıklatıp **Tamam**.

    Visual Studio Çözüm Gezgini'nde sağ bölmede görünür boş bir proje oluşturur.

1. Çözüm Gezgini'nde sağ **kaynak dosyaları** düğüm c++ proje ve ardından **Ekle** > **yeni öğe**ve ardından **C++ dosyası (.cpp)**. Dosya adını verin **Mixed_Mode.cpp**ve **Ekle**.

    Visual Studio, yeni C++ dosyası ekler.

1. Aşağıdaki kodu kopyalayın *Mixed_Mode.cpp*:

    ```cpp
    #include "Mixed_Mode.h"
    ```
1. Çözüm Gezgini'nde sağ **üst bilgi dosyaları** düğüm c++ proje ve ardından **Ekle** > **yeni öğe**ve ardından  **Üst bilgi dosyası (.h)**. Dosya adını verin **Mixed_Mode.h**ve **Ekle**.

    Visual Studio yeni üst bilgi dosyası ekler.

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

1. Hata ayıklama araç çubuğundan seçin bir **hata ayıklama** yapılandırma ve **x86** veya **x64** platformu olarak (her zaman 64 bit modunda çalıştırır, .NET Core için seçin **x64**  platformu olarak).

1. Çözüm Gezgini'nde proje düğümüne sağ tıklayın (**Mixed_Mode_Debugging**) seçip **özellikleri**.

    > [!IMPORTANT]
    > Özellik için C++ platformlar başına yapılandırmadır. Bu nedenle, diğer (x86 için x64 veya bunun tersini de) birinden geçerseniz, yeni yapılandırma özelliklerini de ayarlamanız gerekir. (Ya da Özellikler sayfasında doğrulayın **x64** veya **Win32** sayfanın en üstündeki platformu olarak ayarlanır.)

1. İçinde **özellikleri** sayfasında **yapılandırma özellikleri** > **bağlayıcı** > **Gelişmiş**, ve ardından **Hayır giriş noktası** aşağı açılan listesinde, emin olun **Hayır** seçilir. Ayarı değiştirmeniz gerekirse **Hayır**, ardından **Uygula**.

1. İçinde **özellikleri** sayfasında **yapılandırma özellikleri** > **genel**ve ardından **dinamik kitaplık (.dll)** gelen **yapılandırma türü** alan. Ardından ayarları uygulayın.

    ![Yerel bir DLL için geçiş](../debugger/media/mixed-mode-set-as-native-dll.png)

1. Projeye sağ tıklayıp seçin **yapı**.

    Projenin hatasız oluşturması gerekir.

## <a name="create-a-simple-net-framework-or-net-core-app-to-call-the-dll"></a>DLL çağırmak için basit bir .NET Framework veya .NET Core uygulaması oluşturma

1. Visual Studio'da **dosya** > **yeni** > **proje**.

    > [!NOTE]
    > Çözüme yeni bir çözüm oluşturmak yerine C++ projesi ile yeni yönetilen proje de ekleyebilirsiniz, ancak biz, burada daha büyük bir hata ayıklama senaryoları desteklemek için yapıyor değil.

1. Uygulama kodunuz için bir şablon seçin.

    .NET Framework içinde **yeni proje** iletişim kutusunda **Visual C#**, **Windows Masaüstü** Yüklü Şablonlar bölümünden ve Ortabölmedeseçin **Konsol uygulaması (.NET Framework)**.

    .NET Core için de **yeni proje** iletişim kutusunda **Visual C#**, **.NET Core** Yüklü Şablonlar bölümünden ve Orta bölmede seçin  **Konsol uygulaması (.NET Core)**.

1. İçinde **adı** alanına **Mixed_Mode_Calling_App** tıklatıp **Tamam**.

    Visual Studio Çözüm Gezgini'nde sağ bölmede görünür konsol projesi oluşturur.

1. İçinde *Program.cs*, varsayılan kodu aşağıdaki kodla değiştirin:

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

1. Yeni kod içinde dosya yolu yolunu (açıklamalarına bakın), daha önce oluşturduğunuz DLL için güncelleştirin. Değiştirdiğiniz emin *kullanıcıadı* yer tutucu.

## <a name="configure-mixed-mode-debugging-net-framework"></a>Karışık mod hata ayıklaması (.NET Framework) yapılandırma

1. Yönetilen Çözüm Gezgini'nde sağ **Mixed_Mode_Calling_App** projesini ve ardından **başlangıç projesi olarak ayarla**.

1. Yönetilen sağ **Mixed_Mode_Calling_App** proje ve ardından **özellikleri**ve ardından **hata ayıklama** sol bölmesinde. Seçin **yerel kod hata ayıklamayı**ve ardından değişiklikleri kaydetmek için Özellikler sayfasını kapatın.

    ![Karışık modda hata ayıklama etkinleştirme](../debugger/media/mixed-mode-enable-native-code-debugging.png)

## <a name="configure-mixed-mode-debugging-net-core"></a>Karışık mod hata ayıklaması (.NET Core) yapılandırma

Çoğu Visual Studio 2017 sürümünde .NET Core kullanarak uygulamayı yerel kod için karışık modda hata ayıklama etkinleştirmelisiniz *launchSettings.json* yerine dosya **özellikleri** sayfası. Bu özellik için kullanıcı Arabirimi güncelleştirmeleri izlemek için bkz [GitHub sorunu](https://github.com/dotnet/project-system/issues/1125).

1. Açık *launchSettings.json* dosyası *özellikleri* klasör. Varsayılan olarak, dosyanın bu konumda bulabilirsiniz.

    *C:\Users\<kullanıcıadı > \source\repos\Mixed_Mode_Calling_App\Properties*

    Dosya mevcut değilse, proje özelliklerini açın (sağ tıklayın yönetilen **Mixed_Mode_Calling_App** seçin ve Çözüm Gezgini'nde proje **özellikleri**). Geçici bir değişiklik yapmak **hata ayıklama** sekmesini ve projenizi derleyin. Yaptığınız değişikliği geri alın.

1. İçinde *lauchsettings.json* dosyasında, aşağıdaki özelliği ekleyin:

    ```csharp
    "nativeDebugging": true
    ```

    Bu nedenle, örneğin, dosyanız aşağıdaki gibi görünebilir:

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

## <a name="set-a-breakpoint-and-start-the-debugger"></a>Bir kesme noktası ayarlayın ve hata ayıklayıcıyı başlatın

1. İçinde C# projesini açarsanız *Program.cs* sol kenar boşluğunu tıklayarak aşağıdaki kod satırında bir kesme noktası ayarlayın:

    ```csharp
    int result = Multiply(7, 7);
    ```

    Kırmızı bir daire kesme noktasını ayarlamanız göstermek için sol kenar boşluğunda görünür.

1. Tuşuna **F5** (**hata ayıklama** > **hata ayıklamayı Başlat**) hata ayıklayıcıyı başlatmak için.

    Hata ayıklayıcı, ayarladığınız kesme noktasına duraklatır. Sarı bir ok, hata ayıklayıcı şu anda duraklatılmış burada gösterir.

## <a name="step-into-native-code"></a>Yerel kod içine adımla

1. Yönetilen uygulama duraklatıldığı sırada basın **F11** (**hata ayıklama** > **içine adımla**).

    Yerel kod ile üst bilgi dosyası açılır ve burada hata ayıklayıcı duraklatıldı sarı ok görürsünüz.

    ![Yerel kod içine adımla](../debugger/media/mixed-mode-step-into-native-code.png)

    Artık, ayarlama yapma ve kesme noktaları isabet ve değişkenleri denetleyin.

1. Değerleri görmek için değişkenlerin gelin.

1. Bakmak **Otolar** ve **Yereller** değişkeni ve bunların değerlerini görmek için windows.

    Hata ayıklayıcısında duraklatıldıktan olsa da diğer hata ayıklayıcı özellikleri gibi kullanabilir **Watch** penceresi ve **çağrı yığını** penceresi.

1. Tuşuna **F11** yeniden hata ayıklayıcı bir satırın ilerlemek için.

1. Tuşuna **Shift + F11** (**hata ayıklama** > **Step Out**) uygulama yürütmeye devam et ve tekrar yönetilen uygulamayı duraklatmak için.

1. Tuşuna **F5** uygulamaya devam etmek için.

    Tebrikler! Karışık modda hata ayıklama şirket öğreticisini tamamladınız.

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, karışık modda hata ayıklama etkinleştirerek yönetilen yerel kod hata ayıklama öğrendiniz. Diğer hata ayıklayıcı özelliklerine genel bakış için şu makaleye bakın:

> [!div class="nextstepaction"]
> [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
