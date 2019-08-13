---
title: C#birim testi öğreticisi
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
ms.openlocfilehash: 2c7a81eefc48626a57d15f99579e151390b52fb9
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926798"
---
# <a name="walkthrough-create-and-run-unit-tests-for-managed-code"></a>İzlenecek yol: Yönetilen kod için birim testleri oluşturma ve çalıştırma

Bu makalede, yönetilen kod ve Visual Studio **Test Gezgini**için Microsoft birim testi çerçevesini kullanarak bir dizi birim testi oluşturma, çalıştırma ve özelleştirme adımları anlatılmaktadır. Geliştirme aşamasındaki bir C# proje ile çalışmaya başlayın, kodunu çalıştıran testler oluşturun, testleri çalıştırın ve sonuçları inceleyin. Ardından proje kodunu değiştirin ve testleri yeniden çalıştırın.

## <a name="create-a-project-to-test"></a>Test etmek için bir proje oluşturun

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

2. **Dosya** menüsünde **Yeni** > **Proje**' yi seçin.

   **Yeni Proje** iletişim kutusu görünür.

3. **Visual C#**  .NET Core kategorisi altında konsol uygulaması (.NET Core) proje şablonunu seçin. >

4. Proje **bankasının**adını belirleyip **Tamam**' a tıklayın.

   Banka projesi oluşturulur ve kod düzenleyicisinde açık olan *program.cs* dosyası ile **Çözüm Gezgini** görüntülenir.

   > [!NOTE]
   > *Program.cs* düzenleyicide açık değilse, açmak için **Çözüm Gezgini** dosya *program.cs* dosyasına çift tıklayın.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın.

2. Başlangıç penceresinde **Yeni proje oluştur**' u seçin.

3. C# **Konsol uygulaması (.NET Core)** proje şablonunu arayıp seçin ve ardından **İleri**' ye tıklayın.

4. Proje **bankasının**adını, ardından **Oluştur**' a tıklayın.

   Banka projesi oluşturulur ve kod düzenleyicisinde açık olan *program.cs* dosyası ile **Çözüm Gezgini** görüntülenir.

   > [!NOTE]
   > *Program.cs* düzenleyicide açık değilse, açmak için **Çözüm Gezgini** dosya *program.cs* dosyasına çift tıklayın.

::: moniker-end

5. *Program.cs* Içeriğini, *BankAccount*sınıfını tanımlayan aşağıdaki C# kodla değiştirin:

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

6. Sağ tıklayıp **Çözüm Gezgini** **Yeniden Adlandır** ' ı seçerek dosyayı *BankAccount.cs* olarak yeniden adlandırın.

7. Üzerinde **derleme** menüsünde tıklatın **Çözümü Derle**.

Artık test edebilirsiniz yöntemleri olan bir projeniz var. Bu makalede, testler `Debit` yöntemine odaklanmaktadır. Bu `Debit` Yöntem para bir hesaptan geri geldiğinde çağrılır.

## <a name="create-a-unit-test-project"></a>Birim testi projesi oluşturma

1. **Dosya** menüsünde**Yeni proje** **Ekle** > ' yi seçin.

   > [!TIP]
   > Ayrıca **Çözüm Gezgini** çözüme sağ tıklayıp**Yeni proje** **Ekle** > ' yi seçebilirsiniz.

::: moniker range="vs-2017"

2. **Yeni proje** iletişim kutusunda, **yüklü**' ı genişletin, **görsel C#** ' i genişletin ve ardından **Test**' i seçin.

3. Şablonlar listesinden **MSTest test projesi (.NET Core)** seçeneğini belirleyin.

4. **Ad** kutusuna yazın `BankTests`ve ardından **Tamam**' ı seçin.

   **BankTests** projesi **Banka** çözümüne eklenir.

::: moniker-end

::: moniker range=">=vs-2019"

2. C# **MSTest test projesi (.NET Core)** proje şablonunu arayıp seçin ve ardından **İleri**' ye tıklayın.

