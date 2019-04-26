---
title: 'CA1716: Tanımlayıcılar anahtar sözcükler ile eşleşmemelidir'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
helpviewer_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
ms.assetid: 900cc8a1-1089-4069-a4ce-10b109ac4fab
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 279bcf3aecc2a637a7a36c2041ed63a72017a800
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62545836"
---
# <a name="ca1716-identifiers-should-not-match-keywords"></a>CA1716: Tanımlayıcılar anahtar sözcükler ile eşleşmemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotMatchKeywords|
|CheckId|CA1716|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir ad, tür adı veya sanal ya da ayrılmış bir anahtar sözcük bir programlama dilinde arabirim üyesiyle eşleşiyor.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen ad alanlarını, türleri ve üyeleri görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Tanımlayıcı ad alanları, türler, için ve sanal ve arabirim üyeleri olmayan ortak dil çalışma zamanını hedefleyen diller tarafından tanımlanan anahtar sözcükleri eşleşmelidir. Kullanılan dil ve anahtar sözcüğü bağlı olarak, derleyici hataları ve belirsizlikler kitaplığı kullanmak zorlaştırabilir.

Bu kural, anahtar sözcükleri şu dillerde karşı denetler:

- Visual Basic
- C#
- C++/CLI

Visual Basic anahtar sözcükleri için kullanılan büyük küçük harf duyarsız karşılaştırma ve büyük küçük harfe duyarlı karşılaştırma diğer diller için kullanılır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Anahtar sözcükler listesinde görünmeyen bir adı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Tanımlayıcı kullanıcılara API'nin karıştırır olmaz ve kitaplığı. NET'te tüm kullanılabilir diller kullanılamaz eminseniz, bu kuraldan bir uyarıyı gösterilmemesini sağlayabilirsiniz.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1716.api_surface = private, internal
```

Bu kategoride (adlandırma), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).