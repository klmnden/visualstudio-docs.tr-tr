---
title: 'CA1721: Özellik adları get metotları ile eşleşmemelidir'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
helpviewer_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
ms.assetid: 45a0e853-1f06-4688-af1b-cc634409e295
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: bf16a9edf25132aa8b58702f01563b8d7ccf109a
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65841502"
---
# <a name="ca1721-property-names-should-not-match-get-methods"></a>CA1721: Özellik adları get metotları ile eşleşmemelidir

|||
|-|-|
|TypeName|PropertyNamesShouldNotMatchGetMethods|
|CheckId|CA1721|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir üyenin adını 'Get' ile başlar ve aksi takdirde bir özellik adıyla eşleşen. Örneğin, 'GetColor' ve 'Color' adlı bir özellik adında bir yöntemi içeren bir tür, bir kuralı ihlali neden.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen üye özellikleri de görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

"Get" yöntemlerinin ve özelliklerinin açıkça işlevlerinden ayırt edilebilen adları olması gerekir.

Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu tutarlılık kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır ve yeni bir yazılım kitaplığı öğrenmek için gereken süreyi azaltır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

'Get' önekli bir metot adı eşleşmiyor adı değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

> [!NOTE]
> Bu uyarı, Iextenderprovider arabirimi uygulayarak "Get" yöntemi neden oluyorsa atlanabilir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1721.api_surface = private, internal
```

Bu kategoride (adlandırma), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bir yöntem ve bu kuralı ihlal ediyor özelliği içerir.

[!code-csharp[FxCop.Naming.GetMethod#1](../code-quality/codesnippet/CSharp/ca1721-property-names-should-not-match-get-methods_1.cs)]
[!code-vb[FxCop.Naming.GetMethod#1](../code-quality/codesnippet/VisualBasic/ca1721-property-names-should-not-match-get-methods_1.vb)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1024: Uygun yerlerde özellikler kullan](../code-quality/ca1024-use-properties-where-appropriate.md)