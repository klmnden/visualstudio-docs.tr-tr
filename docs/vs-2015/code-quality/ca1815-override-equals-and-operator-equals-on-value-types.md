---
title: 'CA1815: Geçersiz kılma eşittir ve işleç değer türlerinde | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1815
- OverrideEqualsAndOperatorEqualsOnValueTypes
helpviewer_keywords:
- OverrideEqualsAndOperatorEqualsOnValueTypes
- CA1815
ms.assetid: 0a8ab3a3-ee8e-46f7-985d-dcf00c89363b
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e21585a7a56fde2fb46ea86adde92eecfd1a4565
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201691"
---
# <a name="ca1815-override-equals-and-operator-equals-on-value-types"></a>CA1815: Değer türlerinde eşittir ve işleç eşittiri geçersiz kılın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|OverrideEqualsAndOperatorEqualsOnValueTypes|
|CheckId|CA1815|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Genel değer türü geçersiz <xref:System.Object.Equals%2A?displayProperty=fullName>, veya eşitlik operatörünün (==) uygulamıyor. Bu kural, sabit listeleri denetlemez.

## <a name="rule-description"></a>Kural Tanımı
 Değer türleri için ' ın devralınmış uygulaması <xref:System.Object.Equals%2A> Reflection kitaplığını kullanır ve tüm alanların içeriğini karşılaştırır. Yansıma hesaplama açısından pahalıdır ve her alan için eşitlik karşılaştırma gereksiz olabilir. Karşılaştırma ya da sıralama örnekleri için kullanıcıların ya da tablo anahtarlarını karma olarak kullandığınız, değer türünüz uygulamalıdır <xref:System.Object.Equals%2A>. İşleç aşırı yüklemesi programlama dilini destekler, ayrıca eşitlik ve eşitsizlik işleci bir uygulama sağlamalıdır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için bir uygulamasını sağlamak <xref:System.Object.Equals%2A>. Mümkünse, eşitlik işlecini uygular.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Değer türü örneklerini birbirine karşılaştırılmayacak varsa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example-of-a-violation"></a>Bir ihlali örneği

### <a name="description"></a>Açıklama
 Aşağıdaki örnek bu kuralı ihlal eden bir yapı (değer türü) gösterir.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Performance.OverrideEqualsViolation#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.OverrideEqualsViolation/cs/FxCop.Performance.OverrideEqualsViolation.cs#1)]

## <a name="example-of-how-to-fix"></a>İlişkin bir örnek için düzeltme

### <a name="description"></a>Açıklama
 Aşağıdaki örnek önceki ihlali geçersiz kılarak düzeltmeleri <xref:System.ValueType.Equals%2A?displayProperty=fullName> ve eşitlik işleçleri (==,! =).

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Performance.OverrideEqualsFixed#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.OverrideEqualsFixed/cs/FxCop.Performance.OverrideEqualsFixed.cs#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2224: Eşittir işlecini aşırı yüklemesi üzerinde geçersiz kılma değerine eşittir](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)

 [CA2231: Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)

 [CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.Object.Equals%2A?displayProperty=fullName>
