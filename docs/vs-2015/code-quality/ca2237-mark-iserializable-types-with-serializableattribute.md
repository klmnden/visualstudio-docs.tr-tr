---
title: 'CA2237: İşareti ISerializable türleri SerializableAttribute ile | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2237
- MarkISerializableTypesWithSerializable
helpviewer_keywords:
- MarkISerializableTypesWithSerializable
- CA2237
ms.assetid: 9bd6bb24-a527-43dd-9952-043c0c694f46
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f9d75a75449a07a5e9f651be0ba61598a29674ab
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201534"
---
# <a name="ca2237-mark-iserializable-types-with-serializableattribute"></a>CA2237: ISerializable türleri SerializableAttribute ile işaretleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkISerializableTypesWithSerializable|
|CheckId|CA2237|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir türün uyguladığı <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimi ve türü olarak işaretlenmemiş ile <xref:System.SerializableAttribute?displayProperty=fullName> özniteliği. Kural türetilen türler, temel türü seri hale getirilebilir değil yok sayar.

## <a name="rule-description"></a>Kural Tanımı
 Ortak dil çalışma zamanı tarafından seri hale getirilebilir olarak tanınması için türleri ile işaretlenmelidir <xref:System.SerializableAttribute> bir uygulaması aracılığıyla özel seri hale getirme yordamı tür kullansa bile özniteliği <xref:System.Runtime.Serialization.ISerializable> arabirimi.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için geçerli <xref:System.SerializableAttribute> öznitelik türü için.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Uygulama etki alanları arasında düzgün çalışması için seri hale getirilebilir olması gerekir çünkü özel durum sınıfları için bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kuralını ihlal eden bir tür gösterir. Açıklamadan çıkarın <xref:System.SerializableAttribute> özniteliği kural karşılamak için satır.

 [!code-csharp[FxCop.Usage.MarkSerializable#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.MarkSerializable/cs/FxCop.Usage.MarkSerializable.cs#1)]
 [!code-vb[FxCop.Usage.MarkSerializable#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.MarkSerializable/vb/FxCop.Usage.MarkSerializable.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2236: ISerializable türler üzerinde taban sınıf yöntemlerini çağırın](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)

 [CA2240: ISerializable'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)

 [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)

 [CA2238: Serileştirme yöntemlerini doğru uygulama](../code-quality/ca2238-implement-serialization-methods-correctly.md)

 [CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin](../code-quality/ca2235-mark-all-non-serializable-fields.md)

 [CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)

 [CA2120: Serileştirme oluşturucularının güvenliğini sağlayın](../code-quality/ca2120-secure-serialization-constructors.md)
