---
title: 'Öğretici: Basit bir C# konsol uygulaması'
description: Visual Studio'da, adım adım C# konsol uygulaması oluşturmayı öğrenin.
ms.custom: seodec18, get-started
ms.date: 03/12/2019
ms.technology: vs-ide-general
ms.topic: tutorial
ms.devlang: CSharp
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: c73212ad53389b71ee2eb2a2660cd3dcbccaad8b
ms.sourcegitcommit: 2dc924c96a6d48803c8eedc3d6781202629b41fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57736918"
---
# <a name="tutorial-create-a-simple-c-console-app-in-visual-studio"></a>Öğretici: Basit bir C# Visual Studio'da konsol uygulaması

Bu öğreticide için C#, bir konsol uygulaması oluşturun ve bunu yaparken bazı Visual Studio tümleşik geliştirme ortamı (IDE) özelliklerini Visual Studio kullanacaksınız.

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

## <a name="create-a-project"></a>Proje oluşturma

Başlamak için oluşturacağız bir C# uygulama projesi. Proje türü bile herhangi bir şey ekledik önce ihtiyacınız olacak tüm şablon dosyaları ile birlikte gelir!

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.
   (Alternatif olarak, basın **Ctrl**+**Shift**+**N**).

3. Sol bölmesinde **yeni proje** iletişim kutusunda **C#** ve ardından **.NET Core**. Orta bölmede seçin **konsol uygulaması (.NET Core)**. Dosya adı ***hesaplayıcı***.

   ![Konsol uygulaması (.NET Core) proje şablonunu yeni proje iletişim kutusunda Visual Studio IDE](./media/new-project-csharp-calculator-console-app.png)

### <a name="add-a-workload-optional"></a>(İsteğe bağlı) bir iş yükü Ekle

Görmüyorsanız **konsol uygulaması (.NET Core)** proje şablonu, alabilirsiniz, ekleyerek **.NET Core çoklu platform geliştirme** iş yükü. İşte nasıl.

#### <a name="option-1-use-the-new-project-dialog-box"></a>1. seçenek: Yeni Proje iletişim kutusunu kullanın

1. Seçin **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu.

   ![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantıyı seçin](./media/csharp-open-visual-studio-installer-generic-dark.png)

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

   ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](./media/dot-net-core-xplat-dev-workload.png)

#### <a name="option-2-use-the-tools-menu-bar"></a>2. seçenek: Araçlar menü çubuğunu kullanın

1. / İptal **yeni proje** iletişim kutusu ve üst menü çubuğundan seçin **Araçları** > **araçları ve özellikleri Al**.

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

## <a name="create-the-app"></a>Uygulama oluşturma

İlk olarak, bazı temel tamsayı matematik şunları keşfedeceğiz C#. Ardından, temel hesaplayıcı oluşturmak için kod ekleyeceğiz. Yanında. Bundan sonra uygulamayı bulun ve hataları düzeltmek için hata ayıklama. Ve son olarak, size daha verimli hale getirmek için kod geliştireceksiniz.

### <a name="explore-integer-math"></a>Tamsayı matematiğini İnceleme

İle bazı temel tamsayı matematik başlayalım C#.

1. Kod Düzenleyicisi'nde, varsayılan "Hello World" kod silin.

    ![Yeni hesaplayıcı uygulamanızdan varsayılan Merhaba Dünya kodu Sil](./media/csharp-console-calculator-deletehelloworld.png)

   Özellikle, yazan satırı silin `Console.WriteLine("Hello World!");`.

1. Bunun yerine, aşağıdaki kodu yazın:

    ```csharp
            int a = 42;
            int b = 119;
            int c = a + b;
            Console.WriteLine(c);
            Console.ReadKey();
    ```

    Bunu yaptığınızda, Visual Studio IntelliSense özelliği, otomatik tamamlama girişi seçeneği sunduğunu dikkat edin.

    ![Visual Studio IDE IntelliSense otomatik tamamlama özelliği gösteren tamsayı matematik kod animasyon](./media/integer-math-intellisense.gif)