3. Projeyi **BankTests**olarak adlandırın.

4.           **Oluştur**'a tıklayın.

   **BankTests** projesi **Banka** çözümüne eklenir.

::: moniker-end

5. **BankTests** projesinde, **Banka** projesine bir başvuru ekleyin.

   **Çözüm Gezgini**, **BankTests** projesi altındaki **Bağımlılıklar** ' ı seçin ve ardından sağ tıklama menüsünden **Başvuru Ekle** ' yi seçin.

6. **Başvuru Yöneticisi** iletişim kutusunda, **Projeler**' i genişletin, **çözüm**' ü seçin ve ardından **Banka** öğesini kontrol edin.

7. **Tamam**’ı seçin.

## <a name="create-the-test-class"></a>Test sınıfı oluşturma

`BankAccount` Sınıfı doğrulamak için bir test sınıfı oluşturun. Proje şablonu tarafından oluşturulan *UnitTest1.cs* dosyasını kullanabilir, ancak dosya ve sınıfa daha açıklayıcı adlar verebilirsiniz.

### <a name="rename-a-file-and-class"></a>Dosya ve sınıfı yeniden adlandırma

1. Dosyayı yeniden adlandırmak için, **Çözüm Gezgini**Içinde, BankTests projesindeki *UnitTest1.cs* dosyasını seçin. Sağ tıklama menüsünde, **Yeniden Adlandır**' ı seçin ve ardından dosyayı *BankAccountTests.cs*olarak yeniden adlandırın.

::: moniker range="vs-2017"

2. Sınıfı yeniden adlandırmak için, açılan iletişim kutusunda **Evet** ' i seçin ve ayrıca kod öğesine başvuruları yeniden adlandırmak isteyip istemediğinizi sorar.

::: moniker-end

::: moniker range=">=vs-2019"

2. Sınıfı yeniden adlandırmak için, imleci kod düzenleyicisinde üzerine `UnitTest1` konumlandırın, sağ tıklayın ve ardından **Yeniden Adlandır**' ı seçin. **BankAccountTests** yazın ve **ENTER**tuşuna basın.

::: moniker-end

*BankAccountTests.cs* dosyası artık aşağıdaki kodu içerir:

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

### <a name="add-a-using-statement"></a>Using deyimleri ekleme

Tam nitelikli adlar kullanmadan test kapsamındaki projeye çağrı yapabilmesi için test sınıfına bir [ `using` ifade](/dotnet/csharp/language-reference/keywords/using-statement) ekleyin. Sınıf dosyasının en üstünde şunu ekleyin:

```csharp
using BankAccountNS;
```

### <a name="test-class-requirements"></a>Test sınıfı gereksinimleri

Bir test sınıfı için en düşük gereksinimler şunlardır:

- Özniteliği `[TestClass]` , test Gezgini 'nde çalıştırmak istediğiniz birim testi yöntemlerini içeren herhangi bir sınıfta gereklidir.

- Test Gezgini 'nin tanımasını istediğiniz her test yönteminin `[TestMethod]` özniteliğine sahip olması gerekir.

`[TestClass]` Özniteliği olmayan bir birim testi projesinde başka sınıflarınız olabilir ve `[TestMethod]` özniteliği olmayan test sınıflarında başka yöntemlere sahip olabilirsiniz. Test yöntemlerinizin bu diğer sınıflarını ve yöntemlerini çağırabilirsiniz.

## <a name="create-the-first-test-method"></a>İlk test yöntemini oluşturma

Bu yordamda, `Debit` `BankAccount` sınıfının yönteminin davranışını doğrulamak için birim testi yöntemleri yazacaksınız.

Denetlenmesi gereken en az üç davranış vardır:

- Bu yöntem, borç <xref:System.ArgumentOutOfRangeException> tutarının bakiyesinden büyük olması halinde bir oluşturur.

- Bu yöntem, borç <xref:System.ArgumentOutOfRangeException> tutarının sıfırdan küçük olması halinde bir oluşturur.

