---
title: Visual Studio'da değişkenleri bir izleme ayarlayın | Microsoft Docs
ms.custom: H1Hack27Feb2017
ms.date: 10/11/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.watch
helpviewer_keywords:
- debugging [Visual Studio], Watch window
- expressions [debugger], evaluating
- variables [debugger], evaluating
- expression evaluation
- registers, evaluating
- debugging [Visual Studio], expression evaluation
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ad08799c0dce3792e096291dfaf62d52e2515df4
ms.sourcegitcommit: 48bc8492973e93612e5afaba3b47d0f98aecf97c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49325022"
---
# <a name="set-a-watch-on-variables-using-the-watch-and-quickwatch-windows-in-visual-studio"></a>Visual Studio'da izleme ve QuickWatch windows kullanarak bir izleme ayarlayın

Hata ayıklarken, kullanabileceğiniz **Watch** ve **QuickWatch** değişkenleri ve ifadeleri izlemek için windows.  Fark **Watch** penceresi, çeşitli değişkenleri görüntüleyebilir ancak **QuickWatch** penceresi bir kerede tek bir değişken görüntüler.

Windows, yalnızca hata ayıklama oturumu sırasında kullanılabilir. Açmak için **Watch** penceresinde seçin **hata ayıklama** > **Windows** > **Watch**, seçin**1 izleyin**, **2 izleyin**, **3 izleyin**, veya **izleyin 4**. Açmak için **QuickWatch** penceresi, değişkeni sağ tıklayıp seçin **QuickWatch**, veya yalnızca seçin **hata ayıklama** > **QuickWatch** .

## <a name="observe-variables-with-the-watch-window"></a>İzleme penceresi değişkenleri gözlemleyin

Birden fazla değişkenle inceleyebileceğiniz **Watch** penceresi. Örneğin, aşağıdaki kodu varsa:

```C++
int main()
{
    int a, b, c;
    a = 1;
    b = 2;
    c = 0;

    for (int i = 0; i < 10; i++)
    {
        a++;
        b *= 2;
        c = a + b;
    }

    return 0;
}

```

Eklemek için üç değişkenlerin değerleri **Watch** penceresi aşağıdaki gibi:

1. Seçin `c = a + b;` satır.

2. Bir kesme noktası ayarlayın (seçerek **hata ayıklama** > **iki durumlu kesme noktası** veya F9 tuşuna basarak).

3. Hata ayıklama (F5) başlatın. Yürütme kesme noktasında durur.

4. Açık **Watch** penceresi (seçerek **hata ayıklama** > **Windows** > **Watch**  >   **Watch 1**, ya da Ctrl + Alt + W, 1 tuşuna basın).

5. Boş bir satırı seçin ve değişken türü `a`. Ardından değişkenlerinin aynı şeyi yapmak `b` ve `c`.

   ![Değişkenleri izleyin](../debugger/media/watchvariables.png "WatchVariables")

6. Hata ayıklayıcı ilerlemek için gerektiği şekilde F11 tuşuna basarak hata ayıklamaya devam et.

Değişken değerleri, yinelenecek şekilde değiştirme görmelisiniz `for` döngü.

Yerel kodda programlama, bazen bir değişken adının bağlamını veya bir değişken adı olan bir ifade nitelemeniz gerekebilir. , İşlev, kaynak dosyası ve bir değişkenin bulunduğu modül bağlamıdır. Bağlam nitelemek varsa, içerik işleci sözdizimini kullanabilirsiniz. Daha fazla bilgi için [bağlam işleci (C++)](../debugger/context-operator-cpp.md).

## <a name="observe-expressions-with-the-watch-window"></a>İzleme penceresinde ifadelerle gözlemleyin

Artık bir ifade kullanmayı deneyelim. Hata ayıklayıcı tarafından tanınan herhangi bir geçerli ifade ekleyebilirsiniz.

Örneğin, önceki bölümde listelenen kodu varsa, bu ifade kullanarak üç değerlerin ortalamasını alabilirsiniz:

![İfadeyi İzle](../debugger/media/watchexpression.png "WatchExpression")

İfadeleri değerlendirme kuralları **Watch** penceresi genellikle aynı olur, kodlama dili ifadelerinde değerlendirme kuralları. İfadeniz söz dizimi hatası varsa, Kod Düzenleyicisi'nde gördüklerinizle aynı derleyici hatası bekler. Örnek buradadır:

![İfade hatası izleyin](../debugger/media/watchexpressionerror.png "WatchExpressionError")

