---
title: C#Birim test Öğreticisi
ms.date: 05/14/2019
ms.topic: conceptual
helpviewer_keywords:
- unit tests, walkthrough
- unit tests, creating
- unit tests, generating
- unit tests, running
- unit tests, authoring
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
author: gewarren
ms.openlocfilehash: 7c588966a957cf6d3127e03c67ad1a1d605fabce
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66401728"
---
# <a name="walkthrough-create-and-run-unit-tests-for-managed-code"></a>İzlenecek yol: Yönetilen kod için birim testleri oluşturma ve çalıştırma

Bu makalede, oluşturma işleminde, çalışan, adımları ve bir dizi birim özelleştirme yönetilen kod ve Visual Studio için Microsoft birim test çerçevesini kullanarak testleri **Test Gezgini**. Geliştirilmekte olan bir C# projesi ile başlayın, kodunu, testleri çalıştırmak ve sonuçları inceleyin testleri oluşturun. Daha sonra proje kodunu değiştirin ve testleri yeniden çalıştırın.

## <a name="create-a-project-to-test"></a>Test etmek için bir proje oluşturun

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

2. Üzerinde **dosya** menüsünde **yeni** > **proje**.

   **Yeni Proje** iletişim kutusu görünür.

3. Altında **Visual C#**  > **.NET Core** kategorisi seçin **konsol uygulaması (.NET Core)** proje şablonu.

4. Projeyi adlandırın **banka**ve ardından **Tamam**.

   Banka projesi oluşturulur ve görüntülenen **Çözüm Gezgini** ile *Program.cs* dosyası Kod Düzenleyicisi'nde açın.

   > [!NOTE]
   > Varsa *Program.cs* olduğu değil, düzenleyicide açın, dosyayı çift tıklatın *Program.cs* içinde **Çözüm Gezgini** açın.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın.

2. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

3. Arayın ve seçin C# **konsol uygulaması (.NET Core)** proje şablonu ve ardından **sonraki**.

4. Projeyi adlandırın **banka**ve ardından **Oluştur**.

   Banka projesi oluşturulur ve görüntülenen **Çözüm Gezgini** ile *Program.cs* dosyası Kod Düzenleyicisi'nde açın.

   > [!NOTE]
   > Varsa *Program.cs* olduğu değil, düzenleyicide açın, dosyayı çift tıklatın *Program.cs* içinde **Çözüm Gezgini** açın.

::: moniker-end

5. Öğesinin içeriğini değiştirin *Program.cs* aşağıdaki C# tanımlayan bir sınıf kodu *BankAccount*:

   ```csharp
   using System;

   namespace BankAccountNS
   {
       /// <summary>
       /// Bank account demo class.
       /// </summary>
       public class BankAccount
       {
           private readonly string m_customerName;
           private double m_balance;

           private BankAccount() { }

           public BankAccount(string customerName, double balance)
           {
               m_customerName = customerName;
               m_balance = balance;
           }

           public string CustomerName
           {
               get { return m_customerName; }
           }

           public double Balance
           {
               get { return m_balance; }
           }

           public void Debit(double amount)
           {
               if (amount > m_balance)
               {
                   throw new ArgumentOutOfRangeException("amount");
               }

               if (amount < 0)
               {
                   throw new ArgumentOutOfRangeException("amount");
               }

               m_balance += amount; // intentionally incorrect code
           }

           public void Credit(double amount)
           {
               if (amount < 0)
               {
                   throw new ArgumentOutOfRangeException("amount");
               }

               m_balance += amount;
           }

           public static void Main()
           {
               BankAccount ba = new BankAccount("Mr. Bryan Walton", 11.99);

               ba.Credit(5.77);
               ba.Debit(11.22);
               Console.WriteLine("Current balance is ${0}", ba.Balance);
           }
       }
   }
   ```

6. Dosyayı Yeniden Adlandır *BankAccount.cs* sağ tıklayıp seçme **Yeniden Adlandır** içinde **Çözüm Gezgini**.

7. Üzerinde **derleme** menüsünde tıklatın **Çözümü Derle**.

Şimdi, test yöntemleri içeren bir proje var. Bu makalede, testleri odaklanmak `Debit` yöntemi. `Debit` Yöntemi bir hesaptan para çekildiğinde olduğunda çağrılır.

