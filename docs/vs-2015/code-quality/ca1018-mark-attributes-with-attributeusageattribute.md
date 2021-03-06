---
title: 'CA1018: Öznitelikleri AttributeUsageAttribute ile işaretle | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1018
- MarkAttributesWithAttributeUsage
helpviewer_keywords:
- CA1018
- MarkAttributesWithAttributeUsage
ms.assetid: 6ab70ec0-220f-4880-af31-45067703133c
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a8b7cea6ea74b336c862cfe44f90e3e1ec54b2c2
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65704223"
---
# <a name="ca1018-mark-attributes-with-attributeusageattribute"></a>CA1018: Öznitelikleri AttributeUsageAttribute ile işaretle
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkAttributesWithAttributeUsage|
|CheckId|CA1018|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 <xref:System.AttributeUsageAttribute?displayProperty=fullName> Özniteliği özel özniteliği mevcut değil.

## <a name="rule-description"></a>Kural Tanımı
 Özel öznitelik tanımladığınızda, kullanarak işaretlemek <xref:System.AttributeUsageAttribute> özel öznitelik kaynak kodunun nerede uygulanabilir belirtmek için. Bir özniteliğin anlamı ve amaçlanan kullanımı, kodun içinde onun varolan konumunu tanımlar. Örneğin, kimin tutmaktan ve her tür kitaplığında geliştirme sorumludur ve sorumluluk her zaman tür düzeyinde atanan kişi tanımlayan bir öznitelik tanımlayabilir. Bu durumda, derleyiciler, sınıflar, numaralandırmalar ve arabirimler özniteliğini etkinleştirmeniz gerekir, ancak yöntemler, olaylar veya özellikler etkinleştirmemelisiniz. Kuruluş politikaları ve yordamları, öznitelik derlemelerini etkin olmadığını dikte.

 <xref:System.AttributeTargets?displayProperty=fullName> Numaralandırması için özel bir öznitelik belirtebilirsiniz hedefleri tanımlar. Atlarsanız <xref:System.AttributeUsageAttribute>, özel bir öznitelik tarafından tanımlandığı gibi tüm hedefler için geçerli olacağı `All` değerini <xref:System.AttributeTargets> sabit listesi.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için kullanarak özniteliği için hedefleri belirtin <xref:System.AttributeUsageAttribute>. Aşağıdaki örnekte bakın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 İleti hariç yerine bu kural ihlalini düzeltmek. Inherits özniteliği bile <xref:System.AttributeUsageAttribute>, öznitelik kod bakımı basitleştirmek için mevcut olmalıdır.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, iki öznitelikleri tanımlar. `BadCodeMaintainerAttribute` yanlış atlar <xref:System.AttributeUsageAttribute> deyimi ve `GoodCodeMaintainerAttribute` doğru Bu bölümde daha önce açıklanan özniteliğini uygular. Unutmayın özelliği `DeveloperName` tasarım kuralı tarafından gerekli [CA1019: Öznitelik bağımsız değişkenleri için erişimcileri tanımlayın](../code-quality/ca1019-define-accessors-for-attribute-arguments.md) ve bütünlük açısından dahil edilmiştir.

 [!code-csharp[FxCop.Design.AttributeUsage#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.AttributeUsage/cs/FxCop.Design.AttributeUsage.cs#1)]
 [!code-vb[FxCop.Design.AttributeUsage#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.AttributeUsage/vb/FxCop.Design.AttributeUsage.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1019: Öznitelik bağımsız değişkenleri için erişimcileri tanımlayın](../code-quality/ca1019-define-accessors-for-attribute-arguments.md)

 [CA1813: Korumasız özniteliklerden kaçının](../code-quality/ca1813-avoid-unsealed-attributes.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Öznitelikler](https://msdn.microsoft.com/library/ee0038ef-b247-4747-a650-3c5c5cd58d8b)