## <a name="bkmk_refreshWatch"></a> Güncel değil Gözcü değerlerini yenileme

Bir yenileme simgesi (döngüsel bir ok) içinde bir ifade değerlendirildiğinde görünebilir **Watch** penceresi. Özellik değerlendirmeyi devre dışı açtıysanız (seçerek **Araçları** > **seçenekleri** > **hata ayıklama**  >   **Genel**, sonra Temizleme **özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştir**), ve aşağıdaki kodu yazdığınız:

```csharp
static void Main(string[] args)
{
    List<string> list = new List<string>();
    list.Add("hello");
    list.Add("goodbye");
}

```

Bir izleme ayarlayın, aşağıdaki görüntüye benzer bir şey görmelisiniz `Count` listenin özelliği:

![RefreshWatch](../debugger/media/refreshwatch.png "RefreshWatch")

Önceki çizimde, bir hata veya güncel değil bir değeri gösterir. Simgesini seçerek değeri genellikle yenileyebilirsiniz ancak bazı durumlarda yenileme değil de tercih edebilirsiniz. İlk neden değeri Hesaplandı değildi bilmeniz gerekir.

Bir araç ipucu ifade neden değerlendirilen değildi simgesinin üzerine getirin, hakkında bilgi sağlar. İfade, circling oklar görünüyorsa, aşağıdaki nedenlerden biri için değerlendirme değildi:

- İfade değerlendirildiğinde gibi bir hata oluştu. Örneğin, bir zaman aşımı oluşmuş olabilir veya bir değişken kapsam dışına silinmiş olabilir.