## <a name="create-a-unit-test-project"></a>Birim testi projesi oluşturma

1. Üzerinde **dosya** menüsünde **Ekle** > **yeni proje**.

   > [!TIP]
   > Çözüm üzerinde sağ tıklatabilirsiniz **Çözüm Gezgini** ve **Ekle** > **yeni proje**.

::: moniker range="vs-2017"

2. İçinde **yeni proje** iletişim kutusunda **yüklü**, genişletme **Visual C#** ve ardından **Test**.

3. Şablonlar listesinden **MSTest Test projesi (.NET Core)** .

4. İçinde **adı** kutusuna `BankTests`ve ardından **Tamam**.

   **BankTests** projesi eklenir **banka** çözüm.

::: moniker-end

::: moniker range=">=vs-2019"

2. Arayın ve seçin C# **MSTest Test projesi (.NET Core)** proje şablonu ve ardından **sonraki**.

3. Projeyi adlandırın **BankTests**.

4. **Oluştur**'u tıklatın.

   **BankTests** projesi eklenir **banka** çözüm.

::: moniker-end

5. İçinde **BankTests** projesi, bir başvuru ekleyin **banka** proje.

   İçinde **Çözüm Gezgini**seçin **bağımlılıkları** altında **BankTests** proje ve ardından **Başvuru Ekle** sağ gelen menüsü.

6. İçinde **başvuru Yöneticisi** iletişim kutusunda **projeleri**seçin **çözüm**, iade edin **banka** öğesi.

7. **Tamam**’ı seçin.

## <a name="create-the-test-class"></a>Test sınıfı oluşturun

Doğrulamak için bir test sınıfı oluşturun `BankAccount` sınıfı. Kullanabileceğiniz *UnitTest1.cs* proje şablonu tarafından oluşturulan dosya, ancak dosyaya verin ve daha açıklayıcı adlar sınıfı. Dosyayı yeniden adlandırarak, tek bir adımda yapabilirsiniz **Çözüm Gezgini**.

### <a name="rename-a-file-and-class"></a>Dosya ve sınıf yeniden adlandır

1. İçinde dosyayı yeniden adlandırmak için **Çözüm Gezgini**seçin *UnitTest1.cs* BankTests projesindeki dosya. Sağ tıklama menüsünden **Yeniden Adlandır**ve ardından dosyayı yeniden adlandır *BankAccountTests.cs*.

   ::: moniker range="vs-2017"

   Açılan iletişim kutusunda seçin **Hayır**.

   ::: moniker-end

2. Sınıfı yeniden adlandırmak için imleci getirin `UnitTest1` Kod Düzenleyicisi ve tuşuna **F2** (veya sağ tıklayıp seçin **Yeniden Adlandır**). Yazın **BankAccountTests** ve tuşuna **Enter**.

*BankAccountTests.cs* dosyası artık şu kodu içerir:

```csharp
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace BankTests
{
    [TestClass]
    public class BankAccountTests
    {
        [TestMethod]
        public void TestMethod1()
        {
        }
    }
}
```

### <a name="add-a-using-statement"></a>Kullanarak bir ekleme deyimi

Ekleme bir [ `using` deyimi](/dotnet/csharp/language-reference/keywords/using-statement) tam adı kullanmadan test altındaki projeye çağırmak için test sınıfına. Sınıf dosyasının en üstüne ekleyin:

```csharp
using BankAccountNS;
```

### <a name="test-class-requirements"></a>Test sınıfı gereksinimleri

Bir test sınıfı için minimum gereksinimleri şunlardır:

- `[TestClass]` Özniteliği Test Gezgini'nde de çalıştırmak istediğiniz birim test yöntemlerini içeren herhangi bir sınıf üzerinde gereklidir.

- Test Explorer'ın bilmek istediğiniz her test yönteminin olmalıdır `[TestMethod]` özniteliği.

Sahip olmadığınız diğer birim testi projesi sınıflarda olabilir `[TestClass]` özniteliği ve diğer yöntemler bulunabilir sahip olmayan test sınıflarında `[TestMethod]` özniteliği. Bu diğer sınıflar ve yöntemler, test yöntemleri çağırabilir.

## <a name="create-the-first-test-method"></a>İlk test yöntemini oluştur

Bu yordamda, birim testi davranışını doğrulamak için yöntem yazacaksınız `Debit` yöntemi `BankAccount` sınıfı.

