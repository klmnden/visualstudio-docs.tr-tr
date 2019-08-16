---
title: Kod Analizi uyarılarını gösterme
ms.date: 12/01/2018
ms.topic: conceptual
helpviewer_keywords:
- source suppression, code analysis
- code analysis, source suppression
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
- CPP
ms.workload:
- multiple
ms.openlocfilehash: 60fcb13c978d614d40964bd8d6da21e8cf41f00f
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551079"
---
# <a name="suppress-code-analysis-warnings"></a>Kod Analizi uyarılarını gösterme

Bir uyarının geçerli olmadığını göstermek için genellikle yararlı olur. Bu, takım üyelerinin kodun gözden geçirdiğini ve uyarının bastırılamayacağını gösterir. Kaynak içi gizleme (ISS), <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> bir uyarının gösterilmemesi için özniteliğini kullanır. Özniteliği, uyarıyı oluşturan kod kesimine yakın şekilde yerleştirilebilir. <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> Özniteliği içine yazarak kaynak dosyasına ekleyebilir veya **hata listesi** kısayol menüsünü otomatik olarak eklemek için bir uyarı üzerinde kullanabilirsiniz.

<xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> Özniteliği, yönetilen kod derlemelerinizin Il meta verilerine dahil olan ve derleme zamanında CODE_ANALYSIS derleme sembolü tanımlanırsa koşullu bir özniteliktir.

C++/CLI ' da, özniteliği eklemek için\_, üstbilgi dosyasındaki makrolar\_CA\_'sı\_iletisini veya CA genel SUPPRESS_MESSAGE ' ı kullanın.

> [!NOTE]
> Kaynak gizleme verilerinin yanlışlıkla serbest bırakılmasını engellemek için sürüm yapılarında kaynak üzerinde gizlemeleri kullanmamalısınız. Ayrıca, kaynak içi göstermeme işleminin işlem maliyeti nedeniyle uygulamanızın performansı düşebilir.

