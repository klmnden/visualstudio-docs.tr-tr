---
title: 'CA1802: Uygun yerlerde sabitleri kullanın'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- UseLiteralsWhereAppropriate
- CA1802
helpviewer_keywords:
- UseLiteralsWhereAppropriate
- CA1802
ms.assetid: 2515e4cd-9e61-486d-b067-58ba1a743ce4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c6512f02d13c2eeb441f5b374c4785deffe22a22
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547059"
---
# <a name="ca1802-use-literals-where-appropriate"></a>CA1802: Uygun yerlerde sabitleri kullanın

|||
|-|-|
|TypeName|UseLiteralsWhereAppropriate|
|CheckId|CA1802|
|Kategori|Microsoft. Performance|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir alan, `static` ve `readonly` (`Shared` ve `ReadOnly` Visual Basic) olarak tanımlanır ve derleme zamanında oluşturulabilir bir değer ile başlatılır.

Bu kural varsayılan olarak yalnızca dışarıdan görünür alanlara bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bildirim türü için statik `static readonly` Oluşturucu çağrıldığında bir alanın değeri çalışma zamanında hesaplanır. `static readonly` Alan bildirildiği zaman başlatılır ve statik bir oluşturucu açıkça bildirilmemiş ise, derleyici alanı başlatmak için statik bir Oluşturucu yayar.

Bir `const` alanın değeri, derleme zamanında hesaplanır ve meta verilerde depolanır, bu da bir `static readonly` alanla karşılaştırıldığında çalışma zamanı performansını artırır.

Hedeflenen alana atanan değer derleme zamanında oluşturulabilir olduğundan, değeri çalışma zamanı yerine derleme zamanında hesaplanabilmesi için bildirimi bir `const` alanla değiştirin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, `static` ve `readonly` değiştiricilerini `const` değiştiriciyle değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek veya performans sorun değilse kuralı devre dışı bırakmak güvenlidir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1802.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (performans) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralı ve `UseReadOnly` `UseConstant`kuralını karşılayan bir türü ihlal eden bir türü gösterir.

[!code-vb[FxCop.Performance.UseLiterals#1](../code-quality/codesnippet/VisualBasic/ca1802-use-literals-where-appropriate_1.vb)]
[!code-csharp[FxCop.Performance.UseLiterals#1](../code-quality/codesnippet/CSharp/ca1802-use-literals-where-appropriate_1.cs)]