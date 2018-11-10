---
title: Otolar ve yerel öğeler pencerelerinde değişkenleri İnceleme | Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 04/17/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.autos
- vs.debug.locals
helpviewer_keywords:
- debugger, variable windows
- debugging [Visual Studio], variable windows
ms.assetid: bb6291e1-596d-4af0-9f22-5fd713d6b84b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 35fa37831ad79a55effe849f8605ae6b5d299d3a
ms.sourcegitcommit: bc43970c000f07c9cc2051f1264a9742943a9755
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51349656"
---
# <a name="inspect-variables-in-the-autos-and-locals-windows"></a>Otolar ve yerel öğeler pencerelerinde değişkenleri denetleyin

**Otolar** ve **Yereller** windows ayıklarken değişken değerleri gösterir. Windows, yalnızca hata ayıklama oturumu sırasında kullanılabilir.

**Otolar** geçerli kesme noktası kullanılan değişkenler penceresi gösterir. **Yereller** penceresi, genellikle geçerli işlev veya yöntem olan yerel kapsamda tanımlanan değişkenler gösterir.

Açmak için **Otolar** hata ayıklarken, penceresinde **hata ayıklama** > **Windows** > **Otolar**, veya tuşuna basın **Ctrl**+**Alt**+**V** > **A**.

Açmak için **Yereller** hata ayıklarken, penceresinde **hata ayıklama** > **Windows** > **Yereller**, veya tuşuna basın **Alt**+**4**.

Temel hata ayıklama hakkında daha fazla bilgiye ihtiyacınız varsa bkz [hata ayıklayıcısını kullanmaya başlama](../debugger/getting-started-with-the-debugger.md).

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio'da veri görselleştirmeleri](/visualstudio/mac/data-visualizations).

## <a name="use-the-autos-and-locals-windows"></a>Otolar ve yerel öğeler pencerelerinde kullanın

Diziler ve nesneleri göster **Otolar** ve **Yereller** ağaç denetimleri olarak windows. Görünümü alanlar ve Özellikler'i gösterecek şekilde genişletmek için bir değişken adının sol tarafındaki oku seçin. İşte bir örnek bir <xref:System.IO.FileStream?displayProperty=fullName> nesnesine **Yereller** penceresi:

![Yerel öğeler FILESTREAM](../debugger/media/locals-filestream.png "Yereller FILESTREAM")

Kırmızı bir değer **Yereller** veya **Otolar** penceresi anlamına gelir değeri son değerlendirme bu yana değişti. Değişiklik, bir önceki hata ayıklama oturumundan olabilir veya penceresinde değeri değiştirildi.

Hata ayıklayıcı pencerelerinde varsayılan sayısal biçimi ondalık. Onaltılığa değiştirmek için sağ **Yereller** veya **Otolar** penceresi ve select **onaltılık gösterim**. Bu değişiklik tüm hata ayıklayıcı pencereleri etkiler.

## <a name="edit-variable-values-in-the-autos-or-locals-window"></a>Otomatik değişkenler veya yerel öğeler penceresinde değişken değerlerini düzenleyin

Çoğu değişkenin değerlerini düzenlemek için **Otolar** veya **Yereller** windows değerine çift tıklayın ve yeni bir değer girin.

Örneğin bir değer için bir ifade girin `a + b`. Hata ayıklayıcı en geçerli dili ifadelerini kabul eder.

Yerel C++ kod içinde bir değişken adının bağlamını nitelemeniz gerekebilir. Daha fazla bilgi için [bağlam işleci (C++)](../debugger/context-operator-cpp.md).

