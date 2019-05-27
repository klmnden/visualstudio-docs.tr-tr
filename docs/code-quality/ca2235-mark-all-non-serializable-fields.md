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
ms.openlocfilehash: 5ebfa5e9b90951acf59c8214941b93adae76d06e
ms.sourcegitcommit: 13ab9a5ab039b070b9cd9251d0b83dd216477203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2019
ms.locfileid: "66177380"
---
# <a name="ca2235-mark-all-non-serializable-fields"></a>CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin

|||
|-|-|
|TypeName|MarkAllNonSerializableFields|
|CheckId|CA2235|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Seri hale getirilemeyen bir örnek alan türü seri hale getirilebilir bir tür içinde bildirilir.

## <a name="rule-description"></a>Kural açıklaması

Seri hale getirilebilir bir tür ile işaretlenmiş biridir <xref:System.SerializableAttribute?displayProperty=fullName> özniteliği. Türü seri olduğunda, bir <xref:System.Runtime.Serialization.SerializationException?displayProperty=fullName> serileştirilebilir değil bir tür bir örnek alan türü içeriyorsa, özel durum *ve* uygulamayan <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimi.

> [!TIP]
> CA2235 değil yangın örneği için uygulayan türlerin alanları <xref:System.Runtime.Serialization.ISerializable> çünkü bunlar kendi serileştirme mantığı sağlar.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için geçerli <xref:System.NonSerializedAttribute?displayProperty=fullName> getirilemeyen alanına öznitelik.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Yalnızca, bu kuraldan bir uyarıyı bastırmak bir <xref:System.Runtime.Serialization.ISerializationSurrogate?displayProperty=fullName> türü bildirilen serileştirilmiş ve seri durumdan alanın örneklerini sağlar.

## <a name="example"></a>Örnek

Aşağıdaki örnek, iki tür gösterir: bir kural ve kural karşılayan bir ihlal ediyor.

[!code-csharp[FxCop.Usage.MarkNonSerializable#1](../code-quality/codesnippet/CSharp/ca2235-mark-all-non-serializable-fields_1.cs)]
[!code-vb[FxCop.Usage.MarkNonSerializable#1](../code-quality/codesnippet/VisualBasic/ca2235-mark-all-non-serializable-fields_1.vb)]

## <a name="remarks"></a>Açıklamalar

CA2235 uygulayan türler analiz değil kural <xref:System.Runtime.Serialization.ISerializable> arabirimi (bunlar da ile işaretlenmediği sürece <xref:System.SerializableAttribute> özniteliği). Bunun nedeni, [CA2237 kural](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md) zaten uygulayan türler işaretleme önerir <xref:System.Runtime.Serialization.ISerializable> ile arabirim <xref:System.SerializableAttribute> özniteliği.

## <a name="related-rules"></a>İlgili kuralları

- [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)
- [CA2236: ISerializable türler üzerinde taban sınıf yöntemlerini çağırın](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)
- [CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)
- [CA2238: Serileştirme yöntemlerini doğru uygulama](../code-quality/ca2238-implement-serialization-methods-correctly.md)
- [CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)
- [CA2240: ISerializable'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)
- [CA2120: Serileştirme oluşturucularının güvenliğini sağlayın](../code-quality/ca2120-secure-serialization-constructors.md)