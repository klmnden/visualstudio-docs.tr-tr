---
title: "CA2240: ISerializable'ı doğru uygulayın | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2240
- ImplementISerializableCorrectly
helpviewer_keywords:
- CA2240
- ImplementISerializableCorrectly
ms.assetid: cf05936d-0d6c-49ed-a1b4-220032e50b97
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 37f84bff4802c703bb61b36e9c1933a31cd6c5e3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68142361"
---
# <a name="ca2240-implement-iserializable-correctly"></a>CA2240: ISerializable'ı doğru uygulayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ImplementISerializableCorrectly|
|CheckId|CA2240|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Dışarıdan görünen tür özelleşmemiş <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimi ve aşağıdaki koşullar doğruysa:

- Tür devralır, ancak geçersiz <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> yöntemi ve türü ile işaretli olmayan örnek alanlarını bildirir <xref:System.NonSerializedAttribute?displayProperty=fullName> özniteliği.

- Tür korumalı değil ve türün uyguladığı bir <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> dışarıdan görünür ve geçersiz kılınabilir bir yöntemi.

## <a name="rule-description"></a>Kural Tanımı
 Örnek, devralınan bir türde bildirilen alanları <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimi seri hale getirme işleminde otomatik olarak bulunmaz. Tür alanları içerecek şekilde uygulamalıdır <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemi ve Serileştirme Oluşturucu. Alanları serileştirilecek değil, uygulama <xref:System.NonSerializedAttribute> alanları kararı açıkça belirtmek için özniteliği.

 Uygulamaları mühürlendi olmayan türlerde <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemi dışarıdan görünür. Bu nedenle, yöntem, türetilen türler tarafından çağrılabilir ve geçersiz kılınabilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için olun <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> yöntemi geçersiz kılınabilir ve tüm örnek alanları seri hale getirme işlemine dahil veya açıkça işaretli olduğundan emin olun <xref:System.NonSerializedAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kural ihlal iki serializable türler gösterir.

 [!code-cpp[FxCop.Usage.ImplementISerializableCorrectly#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Usage.ImplementISerializableCorrectly/cpp/FxCop.Usage.ImplementISerializableCorrectly.cpp#1)]
 [!code-csharp[FxCop.Usage.ImplementISerializableCorrectly#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.ImplementISerializableCorrectly/cs/FxCop.Usage.ImplementISerializableCorrectly.cs#1)]
 [!code-vb[FxCop.Usage.ImplementISerializableCorrectly#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.ImplementISerializableCorrectly/vb/FxCop.Usage.ImplementISerializableCorrectly.vb#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek iki önceki ihlalleri [ISerializable.GetObjectData] (geçersiz kılınabilir uygulaması sağlayarak giderir<!-- TODO: review code entity reference <xref:assetId:///ISerializable.GetObjectData?qualifyHint=False&amp;autoUpgrade=False>  -->) uygulaması sağlayarak ve kitap sınıfı hakkında <!-- TODO: review code entity reference <xref:assetId:///ISerializable.GetObjectData?qualifyHint=False&amp;autoUpgrade=False>  --> için kitaplık sınıfı.

 [!code-cpp[FxCop.Usage.ImplementISerializableCorrectly2#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Usage.ImplementISerializableCorrectly2/cpp/FxCop.Usage.ImplementISerializableCorrectly2.cpp#1)]
 [!code-csharp[FxCop.Usage.ImplementISerializableCorrectly2#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.ImplementISerializableCorrectly2/cs/FxCop.Usage.ImplementISerializableCorrectly2.cs#1)]
 [!code-vb[FxCop.Usage.ImplementISerializableCorrectly2#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.ImplementISerializableCorrectly2/vb/FxCop.Usage.ImplementISerializableCorrectly2.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2236: ISerializable türler üzerinde taban sınıf yöntemlerini çağırın](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)

 [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)

 [CA2238: Serileştirme yöntemlerini doğru uygulama](../code-quality/ca2238-implement-serialization-methods-correctly.md)

 [CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin](../code-quality/ca2235-mark-all-non-serializable-fields.md)

 [CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

 [CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)

 [CA2120: Serileştirme oluşturucularının güvenliğini sağlayın](../code-quality/ca2120-secure-serialization-constructors.md)
