---
title: 'CA2239: İsteğe bağlı metotlar için serileştirme kaldırma metotları sağlayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2239
- ProvideDeserializationMethodsForOptionalFields
helpviewer_keywords:
- ProvideDeserializationMethodsForOptionalFields
- CA2239
ms.assetid: 6480ff5e-0caa-4707-814e-2f927cdafef5
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c0cd59ec30ce45c94ac3422c4271959d74073bff
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920056"
---
# <a name="ca2239-provide-deserialization-methods-for-optional-fields"></a>CA2239: İsteğe bağlı metotlar için serileştirme kaldırma metotları sağlayın

|||
|-|-|
|TypeName|ProvideDeserializationMethodsForOptionalFields|
|CheckId|CA2239|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir tür, <xref:System.Runtime.Serialization.OptionalFieldAttribute?displayProperty=fullName> özniteliğiyle işaretlenmiş bir alana sahip ve tür, serileştirme olay işleme yöntemleri sağlamıyor.

## <a name="rule-description"></a>Kural açıklaması
<xref:System.Runtime.Serialization.OptionalFieldAttribute> Özniteliğin serileştirme üzerinde hiçbir etkisi yoktur; özniteliğiyle işaretlenmiş bir alan serileştirilir. Ancak, alanı seri hale getirme sırasında yok sayılır ve kendi türüyle ilişkili varsayılan değeri korur. Seri hale getirme işlemi sırasında alanı ayarlamak için de serileştirme olay işleyicileri bildirilmelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, türe serileştirme olay işleme yöntemleri ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Seri hale getirme işlemi sırasında alanın yoksayılması gerekiyorsa, bu kuraldan bir uyarıyı gizlemek güvenlidir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, isteğe bağlı bir alan ve Serileştirme olay işleme yöntemleri içeren bir türü gösterir.

[!code-csharp[FxCop.Usage.OptionalFields#1](../code-quality/codesnippet/CSharp/ca2239-provide-deserialization-methods-for-optional-fields_1.cs)]
[!code-vb[FxCop.Usage.OptionalFields#1](../code-quality/codesnippet/VisualBasic/ca2239-provide-deserialization-methods-for-optional-fields_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA2236 ISerializable türlerinde temel sınıf yöntemlerini çağırma](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)

[CA2240 ISerializable 'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)

[CA2229 Serileştirme oluşturucularını Uygula](../code-quality/ca2229-implement-serialization-constructors.md)

[CA2238 Serileştirme yöntemlerini doğru uygulayın](../code-quality/ca2238-implement-serialization-methods-correctly.md)

[CA2235 Tüm seri hale getirilebilir olmayan alanları işaretle](../code-quality/ca2235-mark-all-non-serializable-fields.md)

[CA2237 ISerializable türlerini SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

[CA2120 Güvenli serileştirme oluşturucuları](../code-quality/ca2120-secure-serialization-constructors.md)