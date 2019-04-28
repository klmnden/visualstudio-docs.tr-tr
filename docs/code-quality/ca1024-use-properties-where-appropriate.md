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
ms.openlocfilehash: e4008872a7cb96386ef702d21ba8a18d96037d83
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62779389"
---
# <a name="ca1024-use-properties-where-appropriate"></a>CA1024: Uygun yerlerde özellikleri kullanın

|||
|-|-|
|TypeName|UsePropertiesWhereAppropriate|
|CheckId|CA1024|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir yöntem ile başlayan bir ada sahip `Get`hiçbir parametre almaz ve dizi olmayan bir değer döndürür.

Varsayılan olarak, bu kural yalnızca ortak ve korunan yöntem ele alınmakta, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Çoğu durumda veri özelliklerini temsil eder ve yöntemleri eylemleri gerçekleştirebilirsiniz. Özellikler, bunları kullanmayı kolaylaştırır alanları gibi erişilir. Bir yöntem, Bu koşullardan biri varsa özellik olmak için iyi bir adaydır:

- Hiçbir bağımsız değişkeni alır ve bir nesnenin durum bilgilerini döndürür.

- Bir nesnenin durumu kısmı ayarlamak için tek bir bağımsız değişken kabul eder.

Özellikleri, alanları ise olarak hareket etmesi gerektiğini; yöntem çözemezseniz, bir özelliğe değiştirilmemelidir. Aşağıdaki durumlarda özelliklerini daha iyi yöntemler şunlardır:

- Yöntem, zaman alıcı bir işlem gerçekleştirir. Yöntemi, perceivably ayarlamak veya bir alanın değerini almak için gereken süreden daha yavaştır.

- Bir dönüştürme yöntemi gerçekleştirir. Bir alana erişim depoladığı verilerin dönüştürülmüş bir sürümünü döndürmez.

- Get yöntemi gözlemlenebilir bir yan etkisi vardır. Bir alanın değerini alma yan etkileri üretmez.

- Yürütme sırası önemlidir. Bir alanın değerini ayarlama, diğer işlemleri oluşması bağımlı kalmayacak.

- Yöntemi, art arda iki kez çağırmak farklı sonuçlar oluşturur.

- Yöntem statik olsa da arayan tarafından değiştirilebilen bir nesne döndürür. Bir alanın değerini alma alanı tarafından depolanan verileri değiştirmek çağıranın izin vermez.

- Yöntemi, bir dizi döndürür.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için yöntem bir özelliğini değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Yöntem en az bir tanesi yukarıda listelenen ölçütlerini karşılıyorsa bu kuraldan bir uyarıyı gizler.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1024.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="control-property-expansion-in-the-debugger"></a>Hata ayıklayıcı denetim özelliği genişletme

Hata ayıklayıcıyı autoexpand istemediğiniz programcılar kaçının bir özelliğini kullanarak bir neden olduğundan bu. Örneğin, özellik, büyük nesne ayırma veya P/Invoke çağırma gerektirebilir, ancak gözlemlenebilir bir yan etkileri gerçekten olmayabilir.

Hata ayıklayıcı autoexpanding özelliklerinden uygulayarak engelleyebilir <xref:System.Diagnostics.DebuggerBrowsableAttribute?displayProperty=fullName>. Aşağıdaki örnek, bir örnek özelliğine uygulanan bu özniteliği gösterir.

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

Aşağıdaki örnek, özelliklerine dönüştürülmesi gerektiğini ve alanlar gibi davranırlar yoksa değil çünkü, birkaç gereken çeşitli yöntemler içerir.

[!code-csharp[FxCop.Design.MethodsProperties#1](../code-quality/codesnippet/CSharp/ca1024-use-properties-where-appropriate_1.cs)]