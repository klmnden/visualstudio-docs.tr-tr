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
ms.openlocfilehash: 2353c342b38a9dca42500c8997dcebb03137c91c
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55928549"
---
# <a name="ca2229-implement-serialization-constructors"></a>CA2229: Serileştirme oluşturucularını uygulayın

|||
|-|-|
|TypeName|ImplementSerializationConstructors|
|CheckId|CA2229|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Türün uyguladığı <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirim, temsilci veya arabirimi değil ve aşağıdaki koşullardan biri doğru:

- Tür, alan bir oluşturucu yok. bir <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName> nesnesi ve bir <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> nesnesi (seri hale getirme oluşturucusunu imzası).

- Korumasız bir türdür ve seri hale getirme oluşturucusuna ait erişim değiştiricisinin (Aile) korumalı değil.

- Tür Mühürlü olmadığı ve seri hale getirme oluşturucusuna ait erişim değiştiricisinin özel değildir.

## <a name="rule-description"></a>Kural açıklaması
 Bu kural, özel serileştirme destekleyen türler için geçerlidir. Bunu uygulayan bir tür özel serileştirme destekler <xref:System.Runtime.Serialization.ISerializable> arabirimi. Seri hale getirme oluşturucusunu seri durumdan veya kullanılarak serileştirilmiş nesneler yeniden oluşturmak için gerekli <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> yöntemi.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için seri hale getirme yapıcısını uygular. Kapalı bir sınıf için kurucusunu özel yapın; aksi takdirde korunmuş yapın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kural ihlalini bastırmayın. Türü seri durumdan olmayacaktır ve pek çok senaryoda çalışmaz.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kural karşılayan bir tür gösterir.

 [!code-csharp[FxCop.Usage.ISerializableCtor#1](../code-quality/codesnippet/CSharp/ca2229-implement-serialization-constructors_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName>
- <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName>
- <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName>