---
title: C# konsol uygulamaları Visual Studio ile çalışmaya başlama
description: Visual Studio'da, adım adım C# konsol uygulaması oluşturmayı öğrenin.
ms.custom: ''
ms.date: 09/28/2018
ms.prod: visual-studio-dev15
ms.technology: vs-acquisition
ms.topic: tutorial
ms.devlang: CSharp
author: TerryGLee
ms.author: tglee
manager: douge
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: ad1ee95cb9cc754261502e7377cde6c91e5befce
ms.sourcegitcommit: ad5fb20f18b23eb8bd2568717f61edc6b7eee5e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47859516"
---
# <a name="tutorial-get-started-with-a-c-console-app-in-visual-studio"></a>Öğretici: Visual Studio'da C# konsol uygulaması ile çalışmaya başlama

Bu öğreticide C# konsol uygulaması oluşturun ve bazı özelliklerini Visual Studio kullanacaksınız [Visual Studio tümleşik geliştirme ortamı (IDE)](visual-studio-ide.md) bunu yaparken.

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir C# uygulaması projesi oluşturacağız. Proje türü bile herhangi bir şey ekledik önce ihtiyacınız olacak tüm şablon dosyaları ile birlikte gelir!

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **C#** ve ardından **.NET Core**. Orta bölmede seçin **konsol uygulaması (.NET Core)**. Dosya adı *hesaplayıcı*.

   ![Konsol uygulaması (.NET Core) proje şablonunu yeni proje iletişim kutusunda Visual Studio IDE](../ide/media/new-project-csharp-calculator-console-app.png)

### <a name="add-a-workgroup-optional"></a>(İsteğe bağlı) bir çalışma grubu Ekle

Görmüyorsanız **konsol uygulaması (.NET Core)** proje şablonu, alabilirsiniz, ekleyerek **.NET Core çoklu platform geliştirme** iş yükü. Bu iş yükü, makinenizde yüklü Visual Studio 2017 güncelleştirmeleri bağlı olarak iki aşağıdaki yollardan biriyle ekleyebilirsiniz.

#### <a name="option-1-use-the-new-project-dialog-box"></a>Seçenek 1: Yeni Proje iletişim kutusunu kullanın.

1. Seçin **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu.

   ![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantıyı seçin](../ide/media/csharp-open-visual-studio-installer-generic-dark.png)

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

   ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../ide/media/dot-net-core-xplat-dev-workload.png)

#### <a name="option-2-use-the-tools-menu-bar"></a>2. seçenek: araçlar menü çubuğunu kullanın.

1. / İptal **yeni proje** iletişim kutusu ve üst menü çubuğundan seçin **Araçları** > **araçları ve özellikleri Al**.

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

## <a name="create-a-c-console-calculator-app"></a>"C# konsol hesaplayıcı" uygulaması oluşturma

1. Visual Studio 2017'yi açın ve ardından üstteki menü çubuğundan **dosya** > **yeni** > **proje**.

1. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **C#** ve ardından **.NET Core**. Orta bölmede seçin **konsol uygulaması (.NET Core)**. Dosya adı *hesaplayıcı*.

