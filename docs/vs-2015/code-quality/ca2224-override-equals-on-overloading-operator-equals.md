---
title: 'CA2224: Geçersiz kılma eşittir eşittir işlecini aşırı yüklemesi üzerinde | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2224
- OverrideEqualsOnOverloadingOperatorEquals
- OverrideEqualsOnOverridingOperatorEquals
helpviewer_keywords:
- OverrideEqualsOnOverloadingOperatorEquals
- CA2224
ms.assetid: 7312afd9-84ba-417f-923e-7a159b53bf70
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: b4c16ed5858f18456af59c4cc26f2e0d56e6006a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54761361"
---
# <a name="ca2224-override-equals-on-overloading-operator-equals"></a>CA2224: Eşittir işlecini aşırı yüklerken Equals'ı geçersiz kılın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|OverrideEqualsOnOverloadingOperatorEquals|
|CheckId|CA2224|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Ortak tür eşitlik işlecini uygular, ancak geçersiz <xref:System.Object.Equals%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 Eşitlik işleci işlevselliğini erişmeye sözdizimsel olarak kullanışlı bir yol olması amaçlanmıştır <xref:System.Object.Equals%2A> yöntemi. Eşitlik işleci uygularsanız, mantıksal olarak aynı olmalıdır <xref:System.Object.Equals%2A>.

 Kodunuzu bu kuralı ihlal ediyorsa C# derleyicisinin bir uyarı verir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için eşitlik işlecini uygulamasını kaldırmak, ya da geçersiz kılma <xref:System.Object.Equals%2A> ve iki yöntem dönüş değerlerine sahip. Eşitlik işleci tutarsız davranışa sebep değil, uygulaması sağlayarak ihlali düzeltebilirsiniz <xref:System.Object.Equals%2A> çağrılarının <xref:System.Object.Equals%2A> yöntemi temel sınıf.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Eşitlik işleci'nın devralınmış uygulaması aynı değer döndürürse bu kuraldan bir uyarıyı bastırmak güvenlidir <xref:System.Object.Equals%2A>. Örnek bölümünde, güvenli bir şekilde bu kuraldan bir uyarıyı bastırmak bir tür içerir.

## <a name="examples-of-inconsistent-equality-definitions"></a>Tutarsız eşitlik tanımları örnekleri

### <a name="description"></a>Açıklama
 Aşağıdaki örnek, bir tür eşitlik tutarsız tanımlarını içeren gösterir. `BadPoint` Eşitlik anlamını eşitlik işlecini bir özel uygulanışı sağlayarak değişir, ancak geçersiz <xref:System.Object.Equals%2A> böylece aynı şekilde davranır.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Usage.OperatorEqualsRequiresEquals#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.OperatorEqualsRequiresEquals/cs/FxCop.Usage.OperatorEqualsRequiresEquals.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki kod, davranışı testleri `BadPoint`.

 [!code-csharp[FxCop.Usage.TestOperatorEqualsRequiresEquals#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.TestOperatorEqualsRequiresEquals/cs/FxCop.Usage.TestOperatorEqualsRequiresEquals.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **bir = ([0] 1,1) ve b = ([1] 2,2) eşit? Hayır**
**bir b ==? Hayır**
**a1 ve bir eşit? Evet**
**a1 == bir? Evet**
**b ve bcopy eşit? Hayır**
**b bcopy ==? Evet**
## <a name="example"></a>Örnek
 Aşağıdaki örnek, teknik olarak bu kuralı ihlal ediyor, ancak tutarlı bir şekilde davranmaz bir tür gösterir.

 [!code-csharp[FxCop.Usage.ValueTypeEquals#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.ValueTypeEquals/cs/FxCop.Usage.ValueTypeEquals.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki kod, davranışı testleri `GoodPoint`.

 [!code-csharp[FxCop.Usage.TestValueTypeEquals#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.TestValueTypeEquals/cs/FxCop.Usage.TestValueTypeEquals.cs#1)]

 Bu örnek aşağıdaki çıktıyı üretir.

 **bir = (1,1) ve b = (2,2) eşit? Hayır**
**bir b ==? Hayır**
**a1 ve bir eşit? Evet**
**a1 == bir? Evet**
**b ve bcopy eşit? Evet**
**b bcopy ==? Evet**
## <a name="class-example"></a>Sınıf örneği

### <a name="description"></a>Açıklama
 Aşağıdaki örnek bu kuralı ihlal eden bir sınıf (başvuru türü) gösterir.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Usage.OverrideEqualsClassViolation#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.OverrideEqualsClassViolation/cs/FxCop.Usage.OverrideEqualsClassViolation.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, geçersiz kılarak ihlali düzeltmeleri <xref:System.Object.Equals%2A?displayProperty=fullName>.

 [!code-csharp[FxCop.Usage.OverrideEqualsClassFixed#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.OverrideEqualsClassFixed/cs/FxCop.Usage.OverrideEqualsClassFixed.cs#1)]

## <a name="structure-example"></a>Yapısı örneği

### <a name="description"></a>Açıklama
 Aşağıdaki örnek bu kuralı ihlal eden bir yapı (değer türü) gösterir.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Usage.OverrideEqualsStructViolation#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.OverrideEqualsStructViolation/cs/FxCop.Usage.OverrideEqualsStructViolation.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, geçersiz kılarak ihlali düzeltmeleri <xref:System.ValueType.Equals%2A?displayProperty=fullName>.

 [!code-csharp[FxCop.Usage.OverrideEqualsStructFixed#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.OverrideEqualsStructFixed/cs/FxCop.Usage.OverrideEqualsStructFixed.cs#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1046: Başvuru türlerinde eşittir işleçlerini aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)

 [CA2225: İşleç aşırı yüklemeleri adlandırılmış Alternatiflere sahiptir](../code-quality/ca2225-operator-overloads-have-named-alternates.md)

 [CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

 [CA2218: Gethashcode'u eşittir geçersiz kılmada geçersiz kıl](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)

 [CA2231: Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)
