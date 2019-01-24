---
title: 'CA1002: Genel listeleri gösterme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotExposeGenericLists
- CA1002
helpviewer_keywords:
- CA1002
- DoNotExposeGenericLists
ms.assetid: 5caac810-1a79-47df-a27b-c46c5040bf34
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c438514263d9934f70927b46c8d1c9130746a06f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754081"
---
# <a name="ca1002-do-not-expose-generic-lists"></a>CA1002: Genel listeleri gösterme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotExposeGenericLists|
|CheckId|CA1002|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir türü olan dışarıdan görünen üye içeren bir <xref:System.Collections.Generic.List%601?displayProperty=fullName> türü, döndürür bir <xref:System.Collections.Generic.List%601?displayProperty=fullName> türü veya imzası içerir bir <xref:System.Collections.Generic.List%601?displayProperty=fullName> parametresi.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Collections.Generic.List%601?displayProperty=fullName> Performans ve değil devralma için tasarlanmış bir genel koleksiyondur. <xref:System.Collections.Generic.List%601?displayProperty=fullName> devralınan bir sınıf davranışını değiştirmek kolaylaştıran sanal üyeyi içermiyor. Aşağıdaki genel koleksiyonlar devralma için tasarlanmış ve yerine açılmamalıdır <xref:System.Collections.Generic.List%601?displayProperty=fullName>.

-   <xref:System.Collections.ObjectModel.Collection%601?displayProperty=fullName>

-   <xref:System.Collections.ObjectModel.ReadOnlyCollection%601?displayProperty=fullName>

-   <xref:System.Collections.ObjectModel.KeyedCollection%602?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için değiştirme <xref:System.Collections.Generic.List%601?displayProperty=fullName> devralma için tasarlanmış genel koleksiyonlar birine türü.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu uyarıyı oluşturan derleme yeniden kullanılabilir bir kitaplık tasarlanmamıştır sürece bu kuraldan bir uyarıyı bastırmayın. Örneğin, bunun bir performans kazancı genel listeleri kullanımdan burada elde ayarlanmış performans uygulamasında bu uyarının gösterilmemesi güvenli olur.

## <a name="related-rules"></a>İlgili kuralları
 [CA1005: Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)

 [CA1010: Koleksiyonlar genel arabirim uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

 [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

 [CA1006: Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)

 [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

 [CA1003: Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)

 [CA1007: Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Genel Türler](http://msdn.microsoft.com/library/75ea8509-a4ea-4e7a-a2b3-cf72482e9282)
