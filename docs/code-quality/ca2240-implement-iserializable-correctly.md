---
title: "CA2240: ISerializable'ı doğru uygulayın"
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2240
- ImplementISerializableCorrectly
helpviewer_keywords:
- CA2240
- ImplementISerializableCorrectly
ms.assetid: cf05936d-0d6c-49ed-a1b4-220032e50b97
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 2640fddcde0d8777363a3c56e398e7ff307a20c7
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237874"
---
# <a name="ca2240-implement-iserializable-correctly"></a>CA2240: ISerializable'ı doğru uygulayın

|||
|-|-|
|TypeName|ImplementISerializableCorrectly|
|CheckId|CA2240|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Dışarıdan görünen bir tür <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirime atanabilir ve aşağıdaki koşullardan biri doğru olur:

- Tür devralınır, ancak <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> yöntemini geçersiz kılmaz ve tür, <xref:System.NonSerializedAttribute?displayProperty=fullName> özniteliğiyle işaretlenmemiş örnek alanlarını bildirir.

- Tür Sealed değildir ve tür dışarıdan görünmeyen ve geçersiz kılınabilir <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> bir yöntemi uygular.

## <a name="rule-description"></a>Kural açıklaması
<xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> Arabirimi devralan bir tür içinde belirtilen örnek alanları, serileştirme işlemine otomatik olarak dahil edilmez. Alanları eklemek için, türün <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemi ve serileştirme oluşturucusunu uygulaması gerekir. Alanlar serileştirilmemelidir, açıkça kararı göstermek için alanlara <xref:System.NonSerializedAttribute> özniteliğini uygulayın.

Korumalı olmayan türlerde, <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemin uygulamaları dışarıdan görünür olmalıdır. Bu nedenle, yöntemi türetilmiş türler tarafından çağrılabilir ve geçersiz kılınabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemi görünür ve geçersiz kılınabilir hale getirin ve tüm örnek alanlarının serileştirme işlemine eklendiğinden veya açıkça <xref:System.NonSerializedAttribute> özniteliğiyle işaretlenmiş olduğundan emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnekte, kuralı ihlal eden iki serileştirilebilir tür gösterilmektedir.

[!code-csharp[FxCop.Usage.ImplementISerializableCorrectly#1](../code-quality/codesnippet/CSharp/ca2240-implement-iserializable-correctly_1.cs)]
[!code-cpp[FxCop.Usage.ImplementISerializableCorrectly#1](../code-quality/codesnippet/CPP/ca2240-implement-iserializable-correctly_1.cpp)]
[!code-vb[FxCop.Usage.ImplementISerializableCorrectly#1](../code-quality/codesnippet/VisualBasic/ca2240-implement-iserializable-correctly_1.vb)]

## <a name="example"></a>Örnek
Aşağıdaki örnek, kitap sınıfında bir geçersiz kılınabilir uygulama <xref:System.Runtime.Serialization.ISerializable.GetObjectData> sağlayarak ve kitaplık sınıfında bir `GetObjectData` uygulamasını sağlayarak önceki iki ihlali düzeltir.

[!code-cpp[FxCop.Usage.ImplementISerializableCorrectly2#1](../code-quality/codesnippet/CPP/ca2240-implement-iserializable-correctly_2.cpp)]
[!code-csharp[FxCop.Usage.ImplementISerializableCorrectly2#1](../code-quality/codesnippet/CSharp/ca2240-implement-iserializable-correctly_2.cs)]
[!code-vb[FxCop.Usage.ImplementISerializableCorrectly2#1](../code-quality/codesnippet/VisualBasic/ca2240-implement-iserializable-correctly_2.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA2236 ISerializable türlerinde temel sınıf yöntemlerini çağırma](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)
- [CA2229 Serileştirme oluşturucularını Uygula](../code-quality/ca2229-implement-serialization-constructors.md)
- [CA2238 Serileştirme yöntemlerini doğru uygulayın](../code-quality/ca2238-implement-serialization-methods-correctly.md)
- [CA2235 Tüm seri hale getirilebilir olmayan alanları işaretle](../code-quality/ca2235-mark-all-non-serializable-fields.md)
- [CA2237 ISerializable türlerini SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)
- [CA2239 İsteğe bağlı alanlar için seri durumdan çıkarma yöntemleri sağlama](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)
- [CA2120 Güvenli serileştirme oluşturucuları](../code-quality/ca2120-secure-serialization-constructors.md)