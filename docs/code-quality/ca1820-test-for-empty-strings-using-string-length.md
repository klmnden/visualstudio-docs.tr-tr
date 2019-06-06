---
title: 'CA1820: Dize uzunluğunu kullanarak boş dizeleri test edin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- TestForEmptyStringsUsingStringLength
- CA1820
helpviewer_keywords:
- TestForEmptyStringsUsingStringLength
- CA1820
ms.assetid: da1e70c8-b1dc-46b9-8b8f-4e6e48339681
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bb5160ef663375ee3dd4b45797e8f4536acdf793
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66744654"
---
# <a name="ca1820-test-for-empty-strings-using-string-length"></a>CA1820: Dize uzunluğunu kullanarak boş dizeleri test edin

|||
|-|-|
|TypeName|TestForEmptyStringsUsingStringLength|
|CheckId|CA1820|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Bir dize kullanarak boş bir dize karşılaştırma <xref:System.Object.Equals%2A?displayProperty=nameWithType>.

## <a name="rule-description"></a>Kural açıklaması

Karşılaştırma dizeleri kullanarak <xref:System.String.Length%2A?displayProperty=nameWithType> özelliği veya <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> yöntemdir kullanmaktan daha hızlı <xref:System.Object.Equals%2A>. Bunun nedeni, <xref:System.Object.Equals%2A> ya da daha fazla MSIL yönergeleri yürüten <xref:System.String.IsNullOrEmpty%2A> veya yönerge almak için yürütülen sayısını <xref:System.String.Length%2A> özellik değer ve sıfır olarak karşılaştırır.

Null dizeler için <xref:System.Object.Equals%2A> ve `<string>.Length == 0` farklı davranır. Değeri alınacak çalışırsanız <xref:System.String.Length%2A> boş bir dize özelliği, ortak dil çalışma zamanı oluşturur bir <xref:System.NullReferenceException?displayProperty=fullName>. Boş bir dize ve boş bir dize arasında bir karşılaştırma gerçekleştirmek, ortak dil çalışma zamanı bir özel durum oluşturmaz ve döndürür `false`. Null sınaması, bu iki yaklaşımı göreli performansını önemli ölçüde etkilemez. .NET Framework 2.0 veya üstü hedeflenirken kullanın <xref:System.String.IsNullOrEmpty%2A> yöntemi. Aksi takdirde kullanın <xref:System.String.Length%2A> == 0 karşılaştırma mümkün olduğunda.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için kullanılacak karşılaştırma değiştirme <xref:System.String.IsNullOrEmpty%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Performans sorunu değilse bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, boş bir dize aramak için kullanılan farklı teknikleri gösterir.

[!code-csharp[FxCop.Performance.StringTest#1](../code-quality/codesnippet/CSharp/ca1820-test-for-empty-strings-using-string-length_1.cs)]