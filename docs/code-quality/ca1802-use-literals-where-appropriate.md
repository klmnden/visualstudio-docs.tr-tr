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
ms.openlocfilehash: dfa50fc6007c2313191b430e9ed5445e7fd72a88
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65841559"
---
# <a name="ca1802-use-literals-where-appropriate"></a>CA1802: Uygun yerlerde sabitleri kullanın

|||
|-|-|
|TypeName|UseLiteralsWhereAppropriate|
|CheckId|CA1802|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir alana bildirilen `static` ve `readonly` (`Shared` ve `ReadOnly` Visual Basic'te) ve derleme zamanında hesaplanabilen bir değer ile başlatılır.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen alanları görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Değerini bir `static readonly` bildirim türü statik Oluşturucusu çağrıldığında, alanı çalışma zamanında hesaplanır. Varsa `static readonly` alan bildirildiği ve derleyici alanı başlatmak için bir statik Oluşturucu yayan bir statik Oluşturucu açıkça bildirilmedi başlatılır.

Değerini bir `const` alan derleme zamanında hesaplanır ve için karşılaştırıldığında çalışma zamanı performansını artıran meta verilerde depolanan bir `static readonly` alan.

Hedeflenen alana atanan değer derleme zamanında hesaplanabilir olduğundan, bildirime değiştirme bir `const` çalışma zamanında derleme zaman yerine değeri hesaplanan alanın.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için yerine `static` ve `readonly` değiştiricilerini `const` değiştiricisi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Performans bir sorun değilse bu kuraldan bir uyarıyı bastırmak veya kuralı devre dışı bırakmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1802.api_surface = private, internal
```

Bu kategoride (performans), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bir tür gösterir `UseReadOnly`, kuralı ve bir tür ihlal `UseConstant`, bu kural karşılar.

[!code-vb[FxCop.Performance.UseLiterals#1](../code-quality/codesnippet/VisualBasic/ca1802-use-literals-where-appropriate_1.vb)]
[!code-csharp[FxCop.Performance.UseLiterals#1](../code-quality/codesnippet/CSharp/ca1802-use-literals-where-appropriate_1.cs)]