---
title: Anonim yöntem kod çözümleme uyarıları
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- methods, anonymous
- code analysis, anonymous methods
- anonymous methods, code analysis
ms.assetid: bf0a1a9b-b954-4d46-9c0b-cee65330ad00
dev_langs:
- CSharp
- VB
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5f8bfbf6100eed54589e4ea17a88807f9dd3cca2
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53739406"
---
# <a name="anonymous-methods-and-code-analysis"></a>Anonim Metotlar ve Kod Çözümleme

Bir *anonim yöntem* ada sahip bir yöntemdir. Anonim yöntemler, en sık temsilcinin parametre olarak bir kod bloğu geçirmek için kullanılır. Bu makalede, Kod Analizi uyarıları ve anonim yöntemler için ölçümleri nasıl işlediğini açıklar.

## <a name="anonymous-methods-declared-in-a-member"></a>Bir üye olarak bildirilen anonim yöntemler

Uyarılar ve ölçümler bir yöntem veya erişimci gibi bir üye olarak bildirilen anonim yöntemi için yöntem bildiren bir üye ile ilişkili. Bunlar, bu yöntemi çağıran bir üye ile ilişkili değildir.

Örneğin, sınıfta aşağıdaki bildiriminde bulunan tüm uyarılar **anonymousMethod** karşı harekete Geçirilmemesi gereken **Method1** değil **Method2**.

```vb
Delegate Function ADelegate(ByVal value As Integer) As Boolean

Class AClass
    Sub Method1()
        Dim anonymousMethod As ADelegate = Function(ByVal value As Integer) value > 5
        Method2(anonymousMethod)
    End Sub
    Sub Method2(ByVal anonymousMethod As ADelegate)
        anonymousMethod(10)
    End Sub
End Class
```

```csharp
delegate void Delegate();

class Class
{
    void Method1()
    {
        Delegate anonymousMethod = delegate()
        {
          Console.WriteLine("");
        }
        Method2(anonymousMethod);
    }

    void Method2(Delegate anonymousMethod)
    {
        anonymousMethod();
    }
}
```

## <a name="inline-anonymous-methods"></a>Satır içi anonim yöntemler

Uyarılar ve ölçümler için bir satır içi ataması için bir alan olarak bildirilen anonim yöntemi Oluşturucusu ile ilişkilidir. Alan olarak bildirilirse `static` (`Shared` Visual Basic'te), ölçümleri ve Uyarıları sınıf oluşturucusu ile ilişkilidir. Aksi takdirde, bunlar örnek oluşturucusu ile ilişkili.

Örneğin, sınıfta aşağıdaki bildiriminde bulunan tüm uyarılar **anonymousMethod1** karşı örtük olarak oluşturulan varsayılan oluşturucusu gerçekleştirilecektir **sınıfı**. Bulunan uyarıları **anonymousMethod2** örtük olarak oluşturulan sınıfın Oluşturucusu karşı uygulanır.

```vb
Delegate Function ADelegate(ByVal value As Integer) As Boolean
Class AClass
    Dim anonymousMethod1 As ADelegate = Function(ByVal value As Integer) value > 5
    Shared anonymousMethod2 As ADelegate = Function(ByVal value As Integer) value > 5

    Sub Method1()
        anonymousMethod1(10)
        anonymousMethod2(10)
    End Sub
End Class
```

```csharp
delegate void Delegate();

class Class
{
    Delegate anonymousMethod1 = delegate()
    {
       Console.WriteLine("");
    }

    static Delegate anonymousMethod2 = delegate()
    {
       Console.WriteLine("");
    }

    void Method()
    {
       anonymousMethod1();
       anonymousMethod2();
    }
}
```

Bir sınıf birden çok Oluşturucu sahip bir alan için değer atayan bir satır içi anonim yöntem içerebilir. Bu oluşturucu aynı sınıf içinde başka bir oluşturucu zincirine bağlı sürece bu durumda, uyarılar ve ölçümler ile tüm oluşturucular ilişkilendirilir.

Örneğin, sınıfta aşağıdaki bildiriminde bulunan tüm uyarılar **anonymousMethod** karşı harekete Geçirilmemesi gereken **Class(int)** ve **Class(string)**, ancak çalıştırılmaz **Class()**.

```vb
Delegate Function ADelegate(ByVal value As Integer) As Boolean

Class AClass

    Dim anonymousMethod As ADelegate = Function(ByVal value As Integer) value > 5

    SubNew()
        New(CStr(Nothing))
    End Sub

    Sub New(ByVal a As Integer)
    End Sub

    Sub New(ByVal a As String)
    End Sub
End Class
```

```csharp
delegate void Delegate();

class Class
{
    Delegate anonymousMethod = delegate()
    {
       Console.WriteLine("");
    }

    Class() : this((string)null)
    {
    }

    Class(int a)
    {
    }

    Class(string a)
    {
    }
}
```

Derleyici için başka bir oluşturucu zincirleme değil her oluşturucusu için benzersiz bir yöntem çıkardığından karşı oluşturucular uyarılar oluşturulur. Bu davranış nedeniyle, herhangi bir ihlali, oluşuyor **anonymousMethod** ayrı olarak atlanması gerekir. Yeni bir oluşturucusu varsa bu da anlamına gelen, daha önce karşı gizlenmiş uyarılar **Class(int)** ve **Class(string)** karşı yeni Oluşturucu ayrıca atlanması.

Bu sorunu iki yoldan biriyle çalışabilirsiniz:

- Bildirme **anonymousMethod** ortak bir oluşturucuda, tüm oluşturucular zinciri.
- Bildirme **anonymousMethod** tüm oluşturucular tarafından çağrılan bir başlatma yöntemi içinde.

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilen Kod Kalitesini Analiz Etme](../code-quality/code-analysis-for-managed-code-overview.md)