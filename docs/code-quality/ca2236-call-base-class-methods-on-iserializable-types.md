---
title: 'CA2236: ISerializable türler üzerinde taban sınıf metotlarını çağırın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2236
- CallBaseClassMethodsOnISerializableTypes
helpviewer_keywords:
- CA2236
- CallBaseClassMethodsOnISerializableTypes
ms.assetid: 5a15b20d-769c-4640-b31a-36e07077daae
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 3f0075a6296e839030448c0209c77f1717a5fcb1
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920118"
---
# <a name="ca2236-call-base-class-methods-on-iserializable-types"></a>CA2236: ISerializable türler üzerinde taban sınıf metotlarını çağırın

|||
|-|-|
|TypeName|CallBaseClassMethodsOnISerializableTypes|
|CheckId|CA2236|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir tür, <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimini uygulayan bir türden türetilir ve aşağıdaki koşullardan biri doğrudur:

- Türü serileştirme oluşturucusunu, diğer bir deyişle, <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName> <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> parametre imzasına sahip bir oluşturucuyu uygular, ancak temel türün serileştirme oluşturucusunu çağırmaz.

- Türü yöntemini uygular, <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> ancak temel türünün <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemini çağırmaz.

## <a name="rule-description"></a>Kural açıklaması
Özel bir serileştirme işleminde, bir tür alanları seri hale <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> getirmek için alanları ve serileştirme oluşturucusunu, alanları seri hale getirmek için uygular. Tür, <xref:System.Runtime.Serialization.ISerializable> arabirimini uygulayan bir türden türetildiğinden, <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> temel tür yöntemi ve serileştirme Oluşturucusu, taban türünün alanlarını seri hale getirmek/devre dışı bırakmak için çağrılmalıdır. Aksi takdirde, tür serileştirilmez ve doğru şekilde serileştirilmez. Türetilmiş tür hiçbir yeni alan eklememişse, türün <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemi veya serileştirme oluşturucusunu uygulaması veya temel tür eşdeğerlerini çağırması gerekmez.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, karşılık gelen türetilmiş tür yönteminden <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> veya oluşturucusundan temel tür yöntemini veya serileştirme oluşturucusunu çağırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bir temel sınıfın serileştirme oluşturucusunu ve <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> metodunu çağırarak kuralı karşılayan bir türetilmiş türü gösterir.

[!code-vb[FxCop.Usage.CallBaseISerializable#1](../code-quality/codesnippet/VisualBasic/ca2236-call-base-class-methods-on-iserializable-types_1.vb)]
[!code-csharp[FxCop.Usage.CallBaseISerializable#1](../code-quality/codesnippet/CSharp/ca2236-call-base-class-methods-on-iserializable-types_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2240 ISerializable 'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)

[CA2229 Serileştirme oluşturucularını Uygula](../code-quality/ca2229-implement-serialization-constructors.md)

[CA2238 Serileştirme yöntemlerini doğru uygulayın](../code-quality/ca2238-implement-serialization-methods-correctly.md)

[CA2235 Tüm seri hale getirilebilir olmayan alanları işaretle](../code-quality/ca2235-mark-all-non-serializable-fields.md)

[CA2237 ISerializable türlerini SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

[CA2239 İsteğe bağlı alanlar için seri durumdan çıkarma yöntemleri sağlama](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)

[CA2120 Güvenli serileştirme oluşturucuları](../code-quality/ca2120-secure-serialization-constructors.md)