1. Seçin **hesaplayıcı** , programınızı çalıştırmak için veya basın **F5**.

   ![Araç çubuğunda uygulamayı çalıştırmak için hesap makinesi düğmesini seçin](./media/csharp-console-calculator-button.png)

   Olan 42 + 119 toplamını gösteren bir konsol penceresi açılır **161**.

    ![Tamsayı matematiğini sonuçlarını gösteren konsol penceresi](./media/csharp-console-integer-math.png)

1. **(İsteğe bağlı)**  Sonucu değiştirmek için işleci değiştirebilirsiniz. Örneğin, değiştirebileceğiniz `+` işlecinde `int c = a + b;` kod satırını `-` çıkarma için `*` çarpma için veya `/` bölümünün. Programını çalıştırdığınızda, ardından sonucu, çok değiştirir.

1. Konsol penceresini kapatın.

### <a name="add-code-to-create-a-calculator"></a>Bir hesap makinesi oluşturmak için kod ekleyin

Hesaplayıcı kod daha karmaşık bir takım projenize ekleyerek devam edelim.

1. Kod düzenleyicisinde gördüğünüz kodu silin.

1. Aşağıdaki yeni kodu kod düzenleyicisine yapıştırın veya girin:

    ```csharp
    using System;

    namespace Calculator
    {
        class Program
        {
            static void Main(string[] args)
            {
                // Declare variables and then initialize to zero
                int num1 = 0; int num2 = 0;

                // Display title as the C# console calculator app
                Console.WriteLine("Console Calculator in C#\r");
                Console.WriteLine("------------------------\n");

                // Ask the user to type the first number
                Console.WriteLine("Type a number, and then press Enter");
                num1 = Convert.ToInt32(Console.ReadLine());

                // Ask the user to type the second number
                Console.WriteLine("Type another number, and then press Enter");
                num2 = Convert.ToInt32(Console.ReadLine());

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
                        Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                        break;
                }
                // Wait for the user to respond before closing
                Console.Write("Press any key to close the Calculator console app...");
                Console.ReadKey();
            }
        }
    }
    ```

1. Seçin **hesaplayıcı** , programınızı çalıştırmak için veya basın **F5**.

   ![Araç çubuğunda uygulamayı çalıştırmak için hesap makinesi düğmesini seçin](./media/csharp-console-calculator-button.png)

   Bir konsol penceresi açılır.

1. Konsol penceresinde uygulamanızı görüntülemek ve sayıları için istemleri izleyin **42** ve **119**.

   Uygulamanız aşağıdaki ekran görüntüsüne benzer görünmelidir:

    ![Konsol penceresinde hesaplayıcı uygulamayı gösteren ve gerçekleştirilecek eylemleri istemlerinde içerir](./media/csharp-console-calculator.png)

### <a name="add-functionality-to-the-calculator"></a>Hesaplayıcıya işlevsellik ekleme

Şimdi daha fazla işlevsellik eklemek için kod ince ayar.

### <a name="add-decimals"></a>Ondalık sayı Ekle

Hesaplayıcı uygulama şu anda kabul eder ve tam sayı döndürür. Ancak biz ondalık basamak veren kod eklerseniz daha kesin olacaktır.

Uygulamayı çalıştırın ve sayı 42 119, sayıya göre bölme aşağıdaki ekran görüntüsünde gösterildiği gibi sonuç 0 (sıfır), tam değil ise.

![Bir ondalık döndürmüyor hesaplayıcı uygulama sonucunda sayısal gösteren konsol penceresi](./media/csharp-console-calculator-nodecimal.png)

Şimdi ondalık işler, böylece kodu düzeltin.

1. Tuşuna **Ctrl** + **F** açmak için **Bul ve Değiştir** denetimi.

1. Her örneğini `int` değişkenini `float`.

   Geçiş emin **eşleşen servis talebi** (**Alt**+**C**) ve **eşleşen tam sözcük** (**Alt** + **W**) içinde **Bul ve Değiştir** denetimi.

    ![Animasyon kayan nokta tamsayı değişkeni değiştirme gösteren Bul ve Değiştir denetimi](./media/find-replace-control-animation.gif)

