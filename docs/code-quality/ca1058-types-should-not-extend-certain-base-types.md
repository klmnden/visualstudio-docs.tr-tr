---
title: 'CA1058: Türler belirli temel türleri aşmamalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- TypesShouldNotExtendCertainBaseTypes
- CA1058
helpviewer_keywords:
- CA1058
- TypesShouldNotExtendCertainBaseTypes
ms.assetid: 8446ee40-beb1-49fa-8733-4d8e813471c0
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5d88f08746035792913601b280a0794a9ff50bf2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62795768"
---
# <a name="ca1058-types-should-not-extend-certain-base-types"></a>CA1058: Türler belirli temel türleri aşmamalıdır

|||
|-|-|
|TypeName|TypesShouldNotExtendCertainBaseTypes|
|CheckId|CA1058|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür aşağıdaki temel türlerinden birini genişletir:

- <xref:System.ApplicationException?displayProperty=fullName>
- <xref:System.Xml.XmlDocument?displayProperty=fullName>
- <xref:System.Collections.CollectionBase?displayProperty=fullName>
- <xref:System.Collections.DictionaryBase?displayProperty=fullName>
- <xref:System.Collections.Queue?displayProperty=fullName>
- <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>
- <xref:System.Collections.SortedList?displayProperty=fullName>
- <xref:System.Collections.Stack?displayProperty=fullName>

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

.NET Framework sürüm 1 için yeni özel durumlar türetmek için önerildiği <xref:System.ApplicationException>. Öneri değiştirildi ve yeni özel durumlar türetilmelidir <xref:System.Exception?displayProperty=fullName> veya içinde alt sınıflarından birini <xref:System> ad alanı.

Öğesinin oluşturmayın <xref:System.Xml.XmlDocument> , temel alınan bir nesne modeli veya veri kaynağı, bir XML görünümünü oluşturmak istiyorsanız.

### <a name="non-generic-collections"></a>Genel olmayan koleksiyonları

Kullanın ve/veya mümkün olduğunda genel koleksiyonları genişletin. Daha önce sevk sürece genel olmayan koleksiyon kodunuzda genişletmez.

**Yanlış kullanım örnekleri**

```csharp
public class MyCollection : CollectionBase
{
}

public class MyReadOnlyCollection : ReadOnlyCollectionBase
{
}
```

**Doğru kullanım örnekleri**

```csharp
public class MyCollection : Collection<T>
{
}

public class MyReadOnlyCollection : ReadOnlyCollection<T>
{
}
```

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için farklı bir temel tür ya da bir genel koleksiyon tür türetilir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Hakkında ihlalleri bu kuraldan bir uyarıyı bastırmayın <xref:System.ApplicationException>. Hakkında ihlalleri bu kuraldan bir uyarıyı bastırmak güvenlidir <xref:System.Xml.XmlDocument>. Kodu önceden yayımlanan, genel olmayan koleksiyonu hakkında bir uyarı bastırmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1058.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).