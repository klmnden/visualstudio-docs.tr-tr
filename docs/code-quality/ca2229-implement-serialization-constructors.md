---
title: 'CA2229: Serileştirme oluşturucularını uygulayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2229
- ImplementSerializationConstructors
helpviewer_keywords:
- CA2229
- ImplementSerializationConstructors
ms.assetid: 8e04d5fe-dfad-445a-972e-0648324fac45
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 11dfa98bb348f874a2774454cc465fb80cb71750
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920159"
---
# <a name="ca2229-implement-serialization-constructors"></a>CA2229: Serileştirme oluşturucularını uygulayın

|||
|-|-|
|TypeName|ImplementSerializationConstructors|
|CheckId|CA2229|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Türü <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimini uygular, bir temsilci veya arabirim değildir ve aşağıdaki koşullardan biri doğru olur:

- Türün bir <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName> nesne <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> ve nesne alan bir oluşturucusu yok (serileştirme oluşturucusunun imzası).

- Tür korumasız ve serileştirme Oluşturucusu için erişim değiştiricisi korunmuyor (aile).

- Tür sealed ve serileştirme Oluşturucusu için erişim değiştiricisi özel değildir.

## <a name="rule-description"></a>Kural açıklaması
Bu kural, özel serileştirme desteği olan türler için geçerlidir. Bir tür, <xref:System.Runtime.Serialization.ISerializable> arabirimini uyguluyorsa özel Serileştirmeyi destekler. Serileştirme Oluşturucu, <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> yöntemi kullanılarak seri hale getirilen nesneleri seri durumdan çıkarmak veya yeniden oluşturmak için gereklidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini düzeltmek için seri hale getirme yapıcısını uygular. Kapalı bir sınıf için kurucusunu özel yapın; aksi takdirde korunmuş yapın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Kural ihlalini engellemez. Tür seri hale getirilebilir olmayacaktır ve birçok senaryoda çalışmayacaktır.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralını karşılayan bir türü gösterir.

[!code-csharp[FxCop.Usage.ISerializableCtor#1](../code-quality/codesnippet/CSharp/ca2229-implement-serialization-constructors_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2237 ISerializable türlerini SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName>
- <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName>
- <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName>