---
title: 'CA1708: Tanımlayıcılar yalnızca büyük küçük harfle birbirinden farklı olmamalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- IdentifiersShouldDifferByMoreThanCase
- CA1708
helpviewer_keywords:
- CA1708
- IdentifiersShouldDifferByMoreThanCase
ms.assetid: dac0f01d-dd21-484d-add1-c8cd2bf6969f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7203f7f287ebb5b71ecad6e6ad4a861d63e5cf08
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234223"
---
# <a name="ca1708-identifiers-should-differ-by-more-than-case"></a>CA1708: Tanımlayıcılar yalnızca büyük küçük harfle birbirinden farklı olmamalıdır

|||
|-|-|
|TypeName|IdentifiersShouldDifferByMoreThanCase|
|CheckId|CA1708|
|Kategori|Microsoft. Naming|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

İki tür, üye, parametre veya tam ad alanlarının adları, küçük harfe dönüştürülediklerinde aynıdır.

Bu kural varsayılan olarak yalnızca dışarıdan görünen türler, Üyeler ve ad alanları ' na bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Ortak dil çalışma zamanı hedef dilleri büyük/küçük harf duyarlı olması gerekmediğinden ad alanları, türler, üyeler ve parametreler için tanımlayıcılar yalnızca büyük/küçük harfe göre farklılık göstermeyebilir. Örneğin, yaygın [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] olarak kullanılan büyük/küçük harf duyarsız bir dildir.

Bu kural yalnızca herkes tarafından görülebilir Üyeler üzerinde ateşlenir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Büyük/küçük harfe duyarsız bir şekilde diğer tanımlayıcılarla karşılaştırıldığında benzersiz bir ad seçin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Kitaplık, .NET 'teki tüm kullanılabilir dillerde kullanılamayabilir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1708.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (adlandırma) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example-of-a-violation"></a>İhlalin örneği

Aşağıdaki örnek, bu kuralın ihlaline neden olduğunu gösterir.

[!code-csharp[FxCop.Naming.IdentifiersShouldDifferByMoreThanCase#1](../code-quality/codesnippet/CSharp/ca1708-identifiers-should-differ-by-more-than-case_1.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1709 Tanımlayıcılar doğru şekilde yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)