Denetlenmesi gereken en az üç davranış vardır:

- Çağırılıyorsa yöntem bir <xref:System.ArgumentOutOfRangeException> borç tutarı bakiyeden büyükse.

- Çağırılıyorsa yöntem bir <xref:System.ArgumentOutOfRangeException> borç tutarını küçükse sıfır.

- Yöntemi, Borç tutarını geçerliyse, hesap bakiyeniz borç tutarını çıkarır.

> [!TIP]
> Varsayılan silebilirsiniz `TestMethod1` yöntemi bu izlenecek yolda kullandığından olmaz.

### <a name="to-create-a-test-method"></a>Bir test yöntemi oluşturmak için

İlk testi, geçerli bir tutarın (diğer bir deyişle, bir hesap bakiyesinden ve sıfırdan küçük) doğru bir tutar hesaptan testimizde doğrular. Aşağıdaki yöntemi ekleyin `BankAccountTests` sınıfı:

```csharp
[TestMethod]
public void Debit_WithValidAmount_UpdatesBalance()
{
    // Arrange
    double beginningBalance = 11.99;
    double debitAmount = 4.55;
    double expected = 7.44;
    BankAccount account = new BankAccount("Mr. Bryan Walton", beginningBalance);

    // Act
    account.Debit(debitAmount);

    // Assert
    double actual = account.Balance;
    Assert.AreEqual(expected, actual, 0.001, "Account not debited correctly");
}
```

Yöntem oldukça basittir: yeni bir ayarlar `BankAccount` nesnesi bir Başlangıç bakiyesi ve geçerli bir süre sonra çeker. Kullandığı <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.AreEqual%2A?displayProperty=nameWithType> bitiş bakiyesini beklendiği gibi olduğunu doğrulamak için yöntem.

### <a name="test-method-requirements"></a>Test yöntemi gereksinimleri

Bir test yönteminin aşağıdaki gereksinimleri karşılaması gerekir:

- İle donatılmış `[TestMethod]` özniteliği.

- Döndürür `void`.

- Parametrelere sahip olamaz.

## <a name="build-and-run-the-test"></a>Derleme ve test çalıştırma

1. Üzerinde **derleme** menüsünde seçin **Çözümü Derle**.

2. Varsa **Test Gezgini** olan açın, seçerek açın **Test** > **Windows** > **Test Gezgini** gelen üst menü çubuğu.

3. Seçin **tümünü Çalıştır** testi çalıştırmak için.

   Test çalışırken en üstündeki durum çubuğunda **Test Gezgini** penceresi bir animasyon görünür. Testler başarısız olursa test çalışmasının sonunda, tüm test yöntemleri geçerse yeşil veya Kırmızı çubuk kapatır.

   Bu durumda, test başarısız olur.

4. Yöntemini seçin **Test Gezgini** pencerenin alt kısmındaki ayrıntılarını görüntülemek için.

## <a name="fix-your-code-and-rerun-your-tests"></a>Kodunuzu düzeltin ve testlerinizi yeniden çalıştırın

Test sonucu hatayı açıklayan bir ileti içerir. İçin `AreEqual` yöntemi iletiyi görüntüler beklenenle ve gerçekte ne alındı. Azaltmak için Bakiye bekleniyordu ancak bunun yerine, mevzuatı miktarına göre artar.

Birim testi bir hata ortaya çıkardı: mevzuatı miktarı *eklenen* olmalıydı hesap bakiyesine *çıkartılır*.

### <a name="correct-the-bug"></a>Hatayı düzeltin

İçinde hatayı düzeltmek için *BankAccount.cs* dosya, satırı değiştirin:

```csharp
m_balance += amount;
```

İle:

```csharp
m_balance -= amount;
```

### <a name="rerun-the-test"></a>Testi yeniden çalıştırın

İçinde **Test Gezgini**, seçin **tümünü Çalıştır** ve testi yeniden çalıştırın. Kırmızı/yeşil çubuk geçilen testleri göstermek için yeşile döner.