- Uygulamada bir yan etkisi tetikleyebilir bir işlev çağrısı ifadesi vardır (bkz [yan etkiler ve ifadeler](#bkmk_sideEffects) bölümü).

- Özellikleri otomatik olarak değerlendirilmesini devre dışı etkinleştirdiyseniz ve hata ayıklayıcı tarafından örtük işlev çağırır (seçerek **Araçları** > **seçenekleri** > **hataayıklama**  >  **Genel**, sonra Temizleme **özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştir**). İfade sonra otomatik olarak değerlendirilemiyor.

Değer yenilemek için yenile simgesini seçin veya Ara çubuğuna basın. Hata ayıklayıcısı ifadeyi yeniden dener. Özellikleri ve diğer örtük işlev çağrılarını otomatik olarak değerlendirilmesini kapatıldığı için yenile simgesini görünebilir. Bu durumda, hata ayıklayıcı ifade değerlendirebilirsiniz.

Bir simge, iş parçacıkları benzer iki dalgalı çizgiler daire görünebilir. Bu simge, hata ayıklayıcı olası iş parçacıkları arası bağımlılık nedeniyle ifadeyi değerlendirmez anlamına gelir. Diğer bir deyişle, kodu değerlendirme, geçici olarak çalışması için uygulamanızı diğer iş parçacıkları gerektirir. Kesme modunda olduğunda, uygulamanızdaki tüm iş parçacıkları genellikle durdurulur. Diğer iş parçacıklarını geçici olarak çalışmasına izin vererek olabilir beklenmeyen etkiler, programınızın durumunu ve kesme noktaları ve bu iş parçacıkları üzerinde oluşturulan özel durumlar gibi olayları yok saymak hata ayıklayıcı neden olur.

## <a name="bkmk_sideEffects"></a> Yan etkiler ve ifadeler

Bazı ifadelerin değerlendirilmesi bir değişkenin değerini değiştirebilir veya aksi halde, programınızın durumunu etkileyebilir. Örneğin, aşağıdaki ifade değerlendirildiğinde değerini değiştirir `var1`:

```csharp
var1 = var2
```

Bu kodu neden olabilir bir [yan etkisi](https://en.wikipedia.org/wiki/Side_effect_\(computer_science\)). Yan etkileri hata ayıklama daha zor, programınızın çalışma yöntemlerini değiştirerek yapabilirsiniz.

Yan etkileri olduğu bilinen bir ifade, yalnızca ilk önce onu girdiğinizde bir kez değerlendirilir. Daha fazla değerlendirmeler devre dışıdır. El ile değerin yanında görüntülenen bir güncelleştirme simgesini seçerek bu davranışı geçersiz kılabilirsiniz.

Tüm yan etkileri önlemek için bir yol olan otomatik İşlev değerlendirmesi'ni açmak için (seçerek **Araçları** > **seçenekleri** > **hata ayıklama**  >  **Genel**, sonra Temizleme **özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştir**).

Değerlendirme özellikleri ya da örtük işlev çağrılarını devre dışı bırakıldığında kullanarak değerlendirme zorlayabilirsiniz **ac** biçim belirleyici (için yalnızca C#). Bkz: [biçim belirleyiciler C#](../debugger/format-specifiers-in-csharp.md).

## <a name="bkmk_objectIds"></a> Nesne tanımlayıcıları (C# ve Visual Basic) İzleme penceresinde kullanın

Bazen, belirli bir nesneyi davranışını gözlemlemek istediğiniz. Örneğin, bu değişken kapsam dışına geçti sonra bir yerel değişkeni tarafından başvurulan nesne izlemek isteyebilirsiniz. C# ve Visual Basic'te belirli örneklerini başvuru türleri için nesne kimliklerini oluşturabilir ve bunları kullanmak **Watch** penceresi ve kesme noktası koşulları. Nesne Kimliği hizmetlerinde hata ayıklama ortak dil çalışma zamanı tarafından (CLR) oluşturulan ve nesnesiyle ilişkili.

> [!NOTE]
> Nesne kimlikleri nesnenin çöp olarak toplanacak engellemek yoksa zayıf başvurular oluşturun. Bunlar, yalnızca geçerli hata ayıklama oturumu için geçerli olur.

Aşağıdaki kodda, bir metot oluşturur bir `Person` ne yaptığını öğrenmek yerel bir değişken, ancak kullanarak istediğiniz `Person`ait farklı bir yöntemde adıdır:

```csharp
class Person
{
    public Person(string name)
    {
        Name = name;
    }
    public string Name { get; set; }
}

public class Program
{
    static List<Person> _people = new List<Person>();
    public static void Main(string[] args)
    {
        MakePerson();
        DoSomething();
    }

    private static void MakePerson()
    {
        var p = new Person("Bob");
        _people.Add(p);
    }

    private static void DoSomething()
    {
        // more processing
         Console.WriteLine("done");
    }
}

```

Bir başvuru ekleyebilirsiniz `Person` nesnesine **Watch** penceresi aşağıdaki gibi:

1. Nesneyi oluşturan gerçekleşir kodda bir satır seçin.

2. Bir kesme noktası ayarlayın (seçerek **hata ayıklama** > **iki durumlu kesme noktası** veya F9 tuşuna basarak).

3. Hata ayıklama başlatılamıyor.

4. Yürütme kesme noktasında durur açtığınızda **Yereller** penceresi (seçerek **hata ayıklama** > **Windows** > **Yereller**), değişkeni sağ tıklatın ve seçin **nesne kimliği yap**.

   Bir dolar işareti görmeniz gerekir (**$**) bir sayı artı **Yereller** nesne kimliği olan penceresi

   > [!NOTE]
   > Nesnenin özellikleri gibi görmek istiyorsanız `Person.Name`, özellik değerlendirmesini seçerek etkinleştirmelisiniz **Araçları** > **seçenekleri**  >   **Hata ayıklama** > **genel**, ardından ayarı **özellik değerlendirmesini ve diğer örtük işlev çağrılarını etkinleştir**.

5. Nesne kimliği ekleme **Watch** dolar işareti ve sayı sağ tıklayıp, ardından seçme penceresi **Gözcü Ekle**.

6. Nesnenin davranışını gözlemlemek istediğiniz bir kesme noktası ayarlayın.  Önceki kodda, olurdu içinde `DoSomething()` yöntemi.

7. Hata ayıklamaya devam et. Yürütme durduğunda `DoSomething()` yöntemi **Watch** pencere görüntüler `Person` nesne.

## <a name="use-registers-in-the-watch-window-c-only"></a>Kullanım kayıtları İzleme penceresinde (yalnızca C++)

YAZMAÇ adlarını ve değişken adları kullanarak ekleyebilirsiniz  **$ \<kaydetme&nbsp;adı >** veya  **@ \<kaydetme&nbsp;adı >** yerel kodda hata ayıklama sırasında. Daha fazla bilgi için [sözde değişken](../debugger/pseudovariables.md).

## <a name="dynamic-view-and-the-watch-window"></a>Dinamik Görünüm ve İzleme penceresi

Bazı komut dosyası dilleri (örneğin, JavaScript veya Python) dinamik kullanın veya [yazarak duck](https://en.wikipedia.org/wiki/Duck_typing), ve .NET dillerinde (sürüm 4.0 ve üzeri) destek olduğundan normal hata ayıklama pencerelerini kullanarak gözlemek çok zor olan nesneler, çalışma zamanı özellikleri ve yöntemleri görüntülenemiyor olabilir.

**Watch** penceresi uygulayan bir tür oluşturan bir dinamik Nesne görüntüleyebilir <xref:System.Dynamic.IDynamicMetaObjectProvider> arabirimi. Bu nesne görüntülendiğinde, hata ayıklayıcısı özel bir ekler **dinamik Görünüm** açarsanız nesne adının alt düğüm **Otolar** penceresi (seçerek **hata ayıklama**  >  **Windows** > **Otolar**). Bu düğüm, dinamik dinamik Nesne üyelerini gösterir ancak üye değerlerinin düzenlenmesine izin vermez.

Yeni bir izleme eklemek için değişken, bir dinamik nesneye bir nesne çevirir:

1. Bir alt sağ bir **dinamik Görünüm**.
2. Seçin **izleme Ekle**. Ardından `object.name` olur `((dynamic) object).name`.

Üyeleri değerlendirme bir **dinamik Görünüm** yan etkileri olabilir. Yan etkileri nelerdir açıklaması için bkz [yan etkiler ve ifadeler](#bkmk_sideEffects) bölümü. C# ' ta hata ayıklayıcı otomatik olarak gösterilen değerlerini yeniden değerlendir değil **dinamik Görünüm** yeni bir kod satırına geçtiğinizde. Visual Basic için ifade eklenen **dinamik Görünüm** otomatik olarak yenilenir.

Nasıl yenileneceği hakkında yönergeler için **dinamik Görünüm** değerleri, görmek [güncel Yenile Gözcü değerlerini](#bkmk_refreshWatch) bölümü.

Yalnızca görüntülemek istiyorsanız **dinamik Görünüm** bir nesne için kullanabileceğiniz **dinamik** biçim belirticisi içinde **Watch** penceresi:

- C# İÇİN: `ObjectName, dynamic`
- Visual Basic: `$dynamic, ObjectName`

**Dinamik Görünüm** COM nesneleri için hata ayıklama deneyimini de geliştirir. Hata ayıklayıcı zaman alır, sarılı bir COM nesnesi için **System.comobject'e**, ekler bir **dinamik Görünüm** düğüm nesnesi.

## <a name="observe-a-single-variable-or-expression-with-quickwatch"></a>Tek bir değişken veya QuickWatch ifadesiyle gözlemleyin

Kullanabileceğiniz **QuickWatch** penceresi tek bir değişken gözlemleyin. Örneğin, aşağıdaki kodu varsa:

```csharp
static void Main(string[] args)
{
    int a, b;
    a = 1;
    b = 2;
    for (int i = 0; i < 10; i++)
    {
        a = a + b;
    }
}
```

Bir değişkende inceleyebileceğiniz **QuickWatch** penceresi aşağıdaki gibi:

1. Bir kesme noktası ayarlamak `a = a + b;` satır.

2. Hata ayıklama başlatılamıyor. Yürütme kesme noktasında durur.

3. Değişken seçme `a`.

4. Seçin ya da **hata ayıklama** > **QuickWatch** veya basın **SHIFT + F9**. **QuickWatch** penceresi görüntülenir. İçinde **değer** kutusunda `a` değişkeni 1 değeriyle gösterilir.

   ![QuickWatch değişkeni](../debugger/media/quickwatchvariable.png "QuickWatchVariable")

   Türü gibi bir ifade değişkeni kullanarak bir ifadeyi değerlendirmek için `a + b` için **ifade** kutusuna ve tıklatın **yeniden değerlendir**.

   ![QuickWatch ifade](../debugger/media/quickwatchexpression.png "QuickWatchExpression")

   Değişken veya ifadeyi eklemek için **Watch** penceresinden **QuickWatch**, seçin **Gözcü Ekle**.

   > [!NOTE]
   > **QuickWatch** penceresi olan bir kalıcı iletişim kutusu penceresinin açık olduğu sürece hata ayıklama devam edemiyor bu nedenle.

5. Kapat **QuickWatch** penceresi. Değeri gözlemleyin sırasında hata ayıklama devam edebilmeniz için artık **Watch** penceresi.

## <a name="see-also"></a>Ayrıca bkz.

[Hata ayıklayıcısı pencereleri](../debugger/debugger-windows.md)
