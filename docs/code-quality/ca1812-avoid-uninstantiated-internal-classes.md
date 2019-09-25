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
ms.openlocfilehash: f924e9530a7ee43ec2222366141c3af6be2efc29
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233606"
---
# <a name="ca1812-avoid-uninstantiated-internal-classes"></a>CA1812: Örneklenmemiş iç sınıflardan kaçının

|||
|-|-|
|TypeName|AvoidUninstantiatedInternalClasses|
|CheckId|CA1812|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

İç (derleme düzeyi) türü hiçbir şekilde örneklenemez.

## <a name="rule-description"></a>Kural açıklaması

Bu kural, türün oluşturucularından birine yönelik çağrıyı bulmaya çalışır ve hiçbir çağrı bulunmazsa bir ihlalin bildirir.

Aşağıdaki türler bu kural tarafından incelendi:

- Değer türleri

- Soyut türler

- Numaralandırmalar

- Temsilciler

- Derleyicinin yayınlaması dizi türleri

- Örneklenemez ve yalnızca [`static`](/dotnet/csharp/language-reference/keywords/static) ([ `Shared` Visual Basic](/dotnet/visual-basic/language-reference/modifiers/shared)) yöntemlerinde tanımlanmış olan türler.

' I çözümlenmekte <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?displayProperty=fullName> olan derlemeye uygularsanız, bir alan bir Friend derlemesi tarafından kullanılabilir olduğundan, bu kural ([ `Friend` Visual Basic](/dotnet/visual-basic/language-reference/modifiers/friend)) [`internal`](/dotnet/csharp/language-reference/keywords/internal) olarak işaretlenen türlere bayrak uygulamaz.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, türü kaldırın veya onu kullanan kodu ekleyin. Tür yalnızca `static` Yöntemler içeriyorsa, derleyicinin varsayılan bir ortak örnek Oluşturucu yaymasını engellemek için aşağıdaki birini türüne ekleyin:

- .NET Framework 2,0 veya C# sonraki bir sürümü hedefleyen türler için değiştirici.`static`

- 1,0 ve 1,1 sürümlerini .NET Framework hedefleyen türler için özel Oluşturucu.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek güvenlidir. Aşağıdaki durumlarda bu uyarıyı bastırmalarını öneririz:

- Sınıfı, gibi geç bağlantılı yansıma yöntemleriyle <xref:System.Activator.CreateInstance%2A?displayProperty=fullName>oluşturulur.

- Sınıf, çalışma zamanı veya ASP.NET tarafından otomatik olarak oluşturulur. Otomatik olarak oluşturulan sınıfların bazı örnekleri, veya <xref:System.Configuration.IConfigurationSectionHandler?displayProperty=fullName> <xref:System.Web.IHttpHandler?displayProperty=fullName>uygulamalarıdır.

- Sınıfı [ `new` kısıtlaması](/dotnet/csharp/language-reference/keywords/new-constraint)olan bir tür parametresi olarak geçirilir. Aşağıdaki örnek Rule CA1812 tarafından işaretlenir:

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

## <a name="related-rules"></a>İlgili kurallar

- [CA1811 Çağrılmadı özel koddan kaçının](../code-quality/ca1811-avoid-uncalled-private-code.md)
- [CA1801 Kullanılmayan parametreleri gözden geçir](../code-quality/ca1801-review-unused-parameters.md)
- [CA1804 Kullanılmayan yerelleri kaldır](../code-quality/ca1804-remove-unused-locals.md)