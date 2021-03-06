---
title: 'CA1024: Uygun yerlerde özellikleri kullanın'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- UsePropertiesWhereAppropriate
- CA1024
helpviewer_keywords:
- CA1024
- UsePropertiesWhereAppropriate
ms.assetid: 3a04f765-af7c-4872-87ad-9cc29e8e657f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: d312618c80abb6a4ce6e1a2676903d85867f4989
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236153"
---
# <a name="ca1024-use-properties-where-appropriate"></a>CA1024: Uygun yerlerde özellikleri kullanın

|||
|-|-|
|TypeName|UsePropertiesWhereAppropriate|
|CheckId|CA1024|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir yöntemin ile `Get`başlayan bir adı vardır, hiçbir parametre kullanmaz ve dizi olmayan bir değer döndürür.

Varsayılan olarak, bu kural yalnızca ortak ve korumalı yöntemlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Çoğu durumda, özellikler verileri ve yöntemleri eylemler gerçekleştirir. Özellikler, alanları gibi erişilir, bu da daha kolay kullanılmasını sağlar. Bu koşullardan biri mevcutsa, bir özellik olmak için bir yöntem iyi bir adaydır:

- Bağımsız değişken almaz ve bir nesnenin durum bilgilerini döndürür.

- Bir nesnenin durumunun bir bölümünü ayarlamak için tek bir bağımsız değişkeni kabul eder.

Özellikler alanlar gibi davranmalıdır; yöntemi değilse, bir özelliğe değiştirilmemelidir. Yöntemler aşağıdaki durumlarda özelliklerden daha iyidir:

- Yöntemi zaman alan bir işlem gerçekleştirir. Yöntemi, bir alanın değerini ayarlamak ya da almak için gereken zamandan daha yavaştır perceivably.

- Yöntemi bir dönüştürme gerçekleştirir. Bir alana erişmek, depoladığı verilerin dönüştürülmüş bir sürümünü döndürmez.

- Get yönteminin bir observable yan etkisi vardır. Bir alanın değerini almak hiçbir yan efekt oluşturmaz.

- Yürütmenin sırası önemlidir. Bir alanın değerini ayarlamak, diğer işlemlerin oluşumuna bağlı değildir.

- Yöntemi art arda iki kez çağırmak farklı sonuçlar oluşturur.

- Yöntemi statiktir, ancak çağıran tarafından değiştirilebilen bir nesne döndürür. Bir alanın değerini almak, çağıranın alan tarafından depolanan verileri değiştirmesine izin vermez.

- Yöntemi bir dizi döndürür.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, yöntemini bir özelliği olarak değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yöntem daha önce listelenen ölçütlerden en az birini karşılıyorsa, bu kuraldan bir uyarı gizleyin.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1024.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="control-property-expansion-in-the-debugger"></a>Hata ayıklayıcıda denetim özelliği genişletmesi

Programcıların bir özelliği kullanmaktan kaçınmasının nedeni, hata ayıklayıcının onu denklemeyi istememesinden kaynaklanır. Örneğin, özelliği büyük bir nesne ayırmayı veya bir P/Invoke çağırmayı içerebilir, ancak aslında herhangi bir observable yan etkisi olmayabilir.

Hata ayıklayıcının, özellikleri uygulayarak <xref:System.Diagnostics.DebuggerBrowsableAttribute?displayProperty=fullName>, özellikleri genişletmeyi önleyebilirsiniz. Aşağıdaki örnek, bir örnek özelliğine uygulanan bu özniteliği gösterir.

```vb
Imports System
Imports System.Diagnostics

Namespace Microsoft.Samples

    Public Class TestClass

        ' [...]

        <DebuggerBrowsable(DebuggerBrowsableState.Never)> _
        Public ReadOnly Property LargeObject() As LargeObject
            Get
                ' Allocate large object
                ' [...]
            End Get
        End Property

    End Class

End Namespace
```

```csharp
using System;
using System.Diagnostics;

namespace Microsoft.Samples
{
    publicclass TestClass
    {
        // [...]

        [DebuggerBrowsable(DebuggerBrowsableState.Never)]
        public LargeObject LargeObject
        {
            get
            {
                // Allocate large object
                // [...]
            }
        }
    }
}
```

## <a name="example"></a>Örnek

Aşağıdaki örnek, Özellikler ' e dönüştürülmesi gereken çeşitli yöntemler ve bunlar gibi davranmamaları nedeniyle olmaması gereken birkaç yöntem içerir.

[!code-csharp[FxCop.Design.MethodsProperties#1](../code-quality/codesnippet/CSharp/ca1024-use-properties-where-appropriate_1.cs)]