---
title: 'CA2237: ISerializable türleri SerializableAttribute ile işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2237
- MarkISerializableTypesWithSerializable
helpviewer_keywords:
- MarkISerializableTypesWithSerializable
- CA2237
ms.assetid: 9bd6bb24-a527-43dd-9952-043c0c694f46
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 53d049cad426201a8aaa48662061a4a424116b26
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237934"
---
# <a name="ca2237-mark-iserializable-types-with-serializableattribute"></a>CA2237: ISerializable türleri SerializableAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkISerializableTypesWithSerializable|
|CheckId|CA2237|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Dışarıdan görünen bir tür <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimini uygular ve tür, <xref:System.SerializableAttribute?displayProperty=fullName> özniteliğiyle işaretlenmez. Kural, temel türü seri hale getirilebilir olmayan türetilmiş türleri yoksayar.

## <a name="rule-description"></a>Kural açıklaması
Ortak dil çalışma zamanı tarafından seri hale getirilebilir olarak tanınmak için, tür, <xref:System.SerializableAttribute> <xref:System.Runtime.Serialization.ISerializable> arabirimin uygulanmasıyla özel bir serileştirme yordamı kullanıyor olsa bile, türlerin özniteliğiyle işaretlenmesi gerekir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, türüne <xref:System.SerializableAttribute> özniteliğini uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı, uygulama etki alanlarında doğru şekilde çalışması için seri hale getirilebilir olmaları gerektiğinden özel durum sınıfları için kaldırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir. Kuralın yerine getirmek için özniteliksatırınınaçıklamasınıkaldırın.<xref:System.SerializableAttribute>

[!code-vb[FxCop.Usage.MarkSerializable#1](../code-quality/codesnippet/VisualBasic/ca2237-mark-iserializable-types-with-serializableattribute_1.vb)]
[!code-csharp[FxCop.Usage.MarkSerializable#1](../code-quality/codesnippet/CSharp/ca2237-mark-iserializable-types-with-serializableattribute_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2236 ISerializable türlerinde temel sınıf yöntemlerini çağırma](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)

[CA2240 ISerializable 'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)

[CA2229 Serileştirme oluşturucularını Uygula](../code-quality/ca2229-implement-serialization-constructors.md)

[CA2238 Serileştirme yöntemlerini doğru uygulayın](../code-quality/ca2238-implement-serialization-methods-correctly.md)

[CA2235 Tüm seri hale getirilebilir olmayan alanları işaretle](../code-quality/ca2235-mark-all-non-serializable-fields.md)

[CA2239 İsteğe bağlı alanlar için seri durumdan çıkarma yöntemleri sağlama](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)

[CA2120 Güvenli serileştirme oluşturucuları](../code-quality/ca2120-secure-serialization-constructors.md)