![Visual Studio 2019 gösteren test Gezgini'nde test geçildi](media/test-explorer-banktests-passed.png)

## <a name="use-unit-tests-to-improve-your-code"></a>Kodunuzu geliştirmek için birim testleri kullanın

Bu bölümde, analiz, birim testi geliştirmenin ve yeniden düzenleme düzenlemenin yinelemeli işleminin üretim kodunuzu daha sağlam ve verimli hale getirmek nasıl yardımcı olabileceğini açıklar.

### <a name="analyze-the-issues"></a>Sorunları Çözümle

Geçerli bir süre içinde doğru çıkarılır onaylamak için bir test yöntemi oluşturduğunuz `Debit` yöntemi. Şimdi, çağırılıyorsa yöntem doğrulayın bir <xref:System.ArgumentOutOfRangeException> borç tutarını geçerli olduğunda:

- Bakiye büyüktür veya
- sıfırdan küçük.

### <a name="create-and-run-new-test-methods"></a>Oluşturun ve yeni test metotları çalıştırın

Borç tutarını olduğunda doğru davranış sıfırdan doğrulamak için bir test yöntemi oluşturun:

```csharp
[TestMethod]
[ExpectedException(typeof(ArgumentOutOfRangeException))]
public void Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange()
{
    // Arrange
    double beginningBalance = 11.99;
    double debitAmount = -100.00;
    BankAccount account = new BankAccount("Mr. Bryan Walton", beginningBalance);

    // Act
    account.Debit(debitAmount);

    // Assert is handled by the ExpectedException attribute on the test method.
}
```

Kullanım <xref:Microsoft.VisualStudio.TestTools.UnitTesting.ExpectedExceptionAttribute> doğru özel durumun oluşturulmasını onaylamak için özniteliği. Öznitelik, testin başarısız olmasına neden olan bir <xref:System.ArgumentOutOfRangeException> oluşturulur. Daha fazla genel oluşturmasına, test altındaki yöntemi geçici olarak değiştirirseniz <xref:System.ApplicationException> borç tutarını küçüktür, sıfır test düzgün şekilde davranan&mdash;diğer bir deyişle, işlem başarısız olur.

Çekilen miktarın bakiyeden büyük olduğunu test etmek için aşağıdaki adımları uygulayın:

1. Adlı yeni bir test yöntemi oluşturun `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange`.

2. Kopyalama yöntemi gövdesinden `Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange` yeni yönteme.

3. Ayarlama `debitAmount` bakiyeden büyük bir sayı.

İki test yöntemlerini çalıştıran, testler doğru bir şekilde çalıştığını gösterir.

### <a name="continue-the-analysis"></a>Çözümlemeye devam edin

Test edilen yöntemi daha da artırılabilir. Geçerli bir uygulama ile sahibiz hangi koşulun bilmeniz mümkün değildir (`amount > m_balance` veya `amount < 0`) test sırasında oluşturulan özel durum etmeleri. Yalnızca biliyoruz bir `ArgumentOutOfRangeException` yöntemi herhangi bir durum oluştu. Biz de olan koşul söyleyebilirsiniz daha iyi olurdu `BankAccount.Debit` özel durum oluşturulmasına neden (`amount > m_balance` veya `amount < 0`) size sunduğumuz yöntemi sağlamlık-bağımsız değişkenlerini doğru denetliyor, böylece oyunlarımızın.

Test edilen bir yöntem bakın (`BankAccount.Debit`) yeniden ve her iki koşullu deyimin kullanma bildirimi bir `ArgumentOutOfRangeException` yalnızca oluşturucu bağımsız değişken olarak bir parametre adını alır:

```csharp
throw new ArgumentOutOfRangeException("amount");
```

Çok daha zengin bilgi raporlarının bir oluşturucu kullanabilirsiniz: <xref:System.ArgumentOutOfRangeException.%23ctor(System.String,System.Object,System.String)> adını bağımsız değişken, bağımsız değişken değeri ve kullanıcı tanımlı bir ileti içerir. Bu oluşturucuyu kullanarak test altındaki yöntemi yeniden düzenleyebilirsiniz. Daha da iyi genel olarak kullanılabilen tür üyelerini hataları belirlemek için kullanabilirsiniz.

### <a name="refactor-the-code-under-test"></a>Test altındaki kodu yeniden düzenleyin

İlk olarak, sınıf kapsamındaki hata iletileri için iki sabiti tanımlayın. Bu sınıf, test altındaki yerleştirmek `BankAccount`:

```csharp
public const string DebitAmountExceedsBalanceMessage = "Debit amount exceeds balance";
public const string DebitAmountLessThanZeroMessage = "Debit amount is less than zero";
```

Ardından, iki koşullu ifadeler değiştirin `Debit` yöntemi:

```csharp
    if (amount > m_balance)
    {
        throw new ArgumentOutOfRangeException("amount", amount, DebitAmountExceedsBalanceMessage);
    }

    if (amount < 0)
    {
        throw new ArgumentOutOfRangeException("amount", amount, DebitAmountLessThanZeroMessage);
    }
```

### <a name="refactor-the-test-methods"></a>Test yöntemlerini yeniden düzenleme

Kaldırma `ExpectedException` test metodu özniteliği ve bunun yerine, oluşan özel durumları yakalamalı ve onun ilişkili ileti doğrulayın. <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert.Contains%2A?displayProperty=fullName> Yöntemi, iki dizeyi karşılaştırın olanağı sağlar.

Şimdi, `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange` şuna benzeyebilir:

```csharp
[TestMethod]
public void Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange()
{
    // Arrange
    double beginningBalance = 11.99;
    double debitAmount = 20.0;
    BankAccount account = new BankAccount("Mr. Bryan Walton", beginningBalance);

    // Act
    try
    {
        account.Debit(debitAmount);
    }
    catch (ArgumentOutOfRangeException e)
    {
        // Assert
        StringAssert.Contains(e.Message, BankAccount.DebitAmountExceedsBalanceMessage);
    }
}
```

### <a name="retest-rewrite-and-reanalyze"></a>Değişiyorsa, yeniden yaz ve yeniden Çözümle

Test altındaki yöntemin içindeki bir hata varsa varsayar ve `Debit` yöntemi bile throw değil bir <xref:System.ArgumentOutOfRangeException> hiçbir zaman göz önünde doğru iletiyi özel durumu ile çıktı. Şu anda test yöntemi, bu durumda işlemiyor. Varsa `debitAmount` değeri geçerlidir (diğer bir deyişle, değerinden Bakiye ama sıfırdan büyükse), böylece onay asla harekete hiçbir özel durum yakalandı. Henüz test yöntemi geçirilir. Test yöntemi özel durum oluşturmazsa başarısız istediğinden bu iyi değildir.

Bu, test yönteminde bir hatadır. Sorunu çözmek için ekleme bir <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.Fail%2A> nerede hiçbir özel durum durumu işlemek için test yönteminin sonunda onay.

Sınama gösterir, test artık *başarısız* doğru özel durum yakalandığında. `catch` Bloğu özel durumu yakalar, ancak yöntemi yürütmeye devam eder ve yeni başarısız <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.Fail%2A> onay. Bu sorunu çözmek için ekleme bir `return` deyiminden sonra `StringAssert` içinde `catch` blok. Testi yeniden çalıştırmak bu sorunu düzelttik onaylar. Son sürümü `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange` şöyle görünür:

```csharp
[TestMethod]
public void Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange()
{
    // Arrange
    double beginningBalance = 11.99;
    double debitAmount = 20.0;
    BankAccount account = new BankAccount("Mr. Bryan Walton", beginningBalance);

    // Act
    try
    {
        account.Debit(debitAmount);
    }
    catch (ArgumentOutOfRangeException e)
    {
        // Assert
        StringAssert.Contains(e.Message, BankAccount.DebitAmountExceedsBalanceMessage);
        return;
    }

    Assert.Fail("The expected exception was not thrown.");
}
```

### <a name="conclusion"></a>Sonuç

Test kodu yapılan iyileştirmeler, daha sağlam ve bilgilendirici test yöntemlerimiz olmasını sağladı. Ancak daha da önemlisi, test edilen kod'bunlar da gelişmiştir.

> [!TIP]
> Bu izlenecek yol, yönetilen kod için Microsoft birim testi çerçevesini kullanır. **Test Gezgini** ayrıca üçüncü taraf birim için bağdaştırıcıları olan test çerçevelerini testleri çalıştırabilirsiniz **Test Gezgini**. Daha fazla bilgi için [üçüncü taraf birim testi çerçevelerini yükleme](../test/install-third-party-unit-test-frameworks.md)

## <a name="see-also"></a>Ayrıca bkz.

Bir komut satırından testleri çalıştırma hakkında daha fazla bilgi için bkz: [VSTest.Console.exe komut satırı seçenekleri](vstest-console-options.md).