1. Kod düzenleyicisine aşağıdaki kodu yapıştırın veya girin:

    ```csharp
    using System;

    namespace Calculator
    {
        class Program
        {
            static void Main(string[] args)
            {
                // Declare variables and then instantiate to zero
                double num1 = 0; double num2 = 0;

                // Display title as the C# console calculator app
                Console.WriteLine("Console Calculator in C#\r");
                Console.WriteLine("------------------------\n");

                // Ask the user to type the first number
                Console.WriteLine("Type a number, and then press Enter");
                num1 = Convert.ToDouble(Console.ReadLine());

                // Ask the user to type the second number
                Console.WriteLine("Type another number, and then press Enter");
                num2 = Convert.ToDouble(Console.ReadLine());

                // Ask the user to choose an option
                Console.WriteLine("Choose an option from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                // Use a switch statement to do the math
                switch (Console.ReadLine())
                {
                    case "a":
                        Console.WriteLine($"Your result: {num1} + {num2} = " + (num1 + num2));
                        break;
                    case "s":
                        Console.WriteLine($"Your result: {num1} - {num2} = " + (num1 - num2));
                        break;
                    case "m":
                        Console.WriteLine($"Your result: {num1} * {num2} = " + (num1 * num2));
                        break;
                    case "d":
                        // Ask the user to enter a non-zero divisor until they do so
                        while (num2 == 0)
                        {
                            Console.WriteLine("Enter a non-zero divisor: ");
                            num2 = Convert.ToDouble(Console.ReadLine());
                        }
                        Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                        break;
                    // Return text for an incorrect option entry
                    default:
                        Console.WriteLine("That is an incorrect option entry, please try again.");
                        break;
                }
                // Wait for the user to respond before closing
                Console.Write("Press any key to close the Calculator console app...");
                Console.ReadKey();
            }
        }
    }
    ```

   Sonra görünen kod `static void Main(string[] args)` aşağıdaki ekran görüntüsüne benzer görünmelidir:

   ![C# konsol hesaplayıcı gösteren kod Düzenleyicisi](../ide/media/csharp-console-calculator-code.png)

1. Seçin **hesaplayıcı** , programınızı çalıştırmak için veya basın **F5**.

   ![Araç çubuğunda uygulamayı çalıştırmak için hesap makinesi düğmesini seçin](../ide/media/csharp-console-calculator-button.png)

1. Uygulamanız konsol penceresinde görüntüleyin. Komut istemlerini izleyin, uygulamanızı aşağıdaki ekran görüntüsüne benzer görünmelidir:

    ![Konsol penceresi yönergeleri almak için hangi eylemleri içeren hesaplayıcı uygulama gösteriliyor.](../ide/media/csharp-console-calculator.png)

### <a name="close-the-app"></a>Uygulamayı kapatın

1. Hesaplayıcı uygulamayı kapatmak için herhangi bir tuşa basın.

1. Kapat **çıkış** Visual Studio'daki bölmesi.

   ![Visual Studio çıktı bölmesini kapatın](../ide/media/csharp-calculator-close-output-pane.png)

1. Visual Studio’yu kapatın.

## <a name="quick-answers-faq"></a>Hızlı yanıtlar hakkında SSS

İşte bazı temel kavramları vurgulamak için hızlı bir SSS.

### <a name="what-is-c"></a>C# nedir?

C# .NET Core ve .NET Framework üzerinde çalışan bir tür açısından güvenli bir programlama dilidir. C# ile Windows uygulamaları, istemci-sunucu uygulamaları, veritabanı uygulamaları, XML Web Hizmetleri, dağıtılmış bileşenler ve daha fazla oluşturabilirsiniz.

### <a name="what-is-visual-studio"></a>Visual Studio nedir?

Visual Studio geliştiricileri için üretkenlik aracından oluşan bir tümleşik geliştirme paketidir. Bunu, programları ve uygulamaları oluşturmak için kullanabileceğiniz bir program olarak düşünün.

### <a name="what-is-a-console-app"></a>Bir konsol uygulaması nedir?

Bir konsol uygulaması girdi alır ve çıktı olarak da bilinir bir komut satırı penceresinde görüntüler bir konsol.

### <a name="what-is-net-core"></a>.NET Core nedir?

.NET core .NET Framework'ün gelişime sonraki adımdır. Burada .NET Framework programlama dilleri arasında kod paylaşma izin .NET Core platformlar arasında kod paylaşma olanağı ekler. Daha da iyi açık kaynak olan.

(.NET Framework ve .NET Core önceden oluşturulmuş işlev kitaplıkları içerir. Ayrıca, kodunuzu çalıştırmak için bir sanal makine olarak davranan bir ortak dil çalışma zamanı (CLR) içerirler.)

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticiyi tamamlamak Tebrikler! Daha da fazla bilgi edinmek için şu öğretici ile devam edin.

> [!div class="nextstepaction"]
> [C# Eğitmenleri](/dotnet/csharp/tutorials/)

## <a name="see-also"></a>Ayrıca bkz.

* [Video dersi yeni başlayanlar için C# temel](https://mva.microsoft.com/en-us/training-courses/c-fundamentals-for-absolute-beginners-16169)
