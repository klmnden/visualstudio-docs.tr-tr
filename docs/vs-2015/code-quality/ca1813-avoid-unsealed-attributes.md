---
title: 'CA1813: Korumasız özniteliklerden kaçının | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1813
- AvoidUnsealedAttributes
helpviewer_keywords:
- CA1813
- AvoidUnsealedAttributes
ms.assetid: f5e31b4c-9f8b-49e1-a2a8-bb5f1140729a
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1581049a0899cd7c8ed7898b3099800a9e68795a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54756219"
---
# <a name="ca1813-avoid-unsealed-attributes"></a>CA1813: Mühürsüz özniteliklerden kaçının
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|AvoidUnsealedAttributes|
|CheckId|CA1813|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir ortak türün devraldığı <xref:System.Attribute?displayProperty=fullName>soyut ve korumalı değil (`NotInheritable` Visual Basic'te).

## <a name="rule-description"></a>Kural Tanımı
 [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] Sınıf kitaplığı özel öznitelikleri almak için yöntemler sağlar. Varsayılan olarak, bu yöntemleri öznitelik devralma hiyerarşisinde arar; Örneğin <xref:System.Attribute.GetCustomAttribute%2A?displayProperty=fullName> belirtilen öznitelik türünün veya belirtilen öznitelik türü genişleten herhangi bir öznitelik türü arar. Öznitelik mühürleme kalıtım hiyerarşisi aracılığıyla aramayı ortadan kaldırır ve performansı artırabilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için öznitelik türünü mühürleyin veya soyut olun.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak güvenlidir. Yalnızca, bir öznitelik hiyerarşisi tanımlama ve öznitelik mühürleme ya da soyut yapmak varsa bunu yapmanız gerekir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bu kural karşılayan özel bir öznitelik gösterir.

 [!code-csharp[FxCop.Performance.AttributesSealed#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.AttributesSealed/cs/FxCop.Performance.AttributesSealed.cs#1)]
 [!code-vb[FxCop.Performance.AttributesSealed#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Performance.AttributesSealed/vb/FxCop.Performance.AttributesSealed.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1019: Öznitelik bağımsız değişkenleri için erişimcileri tanımlayın](../code-quality/ca1019-define-accessors-for-attribute-arguments.md)

 [CA1018: Öznitelikleri AttributeUsageAttribute ile işaretle](../code-quality/ca1018-mark-attributes-with-attributeusageattribute.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Öznitelikler](http://msdn.microsoft.com/library/ee0038ef-b247-4747-a650-3c5c5cd58d8b)