- Borç miktarı geçerliyse, yöntemi hesap bakiyesinden borç tutarını çıkartır.

> [!TIP]
> Bu izlenecek yolda kullanmayacağından, varsayılan `TestMethod1` yöntemi silebilirsiniz.

### <a name="to-create-a-test-method"></a>Test yöntemi oluşturmak için

İlk test, geçerli bir tutarın (yani, hesap bakiyesi ve sıfırdan büyük bir değerden daha az), hesaptan doğru miktarı çizdiğini doğrular. Aşağıdaki yöntemi bu `BankAccountTests` sınıfa ekleyin:

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

Yöntemi basittir: bir başlangıç bakiyesine sahip yeni `BankAccount` bir nesne ayarlar ve ardından geçerli bir miktar çizer. Son Bakiyenin beklenen <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.AreEqual%2A?displayProperty=nameWithType> şekilde olduğunu doğrulamak için yöntemini kullanır.

### <a name="test-method-requirements"></a>Test yöntemi gereksinimleri

Bir test yönteminin aşağıdaki gereksinimleri karşılaması gerekir:

- Bu, `[TestMethod]` özniteliğiyle donatılmalıdır.

- Döndürür `void`.

- Parametrelere sahip olamaz.

## <a name="build-and-run-the-test"></a>Test oluşturun ve çalıştırın

1. **Build** menüsünde **Build Solution**öğesini seçin.

2. **Test Gezgini** açık değilse, üstteki menü çubuğundan**Windows** > **Test Gezgini** 'ni **Test** > et ' i seçerek açın.

3. Testi çalıştırmak için **Tümünü Çalıştır** ' ı seçin.

   Test çalışırken, **Test Gezgini** penceresinin üstündeki durum çubuğu canlandırılır. Test çalıştırmasının sonunda, tüm test yöntemleri başarılı olursa çubuk yeşile dönüşür veya testlerin herhangi biri başarısız olursa kırmızı olur.

   Bu durumda, test başarısız olur.

4. Pencerenin alt kısmındaki Ayrıntıları görüntülemek için **Test Gezgini** ' nde yöntemi seçin.

## <a name="fix-your-code-and-rerun-your-tests"></a>Kodunuzu düzeltemedi ve testlerinizi yeniden çalıştırın

Test sonucu, hatayı açıklayan bir ileti içerir. `AreEqual` Yöntemi için, ileti beklendiğini ve gerçekten alındığını gösterir. Bakiyenin azalmasını bekliyorduk, ancak bunun yerine çekme miktarı artar.

Birim testi bir hatayı kapsamıyor: geri al 'ın miktarı, kaldırılması gereken Hesap bakiyesine *eklenir* .

### <a name="correct-the-bug"></a>Hatayı düzeltin

Hatayı düzeltmek için, *BankAccount.cs* dosyasında şu satırı değiştirin:

```csharp
m_balance += amount;
```

kullanılarak

```csharp
m_balance -= amount;
```

### <a name="rerun-the-test"></a>Testi yeniden çalıştırın

**Test Gezgini**'nde testi yeniden **çalıştırmak için Tümünü Çalıştır** ' ı seçin. Kırmızı/yeşil çubuk, testin geçtiğini belirtmek için yeşile dönüşür.

