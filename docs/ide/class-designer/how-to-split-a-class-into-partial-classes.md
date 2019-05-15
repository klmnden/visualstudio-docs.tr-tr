---
title: 'Nasıl yapılır: Bir sınıfı kısmi sınıflara (Sınıf Tasarımcısı) bölme'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Class Designer, partial classes
- partial classes, Class Designer
ms.assetid: 6f6b0b30-3996-4569-9200-20482b3adf90
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: e1426b1ad9799984f7b14604a1d8b685e9ce8813
ms.sourcegitcommit: 77b4ca625674658d5c5766e684fa0e2a07cad4da
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65615403"
---
# <a name="how-to-split-a-class-into-partial-classes-in-class-designer"></a>Nasıl yapılır: Bir sınıf, Sınıf Tasarımcısı'nda parçalı sınıflar Böl

Kullanabileceğiniz `partial` anahtar sözcüğü (`Partial` Visual Basic'te) bir sınıf veya yapı çeşitli bildirimler arasında bildirimi ayırmak için. İstediğiniz sayıda kısmi bildirimleri kullanabilirsiniz.

Bildirimler, bir veya birden çok kaynak dosyalarında olabilir. Tüm bildirimler aynı derleme ve aynı ad alanı içinde olmalıdır.

Kısmi sınıflar çeşitli durumlarda yararlı olur. Büyük bir proje üzerinde örneğin, bir sınıfın birden çok dosyaya ayırmak proje üzerinde aynı anda çalışmak birden fazla Programcı sağlar. Visual Studio oluşturan kod ile çalışırken, sınıf kaynak dosyasını yeniden oluşturmak zorunda kalmadan değiştirebilirsiniz. (Windows Forms ve web hizmeti sarmalayıcı kodu Visual Studio'nun oluşturduğu kod örneklerini içerir.) Bu nedenle, otomatik olarak oluşturulan sınıfları oluşturan Visual Studio dosyayı değiştirmek zorunda kalmadan kullanan kodu oluşturabilirsiniz.

Kısmi yöntemler iki tür vardır. C# ' ta bildirme ve uygulama çağrılır; Visual Basic'te, bunlara bildirimini ve uygulamasını verilir.

**Sınıf Tasarımcısı** kısmi sınıflar ve yöntemler destekler. Tür şeklini sınıf diyagramı içinde kısmi sınıfın tek bildirimde konumunu ifade eder. Kısmi sınıf birden çok dosyalarında tanımlandıysa, bildirim konumu belirtebilirsiniz **Sınıf Tasarımcısı** ayarlayarak kullanacağı **yeni üye konumu** özelliğinde **özellikleri**  penceresi. Diğer bir deyişle, bir sınıf şeklinin çift tıkladığınızda **Sınıf Tasarımcısı** tarafından tanımlanmış sınıf bildirimi içeren kaynak dosyaya gider **yeni üye konumu** özelliği. Kısmi bir yöntem, sınıf şeklinin içinde çift tıkladığınızda **Sınıf Tasarımcısı** için kısmi yöntem bildiriminde gider. Ayrıca, **özellikleri** penceresinde **dosya adı** özelliği bildirimi konuma başvuruyor. Kısmi sınıflar için **dosya adı** bildirimini ve uygulamasını bu sınıfın kodu içeren dosyaları listeler. Ancak, kısmi yöntemler için **dosya adı** kısmi yöntem bildirimi içeren dosyanın listeler.

Aşağıdaki örnekler sınıfının tanımını bölme `Employee` alanına iki bildirimler, her biri farklı bir yordam tanımlar. İki kısmi tanım örneklerde, bir kaynak dosyasında veya iki farklı kaynak dosyalar olabilir.

> [!NOTE]
> Visual Basic, Visual Studio tarafından oluşturulan kod, kullanıcı tarafından yazılan kodu ayırmak için kısmi sınıf tanımları kullanır. Kod ayrı kaynak dosyalarıyla ayrılır. Örneğin, **Windows Form Tasarımcısı** denetimleri için kısmi sınıflar gibi tanımlar `Form`. Bu denetimler oluşturulan kodda değiştirmeniz gerekir.

Visual Basic'te kısmi türleri hakkında daha fazla bilgi için bkz. [kısmi](/dotnet/visual-basic/language-reference/modifiers/partial).

## <a name="example"></a>Örnek

Bir sınıf tanımı bölmek için kullanın `partial` anahtar sözcüğü (`Partial` Visual Basic'te), aşağıdaki örnekte gösterildiği gibi:

```csharp
// First part of class definition.
public partial class Employee
{
    public void CalculateWorkHours()
    {
    }
}

// Second part of class definition.
public partial class Employee
{
    public void CalculateTaxes()
    {
    }
}
```

```vb
' First part of class definition.
Partial Public Class Employee
    Public Sub CalculateWorkHours()
    End Sub
End Class

' Second part of class definition.
Partial Public Class Employee
    Public Sub CalculateTaxes()
    End Sub
End Class
```

## <a name="see-also"></a>Ayrıca bkz.

- [Kısmi sınıflar ve yöntemler](/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods)
- [partial (tür) (C# Başvurusu)](/dotnet/csharp/language-reference/keywords/partial-type)
- [partial (yöntem) (C# Başvurusu)](/dotnet/csharp/language-reference/keywords/partial-method)
- [Kısmi (Visual Basic)](/dotnet/visual-basic/language-reference/modifiers/partial)