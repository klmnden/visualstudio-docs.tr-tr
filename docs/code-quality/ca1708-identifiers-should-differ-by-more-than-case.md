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
ms.openlocfilehash: 32ac2e430abdc068070457dcf362e39dcbc0b398
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57867550"
---
# <a name="ca1708-identifiers-should-differ-by-more-than-case"></a>CA1708: Tanımlayıcılar yalnızca büyük küçük harfle birbirinden farklı olmamalıdır

|||
|-|-|
|TypeName|IdentifiersShouldDifferByMoreThanCase|
|CheckId|CA1708|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

İki tür, üye, parametre veya tam ad alanları adları, küçük harfe dönüştürülmüş zaman aynıdır.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler, üyeler ve ad alanları görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Ortak dil çalışma zamanı hedef dilleri büyük/küçük harf duyarlı olması gerekmediğinden ad alanları, türler, üyeler ve parametreler için tanımlayıcılar yalnızca büyük/küçük harfe göre farklılık göstermeyebilir. Örneğin, [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] yaygın olarak kullanılan bir büyük küçük harf duyarsız dilidir.

Bu kural yalnızca herkese görünür üyelere tetikler.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Büyük küçük harf duyarlı bir şekilde diğer tanımlayıcılarla karşılaştırılır, benzersiz bir ad seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın. Kitaplığı, .NET Framework içindeki kullanılabilir tüm dillerde kullanılabilir olmayabilir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1708.api_surface = private, internal
```

Bu kategoride (adlandırma), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example-of-a-violation"></a>Bir ihlali örneği

Aşağıdaki örnek, bu kural ihlalini gösterir.

[!code-csharp[FxCop.Naming.IdentifiersShouldDifferByMoreThanCase#1](../code-quality/codesnippet/CSharp/ca1708-identifiers-should-differ-by-more-than-case_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1709: Tanımlayıcılar doğru yazılmalıdır](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)