![Başarılı testi gösteren Visual Studio 2019 ' de test Gezgini](media/test-explorer-banktests-passed.png)

## <a name="use-unit-tests-to-improve-your-code"></a>Kodunuzu geliştirmek için birim testlerini kullanın

Bu bölümde, yinelenen analiz, birim testi geliştirme ve yeniden düzenleme işlemlerinin üretim kodunuzu daha sağlam ve etkili hale getirmenize nasıl yardımcı olduğu açıklanır.

### <a name="analyze-the-issues"></a>Sorunları çözümleyin

Geçerli bir miktarın `Debit` yöntemde doğru şekilde kesildiğini onaylamak için bir test yöntemi oluşturdunuz. Şimdi, borç tutarının aşağıdakilerden biri olması durumunda <xref:System.ArgumentOutOfRangeException> yöntemin bir olduğunu doğrulayın:

- bakiyesinden büyük veya
- sıfırdan küçük.

### <a name="create-and-run-new-test-methods"></a>Yeni test yöntemleri oluştur ve Çalıştır

Borç miktarı sıfırdan küçükse doğru davranışı doğrulamak için bir test yöntemi oluşturun:

```csharp
[TestMethod]
public void Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange()
{
    // Arrange
    double beginningBalance = 11.99;
    double debitAmount = -100.00;
    BankAccount account = new BankAccount("Mr. Bryan Walton", beginningBalance);

    // Act and assert
    Assert.ThrowsException<System.ArgumentOutOfRangeException>(() => account.Debit(debitAmount));
}
```

Doğru özel durumun atılmışsa emin olmak için yönteminikullanın.<xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.ThrowsException%2A> Bu yöntem, bir <xref:System.ArgumentOutOfRangeException> oluşturulmadığı takdirde testin başarısız olmasına neden olur. Test altındaki yöntemi geçici olarak değiştirirseniz, borç miktarı sıfırdan küçükse, test <xref:System.ApplicationException> doğru bir şekilde&mdash;davranır, başarısız olur.

Geri kalan miktar bakiyesinden daha büyükse, büyük/küçük harf durumunu test etmek için aşağıdaki adımları uygulayın:

1. Adlı `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange`yeni bir test yöntemi oluşturun.

2. Yöntem gövdesini ' dan `Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange` yeni yönteme kopyalayın.

3. Sayısını bakiyesinden daha büyük bir sayı olarakayarlayın.`debitAmount`

İki testi çalıştırın ve bunların başarılı olduğunu doğrulayın.

### <a name="continue-the-analysis"></a>Analize devam edin

Test edilmekte olan yöntem daha fazla geliştirilebilir. Geçerli uygulamayla, test sırasında hangi koşulun (`amount > m_balance` veya `amount < 0`) atılmakta olduğunu belirlemenin bir yolu yoktur. Yönteminde bir `ArgumentOutOfRangeException` yerde oluşturulduğunu biliyoruz. Özel durumun hangi koşulla `BankAccount.Debit` kaynaklandığını (`amount > m_balance` veya `amount < 0`) söylediğimiz durumlarda, yöntemimizin bağımsız değişkenlerini doğru şekilde kontrol etmemiz konusunda emin olduğumuz için bu daha iyi olacaktır.

Test edilen yönteme (`BankAccount.Debit`) yeniden bakın ve her iki koşullu deyimin da bağımsız değişkenin adını parametre olarak alan bir `ArgumentOutOfRangeException` Oluşturucu kullandığına dikkat edin:

```csharp
throw new ArgumentOutOfRangeException("amount");
```

Daha zengin bilgilerin bulunduğu raporları kullanabileceğiniz bir Oluşturucu vardır: <xref:System.ArgumentOutOfRangeException.%23ctor(System.String,System.Object,System.String)> bağımsız değişkenin adını, bağımsız değişken değerini ve Kullanıcı tanımlı bir iletiyi içerir. Bu Oluşturucuyu kullanmak için test edilen yöntemi yeniden düzenleyebilirsiniz. Daha da iyisi, hataları belirtmek için genel kullanıma açık tür üyelerini kullanabilirsiniz.

### <a name="refactor-the-code-under-test"></a>Test altındaki kodu yeniden düzenleme

İlk olarak, sınıf kapsamındaki hata iletileri için iki sabit tanımlayın. Bunları test `BankAccount`edilen sınıfına yerleştirin:

```csharp
public const string DebitAmountExceedsBalanceMessage = "Debit amount exceeds balance";
public const string DebitAmountLessThanZeroMessage = "Debit amount is less than zero";
```

Ardından, `Debit` yönteminde iki koşullu deyimi değiştirin:

```csharp
if (amount > m_balance)
{
    throw new System.ArgumentOutOfRangeException("amount", amount, DebitAmountExceedsBalanceMessage);
}

if (amount < 0)
{
    throw new System.ArgumentOutOfRangeException("amount", amount, DebitAmountLessThanZeroMessage);
}
```

### <a name="refactor-the-test-methods"></a>Test yöntemlerini yeniden düzenleme

Çağrısını kaldırarak test yöntemlerini yeniden düzenleyin <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.ThrowsException%2A?displayProperty=nameWithType>. Çağrıyı `Debit()` bir`try/catch` blokta sarın, beklenen özel durumu yakalayın ve ilişkili iletisini doğrulayın. <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert.Contains%2A?displayProperty=fullName> Yöntemi iki dizeyi karşılaştırma yeteneği sağlar.

`Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange` Şimdi, şöyle görünebilir:

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
    catch (System.ArgumentOutOfRangeException e)
    {
        // Assert
        StringAssert.Contains(e.Message, BankAccount.DebitAmountExceedsBalanceMessage);
    }
}
```

### <a name="retest-rewrite-and-reanalyze"></a>Yeniden test etme, yeniden yazma ve yeniden çözümleme

Test edilen yöntemde bir hata olduğunu varsayın ve `Debit` yöntemin, özel durum ile doğru iletiyi <xref:System.ArgumentOutOfRangeException> hiçbir şekilde bir daha belirtmediğini hiçbir şekilde oluşturmadığını unutmayın. Şu anda, test yöntemi bu durumu işlemez. `debitAmount` Değer geçerliyse (yani, bakiyesinden daha küçüktür, ancak sıfırdan büyük), hiçbir özel durum yakalanmaz, bu nedenle onaylama hiçbir şekilde tetiklemeye devam eder. Henüz, test yöntemi geçer. Hiçbir özel durum atılmadığı takdirde test yönteminin başarısız olmasını istediğiniz için bu iyi değildir.

Bu, test yöntemindeki bir hatadır. Sorunu çözmek için, bir özel durumun <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.Fail%2A> oluşturulduğu durumu işlemek üzere test yönteminin sonuna bir onay ekleyin.

Testin yeniden çalıştırılması, doğru özel durum yakalanırsa testin artık *başarısız* olduğunu gösterir. Blok özel durumu yakalar, ancak yöntem yürütülmeye devam eder ve yeni <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert.Fail%2A> onaylama sırasında başarısız olur. `catch` Bu sorunu çözmek için, `return` `catch` bloktaki `StringAssert` öğesinden sonra bir ifade ekleyin. Testi yeniden çalıştırmak, bu sorunu düzelttik olduğunu onaylar. Öğesinin son sürümü şöyle `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange` görünür:

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
    catch (System.ArgumentOutOfRangeException e)
    {
        // Assert
        StringAssert.Contains(e.Message, BankAccount.DebitAmountExceedsBalanceMessage);
        return;
    }

    Assert.Fail("The expected exception was not thrown.");
}
```

### <a name="conclusion"></a>Sonuç

Test koduna yönelik iyileştirmeler daha sağlam ve bilgilendirici test yöntemlerine sahiptir. Ancak daha da önemlisi test altındaki kodu geliştirmiştir.

> [!TIP]
> Bu izlenecek yol, yönetilen kod için Microsoft birim testi çerçevesini kullanır. **Test Gezgini** , **Test Gezgini**için bağdaştırıcılara sahip üçüncü taraf birim testi çerçevelerinden testleri de çalıştırabilir. Daha fazla bilgi için [üçüncü taraf birim testi çerçevelerini yükleme](../test/install-third-party-unit-test-frameworks.md).

## <a name="see-also"></a>Ayrıca bkz.

Bir komut satırından testlerin nasıl çalıştırılacağı hakkında daha fazla bilgi için bkz. [VSTest. Console. exe komut satırı seçenekleri](vstest-console-options.md).