1. Hesaplayıcı uygulamanızı tekrar çalıştırın ve sayı bölmek **42** numarasıyla **119**.

   Uygulama artık ondalık bir sayı sıfır yerine döndürdüğüne dikkat edin.

    ![Artık bir ondalık sayı döndüren hesaplayıcı uygulama sonucunda sayısal gösteren konsol penceresi](./media/csharp-console-calculator-decimal.png)

Bununla birlikte, uygulamayı yalnızca ondalık bir sonuç üretir. Uygulama çok ondalık basamak hesaplayabilmeniz birkaç daha fazla tweaks koda olalım.

1. Kullanım **Bul ve Değiştir** denetimi (**Ctrl** + **F**) her bir örneğini değiştirmek için `float` değişkenini `double`ve her değiştirmek için örneğini `Convert.ToInt32` yönteme `Convert.ToDouble`.

1. Hesaplayıcı uygulamanızı çalıştırın ve sayı bölmek **42,5** numarasıyla **119.75**.

   Uygulama artık ondalık değer kabul eder ve sonuç olarak daha uzun bir ondalık sayı döndüren dikkat edin.

    ![Konsol penceresi artık ondalık sayılar kabul eder ve daha uzun bir ondalık sayı sonuç olarak döndüren hesaplayıcı uygulama gösteriliyor](./media/csharp-console-calculator-usedecimals.png)

    (Ondalık basamak sayısını gidereceğiz [kod gözden geçirme](#revise-the-code) bölümüne.)

## <a name="debug-the-app"></a>Uygulamasında hata ayıklama

Temel hesaplayıcı uygulamamız iyileştirdik, ancak bu henüz failsafes yerde kullanıcı giriş hataları gibi özel durumları işlemek için gerekli değildir.

Örneğin, bir sayı sıfıra bölme veya uygulama bir sayısal karakter beklerken bir alfa karakter girin denerseniz (veya tersi), Uygulama çalışmayı durduruyor ve bir hata döndürür.

Şimdi bazı ortak kullanıcı giriş hatalarını yol, bunları hata ayıklayıcıda bulun ve bunları kodda düzeltin.

>[!TIP]
>Hata ayıklayıcı ve nasıl çalıştığı hakkında daha fazla bilgi için bkz. [Visual Studio hata ayıklayıcıya ilk bakış](../../debugger/debugger-feature-tour.md) sayfası.

### <a name="fix-the-divide-by-zero-error"></a>"Sıfıra" hatayı düzeltin

Konsol uygulaması, bir sayı sıfıra bölünme çalıştığınızda, donuyor. Visual Studio ardından, Kod Düzenleyicisi'nde sorunun ne olduğunu gösterir.

   ![Visual Studio Kod Düzenleyicisi'ni sıfırla bölme hatayı gösterir](./media/csharp-console-calculator-dividebyzero-error.png)

Bu hatayı işlemek üzere kod değiştirelim.

1. Doğrudan arasında görünür kodunu silmek `case "d":` belirten açıklama `// Wait for the user to respond before closing`.

1. Bunu, aşağıdaki kodla değiştirin:

   ```csharp
            // Ask the user to enter a non-zero divisor until they do so
                while (num2 == 0)
                {
                    Console.WriteLine("Enter a non-zero divisor: ");
                    num2 = Convert.ToInt32(Console.ReadLine());
                }
                Console.WriteLine($"Your result: {num1} / {num2} = " + (num1 / num2));
                break;
        }
    ```

   Bölümü kodun ekledikten sonra `switch` deyimi aşağıdaki ekran görüntüsüne benzer görünmelidir:

   ![Visual Studio Kod düzenleyicisinde düzeltilmiş "anahtar" bölümü](./media/csharp-console-calculator-switch-code.png)

Artık, herhangi bir sayı sıfıra bölünme, uygulama için başka bir numara sorar. Hatta daha iyi: Sıfır dışındaki bir sayı sağladığınız kadar isteyen durdurmaz.

   ![Visual Studio Kod Düzenleyicisi'ni sıfırla bölme hatayı gösterir](./media/csharp-console-calculator-dividebyzero.png)

### <a name="fix-the-format-error"></a>"Format" hatayı düzeltin

Uygulamayı bir sayısal karakter beklerken bir alfa karakter girerseniz (veya tersi) konsol uygulaması donuyor. Visual Studio ardından, Kod Düzenleyicisi'nde sorunun ne olduğunu gösterir.

   ![Visual Studio Kod Düzenleyicisi'ni biçim hatası gösterir.](./media/csharp-console-calculator-format-error.png)

Bu hatayı düzeltmek için size daha önce girdiğiniz kodun düzenlemelisiniz.

#### <a name="revise-the-code"></a>Kodu gözden geçirin

Dayanan yerine `program` tüm kod işlemek için sınıf, biz uygulamamızı iki sınıflara bölün: `calculator` ve `program`.

`calculator` Sınıfı hesaplama iş toplu işlemek ve `program` sınıfı, kullanıcı arabirimi ve hata yakalama iş işleyecek.

Haydi başlayalım.

1. Her şeyi sildiğinizden *sonra* aşağıdaki kod bloğu:

    ```csharp

    using System;

    namespace Calculator
    {

    ```

1. Ardından, yeni bir ekleme `calculator` sınıfına aşağıdaki gibi:

    ```csharp
    class Calculator
    {
        public static double DoOperation(double num1, double num2, string op)
        {
            double result = double.NaN; // Default value is "not-a-number" which we use if an operation, such as division, could result in an error

            // Use a switch statement to do the math
            switch (op)
            {
                case "a":
                    result = num1 + num2;
                    break;
                case "s":
                    result = num1 - num2;
                    break;
                case "m":
                    result = num1 * num2;
                    break;
                case "d":
                    // Ask the user to enter a non-zero divisor
                    if (num2 != 0)
                    {
                        result = num1 / num2;
                    }
                    break;
                // Return text for an incorrect option entry
                default:
                    break;
            }
            return result;
        }
    }

    ```

1. Ardından, yeni bir ekleme `program` sınıfına aşağıdaki gibi:

    ```csharp
    class Program
    {
        static void Main(string[] args)
        {
            bool endApp = false;
            // Display title as the C# console calculator app
            Console.WriteLine("Console Calculator in C#\r");
            Console.WriteLine("------------------------\n");

            while (!endApp)
            {
                // Declare variables and set to empty
                string numInput1 = "";
                string numInput2 = "";
                double result = 0;

                // Ask the user to type the first number
                Console.Write("Type a number, and then press Enter: ");
                numInput1 = Console.ReadLine();

                double cleanNum1 = 0;
                while (!double.TryParse(numInput1, out cleanNum1))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput1 = Console.ReadLine();
                }

                // Ask the user to type the second number
                Console.Write("Type another number, and then press Enter: ");
                numInput2 = Console.ReadLine();

                double cleanNum2 = 0;
                while (!double.TryParse(numInput2, out cleanNum2))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput2 = Console.ReadLine();
                }

                // Ask the user to choose an operator
                Console.WriteLine("Choose an operator from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                string op = Console.ReadLine();

                try
                {
                    result = Calculator.DoOperation(cleanNum1, cleanNum2, op);
                    if (double.IsNaN(result))
                    {
                        Console.WriteLine("This operation will result in a mathematical error.\n");
                    }
                    else Console.WriteLine("Your result: {0:0.##}\n", result);
                }
                catch (Exception e)
                {
                    Console.WriteLine("Oh no! An exception occurred trying to do the math.\n - Details: " + e.Message);
                }

                Console.WriteLine("------------------------\n");

                // Wait for the user to respond before closing
                Console.Write("Press 'n' and Enter to close the app, or press any other key and Enter to continue: ");
                if (Console.ReadLine() == "n") endApp = true;

                Console.WriteLine("\n"); // Friendly linespacing
            }
            return;
        }
    }
    ```

1. Seçin **hesaplayıcı** , programınızı çalıştırmak için veya basın **F5**.

1. Komut istemlerini izleyin ve sayı bölmek **42** numarasıyla **119**. Uygulamanız aşağıdaki gibi görünmelidir:

    ![Hangi Eylemler ve hata işleme için hatalı girişleri istemlerinde içeren UIMap'e yeniden işlenmiş hesaplayıcı uygulama gösteren konsol penceresi](./media/csharp-console-calculator-refactored.png)

    Konsol uygulamasını kapatmak seçene kadar daha fazla denklemler girmek için seçenek olduğunu fark edeceksiniz. Ve sonuçta ondalık basamak sayısını azalttık de.

## <a name="close-the-app"></a>Uygulamayı kapatın

1. Zaten yapmadıysanız, hesaplayıcı uygulamayı kapatın.

1. Kapat **çıkış** Visual Studio'daki bölmesi.

   ![Visual Studio çıktı bölmesini kapatın](./media/csharp-calculator-close-output-pane.png)

1. Visual Studio'da **Ctrl**+**S** uygulamanızı kaydetmek için.

1. Visual Studio’yu kapatın.

## <a name="code-complete"></a>Kod tamamlandı

Bu öğretici sırasında hesaplayıcı uygulamaya çok değişiklikler yaptık. Uygulama artık bilgi işlem kaynaklarının daha verimli bir biçimde gerçekleştirir ve çoğu kullanıcı giriş hatalarını işler.

Tek bir yerde tam kod şöyledir:

```csharp

using System;

namespace Calculator
{
    class Calculator
    {
        public static double DoOperation(double num1, double num2, string op)
        {
            double result = double.NaN; // Default value is "not-a-number" which we use if an operation, such as division, could result in an error

            // Use a switch statement to do the math
            switch (op)
            {
                case "a":
                    result = num1 + num2;
                    break;
                case "s":
                    result = num1 - num2;
                    break;
                case "m":
                    result = num1 * num2;
                    break;
                case "d":
                    // Ask the user to enter a non-zero divisor
                    if (num2 != 0)
                    {
                        result = num1 / num2;
                    }
                    break;
                // Return text for an incorrect option entry
                default:
                    break;
            }
            return result;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            bool endApp = false;
            // Display title as the C# console calculator app
            Console.WriteLine("Console Calculator in C#\r");
            Console.WriteLine("------------------------\n");

            while (!endApp)
            {
                // Declare variables and set to empty
                string numInput1 = "";
                string numInput2 = "";
                double result = 0;

                // Ask the user to type the first number
                Console.Write("Type a number, and then press Enter: ");
                numInput1 = Console.ReadLine();

                double cleanNum1 = 0;
                while (!double.TryParse(numInput1, out cleanNum1))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput1 = Console.ReadLine();
                }

                // Ask the user to type the second number
                Console.Write("Type another number, and then press Enter: ");
                numInput2 = Console.ReadLine();

                double cleanNum2 = 0;
                while (!double.TryParse(numInput2, out cleanNum2))
                {
                    Console.Write("This is not valid input. Please enter an integer value: ");
                    numInput2 = Console.ReadLine();
                }

                // Ask the user to choose an operator
                Console.WriteLine("Choose an operator from the following list:");
                Console.WriteLine("\ta - Add");
                Console.WriteLine("\ts - Subtract");
                Console.WriteLine("\tm - Multiply");
                Console.WriteLine("\td - Divide");
                Console.Write("Your option? ");

                string op = Console.ReadLine();

                try
                {
                    result = Calculator.DoOperation(cleanNum1, cleanNum2, op);
                    if (double.IsNaN(result))
                    {
                        Console.WriteLine("This operation will result in a mathematical error.\n");
                    }
                    else Console.WriteLine("Your result: {0:0.##}\n", result);
                }
                catch (Exception e)
                {
                    Console.WriteLine("Oh no! An exception occurred trying to do the math.\n - Details: " + e.Message);
                }

                Console.WriteLine("------------------------\n");

                // Wait for the user to respond before closing
                Console.Write("Press 'n' and Enter to close the app, or press any other key and Enter to continue: ");
                if (Console.ReadLine() == "n") endApp = true;

                Console.WriteLine("\n"); // Friendly linespacing
            }
            return;
        }
    }
}

```

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticiyi tamamlamak Tebrikler! Daha da fazla bilgi edinmek için şu öğretici ile devam edin.

> [!div class="nextstepaction"]
> [Daha fazla devam C# öğreticiler](/dotnet/csharp/tutorials/)

## <a name="see-also"></a>Ayrıca bkz.

* [C# IntelliSense](../../ide/visual-csharp-intellisense.md)
* [Hata ayıklamayı öğrenin C# Visual Studio'daki kod](tutorial-debugger.md)
