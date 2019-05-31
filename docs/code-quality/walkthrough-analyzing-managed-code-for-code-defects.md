---
title: Kod kusurları için yönetilen kod gözden geçirme analiz etme | Microsoft Docs
ms.date: 01/29/2018
ms.topic: conceptual
helpviewer_keywords:
- code analysis [Visual Studio]
- managed code, analyzing
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 3097e52f99f044257b8eaf634455bdf19978d0c3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62825049"
---
# <a name="walkthrough-analyzing-managed-code-for-code-defects"></a>İzlenecek yol: Kod kusurları için yönetilen kodu analiz etme

Bu izlenecek yolda Kod Analizi aracını kullanarak kod kusurları için yönetilen bir proje analiz.

Bu kılavuzda, Microsoft .NET Framework tasarım yönergeleri ile uyumluluk için bütünleştirilmiş kodlarınızı .NET yönetilen kodu analiz etmek için kod analizini kullanarak işleminin adım gösterilir.

## <a name="create-a-class-library"></a>Bir sınıf kitaplığı oluşturma

### <a name="to-create-a-class-library"></a>Bir sınıf kitaplığı oluşturmak için

1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**.

1. İçinde **yeni proje** iletişim kutusunda **yüklü** > **Visual C#** ve ardından **Windows Masaüstü**.

1. Seçin **sınıf kitaplığı (.NET Framework)** şablonu.

1. İçinde **adı** metin kutusunda, **CodeAnalysisManagedDemo** ve ardından **Tamam**.

1. Proje oluşturulduktan sonra açın *Class1.cs* dosya.

1. Class1.cs varolan metni, aşağıdaki kodla değiştirin:

   ```csharp
   using System;

   namespace testCode
   {
       public class demo : Exception
       {
           public static void Initialize(int size) { }
           protected static readonly int _item;
           public static int item { get { return _item; } }
       }
   }
   ```

1. Class1.cs dosyasını kaydedin.

## <a name="analyze-the-project"></a>Projeyi Çözümle

### <a name="to-analyze-a-managed-project-for-code-defects"></a>Kod kusurları için yönetilen bir projesini analiz etmek için

1. CodeAnalysisManagedDemo projede seçin **Çözüm Gezgini**.

1. Üzerinde **proje** menüsünü tıklatın **özellikleri**.

     CodeAnalysisManagedDemo Özellikler sayfası görüntülenir.

1. Seçin **Kod Analizi** sekmesi.

1. Emin olun **derlemede kod analizini etkinleştir** denetlenir.

1. Gelen **bu kural kümesini Çalıştır** aşağı açılan listesinden **Microsoft tüm kurallar**.

1. Üzerinde **dosya** menüsünde tıklayın **seçili öğeleri Kaydet**ve ardından Özellikler pencerelerini kapatın.

1. Üzerinde **derleme** menüsünde tıklatın **derleme CodeAnalysisManagedDemo**.

    CodeAnalysisManagedDemo proje derleme uyarıları gösterilir **hata listesi** ve **çıkış** windows.

## <a name="correct-the-code-analysis-issues"></a>Kod Analizi sorunlarını düzeltin

### <a name="to-correct-code-analysis-rule-violations"></a>Kod Analizi kural ihlallerini düzeltmek üzere

1. Üzerinde **görünümü** menüsünde seçin **hata listesi**.

    Seçtiğiniz Geliştirici profili bağlı olarak, işaret gerekebilir **diğer Windows** üzerinde **görünümü** menüsünde ve ardından **hata listesi**.

1. İçinde **Çözüm Gezgini**, seçin **tüm dosyaları göster**.

1. Özellikler düğümü genişletin ve ardından açın *AssemblyInfo.cs* dosya.

1. Uyarıları gidermek için aşağıdaki ipuçlarını kullanın:

   [CA1014: Derlemeleri CLSCompliantAttribute ile işaretle](../code-quality/ca1014-mark-assemblies-with-clscompliantattribute.md): CLSCompliantAttribute ile işaretlenmelidir Microsoft.Design: 'Tanıtım' ve değeri true olmalıdır.

   1. Kod ekleme `using System;` AssemblyInfo.cs dosyası için.

   1. Ardından, kod ekleme `[assembly: CLSCompliant(true)]` AssemblyInfo.cs dosyasını sonuna.

   [CA1032: Standart özel durum oluşturucuları uygulayın](../code-quality/ca1032-implement-standard-exception-constructors.md): Microsoft.Design: Bu sınıfına aşağıdaki oluşturucuyu ekleyin: Genel demo(String)

   1. Oluşturucu Ekle `public demo (String s) : base(s) { }` sınıfa `demo`.

   [CA1032: Standart özel durum oluşturucuları uygulayın](../code-quality/ca1032-implement-standard-exception-constructors.md): Microsoft.Design: Bu sınıfına aşağıdaki oluşturucuyu ekleyin: Genel Tanıtım (dize, özel durum)

   1. Oluşturucu Ekle `public demo (String s, Exception e) : base(s, e) { }` sınıfa `demo`.

   [CA1032: Standart özel durum oluşturucuları uygulayın](../code-quality/ca1032-implement-standard-exception-constructors.md): Microsoft.Design: Bu sınıfına aşağıdaki oluşturucuyu ekleyin: tanıtım (SerializationInfo, StreamingContext) korumalı

   1. Kod ekleme `using System.Runtime.Serialization;` Class1.cs dosyasının başına.

   1. Ardından, oluşturucu Ekle `protected demo (SerializationInfo info, StreamingContext context) : base(info, context) { } to the class demo.`

   [CA1032: Standart özel durum oluşturucuları uygulayın](../code-quality/ca1032-implement-standard-exception-constructors.md): Microsoft.Design: Bu sınıfına aşağıdaki oluşturucuyu ekleyin: Genel demo()

   1. Oluşturucu Ekle `public demo () : base() { }` sınıfa `demo` **.**

   [CA1709: Tanımlayıcıları büyük/küçük harfleri doğru](../code-quality/ca1709-identifiers-should-be-cased-correctly.md): Microsoft.Naming: 'TestCode için' değiştirerek ad alanı adı 'testCode' büyük küçük harfleri düzeltin.

   1. Ad alanı büyük küçük harfleri değiştirme `testCode` için `TestCode`.

   [CA1709: Tanımlayıcıları büyük/küçük harfleri doğru](../code-quality/ca1709-identifiers-should-be-cased-correctly.md): Microsoft.Naming: 'Tanıtıma' değiştirerek tür adı 'Tanıtım' büyük küçük harfleri düzeltin.

   1. Üye adını değiştirmek `Demo`.

   [CA1709: Tanımlayıcıları büyük/küçük harfleri doğru](../code-quality/ca1709-identifiers-should-be-cased-correctly.md): Microsoft.Naming: 'Öğesine' değiştirerek üyesi adı 'öğesini' büyük küçük harfleri düzeltin.

   1. Üye adını değiştirmek `Item`.

   [CA1710: Tanımlayıcılar doğru soneki olmalıdır](../code-quality/ca1710-identifiers-should-have-correct-suffix.md): Microsoft.Naming: 'TestCode.demo' end 'Özel durum' içinde yeniden adlandırın.

   1. Sınıfı için kendi oluşturucular adını değiştirip `DemoException`.

   [CA2210: Derlemelerin geçerli tanımlayıcı adları olmalıdır](../code-quality/ca2210-assemblies-should-have-valid-strong-names.md): 'CodeAnalysisManagedDemo' bir tanımlayıcı ad anahtarıyla imzalayın.

   1. Üzerinde **proje** menüsünde seçin **CodeAnalysisManagedDemo özellikleri**.

      Proje özellikleri görüntülenir.

   1. Seçin **imzalama** sekmesi.

   1. Seçin **derlemeyi imzalamayı** onay kutusu.

   1. İçinde **dize ad anahtar dosyası seç** listesinden  **\<yeni … >** .

      **Katı ad anahtarı oluştur** iletişim kutusu görüntülenir.

   1. İçinde **anahtar dosya adını**, TestKey yazın.

   1. Bir parola girin ve ardından **Tamam**.

   1. Üzerinde **dosya** menüsünde seçin **seçili öğeleri Kaydet**ve özellik sayfaları kapatın.

   [CA2237: İşareti ISerializable türleri SerializableAttribute ile](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md): Microsoft.Usage: Bu türü ISerializable uyguladığı 'gösteri' türüne [Serializable] özniteliğini ekleyin.

   1. Ekleme `[Serializable ()]` öznitelik sınıfına `demo`.

   Değişiklikleri tamamladıktan sonra Class1.cs dosyasını aşağıdaki gibi görünmelidir:

   ```csharp
   using System;
   using System.Runtime.Serialization;

   namespace TestCode
   {
       [Serializable()]
       public class DemoException : Exception
       {
           public DemoException () : base() { }
           public DemoException(String s) : base(s) { }
           public DemoException(String s, Exception e) : base(s, e) { }
           protected DemoException(SerializationInfo info, StreamingContext context) : base(info, context) { }

           public static void Initialize(int size) { }
           protected static readonly int _item;
           public static int Item { get { return _item; } }
       }
   }
   ```

1. Projeyi yeniden derleyin.

## <a name="exclude-code-analysis-warnings"></a>Kod Analizi Uyarıları hariç tut

1. Her kalan uyarılar için aşağıdakileri yapın:

    1. Uyarıyı seçin **hata listesi**.

    1. (Bağlam menüsü) sağ tıklama menüsünden seçin **bastır** > **gizleme dosyası içinde**.

1. Projeyi yeniden derleyin.

     Projeyi herhangi bir uyarı veya hata derler.

## <a name="see-also"></a>Ayrıca bkz.

[Yönetilen kod için Kod Analizi](../code-quality/code-analysis-for-managed-code-overview.md)