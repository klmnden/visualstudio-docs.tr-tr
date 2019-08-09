---
title: 'CA1018: Öznitelikleri AttributeUsageAttribute ile işaretle'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1018
- MarkAttributesWithAttributeUsage
helpviewer_keywords:
- CA1018
- MarkAttributesWithAttributeUsage
ms.assetid: 6ab70ec0-220f-4880-af31-45067703133c
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 78917bcd4c67e1da205595bac07c8e0e5947318d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923065"
---
# <a name="ca1018-mark-attributes-with-attributeusageattribute"></a>CA1018: Öznitelikleri AttributeUsageAttribute ile işaretle

|||
|-|-|
|TypeName|MarkAttributesWithAttributeUsage|
|CheckId|CA1018|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
<xref:System.AttributeUsageAttribute?displayProperty=fullName> Özniteliği özel öznitelikte yok.

## <a name="rule-description"></a>Kural açıklaması
Özel bir öznitelik tanımladığınızda, kaynak kodda özel özniteliğin nerede uygulanabileceğini belirtmek için öğesini kullanarak <xref:System.AttributeUsageAttribute> işaretleyin. Bir özniteliğin anlamı ve amaçlanan kullanımı, kodun içinde onun varolan konumunu tanımlar. Örneğin, bir kitaplıktaki her bir türü korumadan ve artırmaktan sorumlu kişiyi tanımlayan bir öznitelik tanımlayabilir ve bu sorumluluk her zaman tür düzeyinde atanır. Bu durumda, derleyiciler sınıflarda, numaralandırmalar ve arabirimlerde özniteliği etkinleştirmeli, ancak Yöntemler, olaylar veya özelliklerde etkinleştirilmemelidir. Kuruluş ilkeleri ve yordamları, özniteliğin derlemelerde etkinleştirilmesi gerekip gerekmediğini de belirler.

Sabit <xref:System.AttributeTargets?displayProperty=fullName> listesi, özel bir öznitelik için belirtebileceğiniz hedefleri tanımlar. Atlanırsa <xref:System.AttributeUsageAttribute>, özel özniteleme, <xref:System.AttributeTargets> numaralandırma `All` değeri tarafından tanımlanan tüm hedefler için geçerli olacaktır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, kullanarak <xref:System.AttributeUsageAttribute>özniteliği için hedefleri belirtin. Aşağıdaki örnekte bakın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
İletiyi dışlamak yerine bu kuralın ihlal edildiğini düzeltmelisiniz. Özniteliği devralsa <xref:System.AttributeUsageAttribute>bile, kod bakımını basitleştirmek için özniteliği bulunmalıdır.

## <a name="example"></a>Örnek
Aşağıdaki örnek iki özniteliği tanımlar. `BadCodeMaintainerAttribute`<xref:System.AttributeUsageAttribute> ifadeyi yanlış bir şekilde atlar ve `GoodCodeMaintainerAttribute` bu bölümde daha önce açıklanan özniteliği doğru şekilde uygular. CA1019 tasarım kuralına [yönelik `DeveloperName` özelliğin gerekli olduğunu unutmayın: Öznitelik bağımsız değişkenleri](../code-quality/ca1019-define-accessors-for-attribute-arguments.md) için erişimcileri tanımlayın ve tamamlana için dahil edilmiştir.

[!code-csharp[FxCop.Design.AttributeUsage#1](../code-quality/codesnippet/CSharp/ca1018-mark-attributes-with-attributeusageattribute_1.cs)]
[!code-vb[FxCop.Design.AttributeUsage#1](../code-quality/codesnippet/VisualBasic/ca1018-mark-attributes-with-attributeusageattribute_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA1019 Öznitelik bağımsız değişkenleri için erişimcileri tanımlayın](../code-quality/ca1019-define-accessors-for-attribute-arguments.md)

[CA1813 Korumasız özniteliklerden kaçının](../code-quality/ca1813-avoid-unsealed-attributes.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Öznitelikler](/dotnet/standard/design-guidelines/attributes)