---
title: 'CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2235
- MarkAllNonSerializableFields
helpviewer_keywords:
- CA2235
- MarkAllNonSerializableFields
ms.assetid: 599ad877-3a15-426c-bf17-5de15427365f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 886cc66f820d201b8ab7f29fee00eebce07fc176
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71238110"
---
# <a name="ca2235-mark-all-non-serializable-fields"></a>CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin

|||
|-|-|
|TypeName|MarkAllNonSerializableFields|
|CheckId|CA2235|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Seri hale getirilemeyen bir örnek alan türü seri hale getirilebilir bir tür içinde bildirilir.

## <a name="rule-description"></a>Kural açıklaması

Seri hale getirilebilir bir tür, <xref:System.SerializableAttribute?displayProperty=fullName> özniteliğiyle işaretlenmiş bir türüdür. Tür serileştirildiğinde, tür seri hale <xref:System.Runtime.Serialization.SerializationException?displayProperty=fullName> getirilebilir olmayan *ve* <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimi uygulamayan bir türün örnek alanını içeriyorsa, bir özel durum oluşturulur.

> [!TIP]
> CA2235, kendi serileştirme mantığını sağladığından, uygulayan <xref:System.Runtime.Serialization.ISerializable> türlerin örnek alanları için başlatılmıyor.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için <xref:System.NonSerializedAttribute?displayProperty=fullName> özniteliği seri hale getirilebilir olmayan alana uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan yalnızca, alan örneklerinin serileştirilmesine ve <xref:System.Runtime.Serialization.ISerializationSurrogate?displayProperty=fullName> seri durumdan çıkarıldığına izin veren bir tür bildirilirse bir uyarı gizleyin.

## <a name="example"></a>Örnek

Aşağıdaki örnek iki tür gösterir: kuralı ihlal eden ve kuralı karşılayan bir.

[!code-csharp[FxCop.Usage.MarkNonSerializable#1](../code-quality/codesnippet/CSharp/ca2235-mark-all-non-serializable-fields_1.cs)]
[!code-vb[FxCop.Usage.MarkNonSerializable#1](../code-quality/codesnippet/VisualBasic/ca2235-mark-all-non-serializable-fields_1.vb)]

## <a name="remarks"></a>Açıklamalar

Rule CA2235, <xref:System.Runtime.Serialization.ISerializable> arabirimini uygulayan türleri analiz etmez (aynı zamanda <xref:System.SerializableAttribute> özniteliğiyle işaretlenmedikçe). Bunun nedeni [kural CA2237](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md) , <xref:System.Runtime.Serialization.ISerializable> arabirimi uygulayan türleri <xref:System.SerializableAttribute> özniteliği ile işaretlemeye zaten öneriyor.

## <a name="related-rules"></a>İlgili kurallar

- [CA2229 Serileştirme oluşturucularını Uygula](../code-quality/ca2229-implement-serialization-constructors.md)
- [CA2236 ISerializable türlerinde temel sınıf yöntemlerini çağırma](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)
- [CA2237 ISerializable türlerini SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)
- [CA2238 Serileştirme yöntemlerini doğru uygulayın](../code-quality/ca2238-implement-serialization-methods-correctly.md)
- [CA2239 İsteğe bağlı alanlar için seri durumdan çıkarma yöntemleri sağlama](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)
- [CA2240 ISerializable 'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)
- [CA2120 Güvenli serileştirme oluşturucuları](../code-quality/ca2120-secure-serialization-constructors.md)