>[!CAUTION]
>Değerleri ve ifadeleri değiştirmeden önce sonuçları anladığınızdan emin olun. Olası bazı sorunlar şunlardır:
>
>-   Bazı ifadelerin değerlendirilmesi bir değişkenin değerini değiştirebilir veya aksi halde, programınızın durumunu etkileyebilir. Örneğin, değerlendirme `var1 = ++var2` hem değerini değiştirir `var1` ve `var2`. Bu deyimler olduğu söylenir [yan etkileri](https://en.wikipedia.org/wiki/Side_effect_\(computer_science\)). Yan etkiler, bunları uyumlu değilse, beklenmeyen sonuçlara neden olabilir.
>
>-   Kayan nokta değerlerini düzenlemek, kesirli bileşenlerin ondalıktan ikiliye dönüştürülmesi nedeniyle küçük yanlışlıklara neden olabilir. Görünüşte zararsız bir düzenleme bitler kayan nokta değişkenindeki bazı değişikliklere neden olabilir.

## <a name="change-the-context-for-the-autos-or-locals-window"></a>Bağlam otomatik değişkenler veya yerel öğeler penceresi için değiştirin

Kullanabileceğiniz **hata ayıklama konumu** istenen işlevi, iş parçacığı veya bağlamı değiştiren işlem seçmek için araç **Otolar** ve **Yereller** windows.

Etkinleştirmek için **hata ayıklama konumu** araç seçin ve araç çubuğu alanı boş bir bölümünden tıklama **hata ayıklama konumu** açılan ya da seçin **görünümü**  >   **Araç çubukları** > **hata ayıklama konumu**.

Bir kesme noktası ayarlayın ve hata ayıklamaya başlayın. Kesme noktası isabet edildiğinde yürütme duraklatır ve konumda görebilirsiniz **hata ayıklama konumu** araç çubuğu.

![Hata ayıklama konumu araç çubuğu](../debugger/media/debuglocationtoolbar.png "hata ayıklama konumu araç çubuğu")

## <a name="bkmk_whatvariables"></a> Otomatik değişkenler penceresi değişkenleri

 **Otolar** penceresi, kullanılabilir C#, Visual Basic ve C++ kodu, ancak JavaScript için veya F#.

 Farklı kod dilleri görüntülemek farklı değişkenlerinde **Otolar** penceresi.

 - İçinde C# ve Visual Basic **Otolar** geçerli ya da önceki satırında kullanılan herhangi bir değişken penceresinde görüntülenir. Örneğin, C# veya kod, aşağıdaki dört değişkenleri bildirin Visual Basic:

   ```csharp
       public static void Main()
       {
          int a, b, c, d;
          a = 1;
          b = 2;
          c = 3;
          d = 4;
       }
   ```

   Satırına bir kesme noktası ayarlamak `c = 3;`, ve hata ayıklayıcıyı başlatın. Yürütme durakladığında **Otolar** penceresi görüntülenir:

   ![Otolar-CSharp](../debugger/media/autos-csharp.png "Otolar-CSharp")

   Değerini `c` 0, çünkü satır `c = 3` henüz çalıştırılmadı.

 - C++ ' ta **Otolar** nerede yürütülmesi duraklatıldı geçerli satırı önce en az üç satır içinde kullanılan değişkenler penceresinde görüntülenir. Örneğin, C++ kodu altı değişkenleri bildirin:

   ```C++
       void main() {
           int a, b, c, d, e, f;
           a = 1;
           b = 2;
           c = 3;
           d = 4;
           e = 5;
           f = 6;
       }
   ```

    Satırına bir kesme noktası ayarlamak `e = 5;` ve hata ayıklayıcı çalıştırın. Yürütme sona erdiğinde, **Otolar** penceresi görüntülenir:

    ![Otolar C++](../debugger/media/autos-cplus.png "Otolar C++")

    Değişken `e` olduğundan başlatılmadı satır `e = 5` henüz çalıştırılmadı.

##  <a name="bkmk_returnValue"></a> Yöntem çağrılarının dönüş değerlerini görüntüleme
 .NET ve C++ kodunda, dönüş değerlerini inceleyebilirsiniz **Otolar** üzerinden veya bir yöntem çağrısının dışına adımladığınızda penceresi. Görüntüleme yöntem çağrısının dönüş yerel değişkenlerle depolanmaz değerleri kullanışlı olabilir. Bir yöntemi, bir parametre veya başka bir yöntemin dönüş değeri olarak kullanılabilir.

 Örneğin, aşağıdaki C# kod iki işlev dönüş değerlerini ekler:

```csharp
static void Main(string[] args)
{
    int a, b, c, d;
    a = 1;
    b = 2;
    c = 3;
    d = 4;
    int x = sumVars(a, b) + subtractVars(c, d);
}

private static int sumVars(int i, int j)
{
    return i + j;
}

private static int subtractVars(int i, int j)
{
    return j - i;
}
```

Dönüş değerleri görmek için `sumVars()` ve `subtractVars()` yöntemini çağırır Otolar penceresinde:

1. Bir kesme noktası ayarlamak `int x = sumVars(a, b) + subtractVars(c, d);` satır.

1. Hata ayıklamayı başlatmak ve yürütme kesme noktasında durakladığında seçin **Step Over** veya basın **F10**. Aşağıdaki dönüş değerleri görmelisiniz **Otolar** penceresi:

  ![Otolar dönüş değeri C# ](../debugger/media/autosreturnvaluecsharp2.png "Otolar dönüş değeriC#")

## <a name="see-also"></a>Ayrıca bkz.

- [Hata ayıklayıcısı pencereleri](../debugger/debugger-windows.md)
- [Mac için Visual Studio'da veri görselleştirmeleri](/visualstudio/mac/data-visualizations)
