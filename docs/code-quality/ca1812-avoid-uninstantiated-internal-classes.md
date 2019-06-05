---
title: 'CA1812: Örneklenmemiş iç sınıflardan kaçının'
ms.date: 05/16/2019
ms.topic: reference
f1_keywords:
- CA1812
- AvoidUninstantiatedInternalClasses
helpviewer_keywords:
- AvoidUninstantiatedInternalClasses
- CA1812
ms.assetid: 1bb92a42-322a-44cc-98a8-8858212c1e1f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a0d55af3c5522c6bb9aa3ad8a023f070c187ca6f
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66714259"
---
# <a name="ca1812-avoid-uninstantiated-internal-classes"></a>CA1812: Örneklenmemiş iç sınıflardan kaçının

|||
|-|-|
|TypeName|AvoidUninstantiatedInternalClasses|
|CheckId|CA1812|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Hiç örneklenmemiş bir iç (derleme düzeyi) türü.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, bir tür oluşturucular bir çağrı bulmaya çalışır ve hiçbir çağrı bulunursa bir ihlali raporlar.

Aşağıdaki türleri bu kural tarafından incelenir değil:

- Değer türleri

- Soyut türler

- Numaralandırmalar

- Temsilciler

- Derleyici yayılan dizi türleri

- Olamaz başlatılamaz ve yalnızca tanımlayan türler [ `static` ](/dotnet/csharp/language-reference/keywords/static) ([ `Shared` Visual Basic'te](/dotnet/visual-basic/language-reference/modifiers/shared)) yöntemleri.

Uygularsanız, <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?displayProperty=fullName> analiz ediliyor. derleme için bu kural olarak işaretlenmiş türler işaretlemez [ `internal` ](/dotnet/csharp/language-reference/keywords/internal) ([ `Friend` Visual Basic'te](/dotnet/visual-basic/language-reference/modifiers/friend)) çünkü bir alan olabilir friend derlemesi tarafından kullanılır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için türünü kaldırmak veya onu kullanan kodu ekleyin. Türü yalnızca içeriyorsa `static` yöntemleri, derleyici varsayılan bir ortak örnek oluşturucusu yayma gelen önlemek için türü için aşağıdakilerden birini ekleyin:

- `static` Değiştiricisini C# hedefleyen türleri [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)] veya üzeri.

- .NET Framework sürümleri 1.0 ve 1.1 hedef türleri için özel bir oluşturucu.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan bir uyarıyı bastırmak güvenlidir. Aşağıdaki durumlarda bu uyarının gösterilmemesi gerektiğini öneririz:

- Sınıfı gibi geç bağlanan yansıma yöntemleri ile oluşturulan <xref:System.Activator.CreateInstance%2A?displayProperty=fullName>.

- Sınıf, ASP.NET ve çalışma zamanı tarafından otomatik olarak oluşturulur. Uygulayan bazı örnekler otomatik olarak oluşturulan sınıfların olanlardır <xref:System.Configuration.IConfigurationSectionHandler?displayProperty=fullName> veya <xref:System.Web.IHttpHandler?displayProperty=fullName>.

- Sınıf olan bir tür parametresi geçirilir bir [ `new` kısıtlaması](/dotnet/csharp/language-reference/keywords/new-constraint). Aşağıdaki örnek, kural tarafından CA1812 işaretlenir:

    ```csharp
    internal class MyClass
    {
        public DoSomething()
        {
        }
    }
    public class MyGeneric<T> where T : new()
    {
        public T Create()
        {
            return new T();
        }
    }

    MyGeneric<MyClass> mc = new MyGeneric<MyClass>();
    mc.Create();
    ```

## <a name="related-rules"></a>İlgili kuralları

- [CA1811: Çağrılmayan özel kodlardan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)
- [CA1801: Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)
- [CA1804: Kullanılmayan yerel öğeleri kaldırın](../code-quality/ca1804-remove-unused-locals.md)