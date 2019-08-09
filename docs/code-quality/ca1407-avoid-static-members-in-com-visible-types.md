---
title: 'CA1407: COM görünebilir türler içinde statik üyelerden kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1407
- AvoidStaticMembersInComVisibleTypes
helpviewer_keywords:
- CA1407
- AvoidStaticMembersInComVisibleTypes
ms.assetid: bebd0776-ad04-453c-bca8-8c124c2d7840
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 631be1a93318cd24af4251fefbc710294fa52bf7
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922003"
---
# <a name="ca1407-avoid-static-members-in-com-visible-types"></a>CA1407: COM görünebilir türler içinde statik üyelerden kaçının

|||
|-|-|
|TypeName|AvoidStaticMembersInComVisibleTypes|
|CheckId|CA1407|
|Kategori|Microsoft. çalışabilirliği|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Özellikle bileşen nesne modeli (com) tarafından görünür olarak işaretlenen bir tür, bir `public``static` yöntemi içerir.

## <a name="rule-description"></a>Kural açıklaması
COM, yöntemleri desteklemez `static` .

Bu kural, özellik ve olay erişimcileri, işleç aşırı yükleme yöntemleri veya <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute?displayProperty=fullName> özniteliği <xref:System.Runtime.InteropServices.ComUnregisterFunctionAttribute?displayProperty=fullName> ya da özniteliği kullanılarak işaretlenen yöntemleri yoksayar.

Varsayılan olarak, aşağıdakiler COM 'a görünür: derlemeler, ortak türler, ortak türlerdeki ortak örnek üyeleri ve tüm ortak değer türleri üyeleri.

Bu kuralın gerçekleşmesi için, aşağıdaki kodun gösterdiği gibi, <xref:System.Runtime.InteropServices.ComVisibleAttribute> derleme düzeyi olarak `false` ayarlanmalıdır ve sınıfı <xref:System.Runtime.InteropServices.ComVisibleAttribute> olarak ayarlanmalıdır `true`.

```csharp
using System;
using System.Runtime.InteropServices;

[assembly: ComVisible(false)]
namespace Samples
{
    [ComVisible(true)]
    public class MyClass
    {
        public static void DoSomething()
        {
        }
    }
}
```

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için tasarımı, `static` yöntemiyle aynı işlevselliği sağlayan bir örnek yöntemi kullanacak şekilde değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bir com istemcisi, `static` yöntemi tarafından belirtilen işlevlere erişim gerektirmiyorsa, bu kuraldan bir uyarıyı gizlemek güvenlidir.

## <a name="example-violation"></a>Örnek Ihlali

### <a name="description"></a>Açıklama
Aşağıdaki örnek, bu kuralı `static` ihlal eden bir yöntemi gösterir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Interoperability.ComVisibleStaticMembersViolation#1](../code-quality/codesnippet/CSharp/ca1407-avoid-static-members-in-com-visible-types_1.cs)]

### <a name="comments"></a>Açıklamalar
Bu örnekte, **Book. FromPages** yöntemi com 'dan çağrılamaz.

## <a name="example-fix"></a>Örnek onarma

### <a name="description"></a>Açıklama
Önceki örnekteki ihlalin giderilmesi için, yöntemini bir örnek yöntemi olarak değiştirebilirsiniz, ancak bu örnekte bu anlamlı değildir. Daha iyi bir çözüm, yöntemin com `ComVisible(false)` 'dan görülemeyeceğini diğer geliştiricilere açık hale getirmek üzere yöntemine açıkça uygulanmasıdır.

Aşağıdaki örnek yöntemi için <xref:System.Runtime.InteropServices.ComRegisterFunctionAttribute> geçerlidir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Interoperability.ComVisibleStaticMembersFixed#1](../code-quality/codesnippet/CSharp/ca1407-avoid-static-members-in-com-visible-types_2.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1017 Derlemeleri ComVisibleAttribute ile işaretleyin](../code-quality/ca1017-mark-assemblies-with-comvisibleattribute.md)

[CA1406 Visual Basic 6 istemcileri için Int64 bağımsız değişkenlerinden kaçının](../code-quality/ca1406-avoid-int64-arguments-for-visual-basic-6-clients.md)

[CA1413 COM görünebilir değer türlerinde genel olmayan alanlardan kaçının](../code-quality/ca1413-avoid-non-public-fields-in-com-visible-value-types.md)

## <a name="see-also"></a>Ayrıca bkz.
[Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)