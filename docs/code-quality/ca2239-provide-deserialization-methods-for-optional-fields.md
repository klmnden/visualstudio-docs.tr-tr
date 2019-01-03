---
title: 'CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 572bf56c63e8fcbf9d78738d7cdffcf9540df158
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53988971"
---
# <a name="ca2239-provide-deserialization-methods-for-optional-fields"></a>CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.

|||
|-|-|
|TypeName|ProvideDeserializationMethodsForOptionalFields|
|CheckId|CA2239|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir tür ile işaretlenmiş bir alana sahip <xref:System.Runtime.Serialization.OptionalFieldAttribute?displayProperty=fullName> özniteliği ve tür, yöntemlerinin yönetilmesi serinin olay sağlamaz.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.Runtime.Serialization.OptionalFieldAttribute> Özniteliği seri hale getirme üzerinde hiçbir etkisi; özniteliği ile işaretlenmiş bir alan serileştirilmiş. Ancak, alan serinin üzerinde göz ardı edilir ve onun türü ile ilişkili varsayılan değerini korur. Serinin işlemi sırasında alan ayarlamak için serinin olay işleyicileri bildirilmesi gerekir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için serinin olay işleme türüne yöntemi ekleyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Alan bir serinin işlemi sırasında dikkate alınması durumunda bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür bir isteğe bağlı alan ve serinin olay işleme yöntemleri gösterir.

 [!code-csharp[FxCop.Usage.OptionalFields#1](../code-quality/codesnippet/CSharp/ca2239-provide-deserialization-methods-for-optional-fields_1.cs)]
 [!code-vb[FxCop.Usage.OptionalFields#1](../code-quality/codesnippet/VisualBasic/ca2239-provide-deserialization-methods-for-optional-fields_1.vb)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2236: ISerializable türler üzerinde taban sınıf yöntemlerini çağırın](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)

 [CA2240: ISerializable'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)

 [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)

 [CA2238: Serileştirme yöntemlerini doğru uygulama](../code-quality/ca2238-implement-serialization-methods-correctly.md)

 [CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin](../code-quality/ca2235-mark-all-non-serializable-fields.md)

 [CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

 [CA2120: Serileştirme oluşturucularının güvenliğini sağlayın](../code-quality/ca2120-secure-serialization-constructors.md)