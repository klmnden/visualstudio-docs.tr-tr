---
title: Kod kusurları için yönetilen kodu çözümlemek için İzlenecek yol | Microsoft Docs
ms.date: 01/29/2018
ms.topic: conceptual
helpviewer_keywords:
- code analysis [Visual Studio]
- managed code, analyzing
author: mikadumont
ms.author: midumont
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 4a00fdb2a41a03554113f2ecb626185aab2c74d5
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69548004"
---
# <a name="walkthrough-use-static-code-analysis-to-find-code-defects"></a>İzlenecek yol: Kod kusurlarını bulmak için statik Kod analizini kullanın

Bu kılavuzda, Eski Kod analizini kullanarak kod kusurları için yönetilen bir proje çözümleyebilirsiniz.

Bu makalede, .NET tarafından yönetilen kod derlemelerinizi .NET tasarım kılavuzlarından uyum sağlamak üzere çözümlemek için eski analizler kullanma sürecinde adım adım açıklanır.

## <a name="create-a-class-library"></a>Sınıf kitaplığı oluşturma

### <a name="to-create-a-class-library"></a>Bir sınıf kitaplığı oluşturmak için

1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**.

1. **Yeni proje** iletişim kutusunda, **yüklü** > **C#görsel**' i genişletin ve ardından **Windows Masaüstü**' ni seçin.

1. **Sınıf kitaplığı (.NET Framework)** şablonunu seçin.

1. **Ad** metin kutusuna **CodeAnalysisManagedDemo** yazın ve ardından **Tamam**' a tıklayın.

1. Proje oluşturulduktan sonra, *Class1.cs* dosyasını açın.

1. Class1.cs içindeki var olan metni şu kodla değiştirin:

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

## <a name="analyze-the-project"></a>Projeyi çözümle

### <a name="to-analyze-a-managed-project-for-code-defects"></a>Kod kusurları için yönetilen bir projeyi analiz etmek için

1. **Çözüm Gezgini**' de CodeAnalysisManagedDemo projesini seçin.

1. **Proje** menüsünde **Özellikler**' e tıklayın.

     CodeAnalysisManagedDemo özellikleri sayfası görüntülenir.

1. **Kod Analizi** sekmesini seçin.

1. **Derlemede Kod analizini etkinleştir '** in işaretli olduğundan emin olun.

1. **Bu kural kümesini Çalıştır** açılan listesinden **Microsoft tüm kurallar**' ı seçin.

1. **Dosya** menüsünde, **Seçili öğeleri kaydet**' e tıklayın ve ardından Özellikler sayfalarını kapatın.

1. **Build** menüsünde **CodeAnalysisManagedDemo oluştur**' a tıklayın.

    CodeAnalysisManagedDemo proje derleme uyarıları **hata listesi** ve **Çıkış** penceresinde gösterilir.

## <a name="correct-the-code-analysis-issues"></a>Kod Analizi sorunlarını düzeltin

### <a name="to-correct-code-analysis-rule-violations"></a>Kod analizi kural ihlallerini düzeltmek için

1. **Görünüm** menüsünde **hata listesi**' yi seçin.

    Seçtiğiniz geliştirici profiline bağlı olarak, **Görünüm** menüsünde **diğer pencereler** ' i işaret etmeniz ve ardından **hata listesi**' yi seçmeniz gerekebilir.

1. **Çözüm Gezgini**, **tüm dosyaları göster**' i seçin.

1. Özellikler düğümünü genişletin ve ardından *AssemblyInfo.cs* dosyasını açın.

1. Uyarıları düzeltmek için aşağıdaki ipuçlarını kullanın:

   [CA1014 Derlemeleri CLSCompliantAttribute](../code-quality/ca1014-mark-assemblies-with-clscompliantattribute.md)ile işaretle: Microsoft. Design: ' demo ', CLSCompliantAttribute ile işaretlenmelidir ve değeri true olmalıdır.

   1. Kodu `using System;` AssemblyInfo.cs dosyasına ekleyin.

   1. Sonra, kodu `[assembly: CLSCompliant(true)]` AssemblyInfo.cs dosyasının sonuna ekleyin.

   [CA1032 Standart özel durum oluşturucularını](../code-quality/ca1032-implement-standard-exception-constructors.md)Uygula: Microsoft. Design: Aşağıdaki oluşturucuyu bu sınıfa ekleyin: Genel Tanıtım (dize)

   1. Oluşturucuyu `public demo (String s) : base(s) { }` sınıfına`demo`ekleyin.

   [CA1032 Standart özel durum oluşturucularını](../code-quality/ca1032-implement-standard-exception-constructors.md)Uygula: Microsoft. Design: Şu oluşturucuyu bu sınıfa ekleyin: public demo (dize, özel durum)

   1. Oluşturucuyu `public demo (String s, Exception e) : base(s, e) { }` sınıfına`demo`ekleyin.

   [CA1032 Standart özel durum oluşturucularını](../code-quality/ca1032-implement-standard-exception-constructors.md)Uygula: Microsoft. Design: Şu oluşturucuyu bu sınıfa ekleyin: protected demo (SerializationInfo, StreamingContext)

   1. Kodu `using System.Runtime.Serialization;` Class1.cs dosyasının başına ekleyin.

   1. Sonra, oluşturucuyu ekleyin`protected demo (SerializationInfo info, StreamingContext context) : base(info, context) { } to the class demo.`

   [CA1032 Standart özel durum oluşturucularını](../code-quality/ca1032-implement-standard-exception-constructors.md)Uygula: Microsoft. Design: Aşağıdaki oluşturucuyu bu sınıfa ekleyin: public demo ()

   1. Oluşturucuyu `public demo () : base() { }` sınıfına `demo`ekleyin **.**

   [CA1709 Tanımlayıcılar doğru](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)olmalıdır: Microsoft. Naming: ' TestCode ' ad alanı adının büyük küçük harflerini ' TestCode ' ile değiştirerek düzeltin.

   1. Ad alanının `testCode` büyük küçük harflerini olarak `TestCode`değiştirin.

   [CA1709 Tanımlayıcılar doğru](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)olmalıdır: Microsoft. Naming: ' Demo ' ad alanının büyük küçük harflerini ' demo ' ile değiştirerek düzeltin.

   1. Üyenin adını olarak `Demo`değiştirin.

   [CA1709 Tanımlayıcılar doğru](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)olmalıdır: Microsoft. Naming: ' İtem ' üye adının büyük küçük harflerini ' öğe ' ile değiştirerek düzeltin.

   1. Üyenin adını olarak `Item`değiştirin.

   [CA1710 Tanımlayıcılar doğru sonekine](../code-quality/ca1710-identifiers-should-have-correct-suffix.md)sahip olmalıdır: Microsoft. Naming: ' TestCode. Demo ' öğesini ' Exception ' ile sona erdirmek için yeniden adlandırın.

   1. Sınıfının ve oluşturucularının adını olarak `DemoException`değiştirin.

   [CA2210 Derlemelerin geçerli tanımlayıcı adları](../code-quality/ca2210-assemblies-should-have-valid-strong-names.md)olmalıdır: ' CodeAnalysisManagedDemo ' öğesini bir tanımlayıcı ad anahtarıyla imzalayın.

   1. **Proje** menüsünde **CodeAnalysisManagedDemo özellikleri**' ni seçin.

      Proje özellikleri görüntülenir.

   1. **İmzalama** sekmesini seçin.

   1. **Derlemeyi imzala** onay kutusunu seçin.

   1. **Bir dize adı seçin anahtar dosyası** listesinde  **\<yeni... öğesini seçin. >** .

      **Tanımlayıcı ad anahtarı oluştur** iletişim kutusu görüntülenir.

   1. **Anahtar dosya adı**' nda, TestKey yazın.

   1. Bir parola girin ve **Tamam**' ı seçin.

   1. **Dosya** menüsünde, **Seçili öğeleri kaydet**' i seçin ve sonra özellik sayfalarını kapatın.

   [CA2237 ISerializable türlerini SerializableAttribute](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)ile işaretleyin: Microsoft. Usage: Bu tür ISerializable uyguladığından ' demo ' türüne [Serializable] özniteliği ekleyin.

   1. `[Serializable ()]` Özniteliğini sınıfına`demo`ekleyin.

   Değişiklikleri tamamladıktan sonra, Class1.cs dosyası aşağıdaki gibi görünmelidir:

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

## <a name="exclude-code-analysis-warnings"></a>Kod Analizi uyarılarını hariç tut

1. Kalan uyarıların her biri için aşağıdakileri yapın:

    1. **Hata listesi**uyarıyı seçin.

    1. Sağ tıklama menüsünde (bağlam menüsü),**gizleme dosyasında** **Gizle** > ' yi seçin.

1. Projeyi yeniden derleyin.

     Proje herhangi bir uyarı veya hata olmadan oluşturulur.

## <a name="see-also"></a>Ayrıca bkz.

[Yönetilen kod için kod analizi](../code-quality/code-analysis-for-managed-code-overview.md)