> [!NOTE]
> Bir projeyi Visual Studio 2017 veya Visual Studio 2019 ' e geçirirseniz, çok sayıda kod analizi uyarısıyla aniden karşılaşabilirsiniz. Uyarıları gidermeye hazırsanız, > **çalışma kodu analizini çözümle ve etkin sorunları Gizle**' yi seçerek bunların tümününgörüntülenmesini sağlayabilirsiniz.
>
> ![Visual Studio 'da Kod analizini çalıştırma ve sorunları gösterme](media/suppress-active-issues.png)

## <a name="suppressmessage-attribute"></a>SuppressMessage özniteliği

**Hata listesi**bir kod analizi uyarısında bağlam veya sağ tıklama menüsünden **Gizle** ' yi seçtiğinizde, kodunuzda veya projenin Global gizleme dosyasına <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> bir öznitelik eklenir.

<xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> Özniteliği aşağıdaki biçimdedir:

```vb
<Scope:SuppressMessage("Rule Category", "Rule Id", Justification = "Justification", MessageId = "MessageId", Scope = "Scope", Target = "Target")>
```

```csharp
[Scope:SuppressMessage("Rule Category", "Rule Id", Justification = "Justification", MessageId = "MessageId", Scope = "Scope", Target = "Target")]
```

```cpp
CA_SUPPRESS_MESSAGE("Rule Category", "Rule Id", Justification = "Justification", MessageId = "MessageId", Scope = "Scope", Target = "Target")
```

Özniteliğin özellikleri şunları içerir:

- **Kategori** -kuralın tanımlandığı kategori. Kod analizi kural kategorileri hakkında daha fazla bilgi için bkz. [yönetilen kod uyarıları](../code-quality/code-analysis-for-managed-code-warnings.md).

- **CheckId** -kuralın tanımlayıcısı. Destek, kural tanımlayıcısı için hem kısa hem de uzun bir ad içerir. Kısa ad CAXXXX; Long adı CAXXXX:

- **Bloklama** -iletinin nasıl bastırılamamasının nedenini belgelemek için kullanılan metin.

- **MessageID** -her ileti için bir sorunun benzersiz tanıtıcısı.

- **Scope** -uyarının gizlendiği hedef. Hedef belirtilmemişse, özniteliğinin hedefine ayarlanır. Desteklenen [kapsamlar](xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Scope) şunları içerir:

  - `module`

  - `resource`

  - `type`

  - `member`

  - `namespace`-Bu kapsam, ad alanının kendisiyle karşı uyarıları göstermez. Ad uzayı içindeki türlere karşı uyarıları göstermez.

  - `namespaceanddescendants`-(Visual Studio 2019 için yeni) bu kapsam, bir ad alanındaki ve tüm alt simgelerinin uyarılarını bastırır. `namespaceanddescendants` Değer eski analiz tarafından yok sayılır.

- **Target** -uyarının bastırılmakta olduğu hedefi belirtmek için kullanılan bir tanımlayıcı. Tam nitelikli bir öğe adı içermelidir.

## <a name="suppressmessage-usage"></a>SuppressMessage kullanımı

Kod Analizi uyarıları, <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> özniteliğin uygulandığı düzeyde bastırılır. Örneğin, öznitelik derleme, modül, tür, üye veya parametre düzeyinde uygulanabilir. Bunun amacı, gizleme bilgilerinin ihlalin gerçekleştiği koda sıkı bir şekilde tam olarak daha katı bir biçimde.

Gizleme 'nin Genel biçimi kural kategorisini ve kural adının isteğe bağlı olarak okunabilir bir gösterimini içeren bir kural tanımlayıcısını içerir. Örneğin:

`[SuppressMessage("Microsoft.Design", "CA1039:ListsAreStrongTyped")]`

Kaynak gizleme gizleme meta verilerini en aza indirmek için kesin performans nedenleriyle, kural adı atlanabilir. Kural kategorisi ve kural KIMLIĞI birlikte yeterince benzersiz bir kural tanımlayıcısı oluşturur. Örneğin:

`[SuppressMessage("Microsoft.Design", "CA1039")]`

Bakım nedenleriyle, kural adının atlanması önerilmez.

## <a name="suppress-selective-violations-within-a-method-body"></a>Yöntem gövdesinde seçmeli ihlalleri gösterme

Gizleme öznitelikleri bir yönteme uygulanabilir, ancak bir yöntem gövdesi içine Katıştırılamaz. Bu, yöntemine <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> özniteliğini eklediğinizde belirli bir kuralın tüm ihlallerinin gizlendiği anlamına gelir.

Bazı durumlarda, örneğin, gelecekteki kodun kod analizi kuralından otomatik olarak muaf olmaması gibi, ihlalin belirli bir örneğini bastırmak isteyebilirsiniz. Belirli kod analizi kuralları, `MessageId` <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> bu özelliği özniteliğin özelliğini kullanarak yapmanıza olanak sağlar. Genel olarak, belirli bir sembolde (yerel bir değişken veya parametre) ihlal için eski kurallar `MessageId` özelliğe göre yapılır. [CA1500: VariableNamesShouldNotMatchFieldNames](../code-quality/ca1500-variable-names-should-not-match-field-names.md) , böyle bir kurala bir örnektir. Ancak, yürütülebilir koddaki (simge dışı) ihlaller için eski kurallar `MessageId` özelliğe uymaz. Ayrıca, .net Compiler platform ("Roslyn") Çözümleyicileri, `MessageId` özelliği dikkate vermez.

Bir kuralın belirli bir sembol ihlalini engellemek için, `MessageId` <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute> özniteliğin özelliğinin sembol adını belirtin. Aşağıdaki örnek,&mdash; `name` değişken`age` için bir tane olmak üzere [CA1500: variablenamesshouldnotmatchfieldnames](../code-quality/ca1500-variable-names-should-not-match-field-names.md)için iki ihlal içeren kodu gösterir. Yalnızca `age` sembol ihlali bastırılır.

```vb
Public Class Animal
    Dim age As Integer
    Dim name As String

    <CodeAnalysis.SuppressMessage("Microsoft.Maintainability", "CA1500:VariableNamesShouldNotMatchFieldNames", MessageId:="age")>
    Sub PrintInfo()
        Dim age As Integer = 5
        Dim name As String = "Charlie"

        Console.WriteLine("Age {0}, Name {1}", age, name)
    End Sub

End Class
```

```csharp
public class Animal
{
    int age;
    string name;

    [System.Diagnostics.CodeAnalysis.SuppressMessage("Microsoft.Maintainability", "CA1500:VariableNamesShouldNotMatchFieldNames", MessageId = "age")]
    private void PrintInfo()
    {
        int age = 5;
        string name = "Charlie";

        Console.WriteLine($"Age {age}, Name {name}");
    }
}
```

## <a name="generated-code"></a>Oluşturulan kod

Yönetilen kod derleyicileri ve bazı üçüncü taraf araçları, hızlı kod geliştirmeyi kolaylaştırmak için kod üretir. Kaynak dosyalarda görünen derleyici tarafından oluşturulan kod genellikle `GeneratedCodeAttribute` özniteliğiyle işaretlenir.

Kod Analizi uyarılarını ve oluşturulan kod için hataları bastırıp bastırmayacağını seçebilirsiniz. Bu tür uyarıları ve hataları gösterme hakkında daha fazla bilgi için bkz [. nasıl yapılır: Oluşturulan kod](../code-quality/how-to-suppress-code-analysis-warnings-for-generated-code.md)uyarılarını gizleyin.

> [!NOTE]
> Kod Analizi, `GeneratedCodeAttribute` bir derlemenin tamamına veya tek bir parametreye uygulandığında yok sayılır.

## <a name="global-level-suppressions"></a>Küresel düzeyde gizlemeler

Yönetilen Kod Analizi Aracı derleme, `SuppressMessage` modül, tür, üye veya parametre düzeyinde uygulanan öznitelikleri inceler. Ayrıca, kaynaklara ve ad alanlarına karşı ihlalleri da tetikler. Bu ihlallerin genel düzeyde uygulanması ve kapsamı belirlenmiş ve hedeflenmiş olması gerekir. Örneğin, aşağıdaki ileti bir ad alanı ihlalini bastırır:

`[module: SuppressMessage("Microsoft.Design", "CA1020:AvoidNamespacesWithFewTypes", Scope = "namespace", Target = "MyNamespace")]`

> [!NOTE]
> Kapsamla ilgili `namespace` bir uyarıyı bastırdığınızda, bu uyarı ad alanının kendisine karşı bastırır. Ad uzayı içindeki türlere karşı uyarıyı göstermez.

Herhangi bir gizleme açık bir kapsam belirtilerek ifade edilebilir. Bu gizlemeler küresel düzeyde canlı olmalıdır. Bir tür dekorasyon yaparak üye düzeyinde gizleme belirtemezsiniz.

Genel düzey gizlemeler, açıkça sağlanmış Kullanıcı kaynağıyla eşleşmeyen derleyici tarafından üretilen koda başvuran iletileri göstermenin tek yoludur. Örneğin, aşağıdaki kod derleyiciye yayılan bir oluşturucuya karşı bir ihlalin bastırır:

`[module: SuppressMessage("Microsoft.Design", "CA1055:AbstractTypesDoNotHavePublicConstructors", Scope="member", Target="Microsoft.Tools.FxCop.Type..ctor()")]`

> [!NOTE]
> `Target`her zaman tam öğe adını içerir.

## <a name="global-suppression-file"></a>Genel gizleme dosyası

Genel gizleme dosyası, bir hedef belirtmeyen küresel düzeyde gizlemeler veya gizlemeleri olan gizlemeleri korur. Örneğin, derleme düzeyi ihlallerin gizlemeleri bu dosyada depolanır. Ayrıca, bir form arkasındaki kod için proje düzeyi ayarları kullanılamadığından bazı ASP.NET gizlemeleri bu dosyada depolanır. **Hata listesi** penceresinde **Gizle** komutunun **Proje gizleme dosyasını** ilk kez seçtiğinizde, genel bir gizleme dosyası oluşturulur ve projenize eklenir.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Diagnostics.CodeAnalysis.SuppressMessageAttribute.Scope>
- <xref:System.Diagnostics.CodeAnalysis>
- [Kod Çözümleyicileri kullanma](../code-quality/use-roslyn-analyzers.md)
