---
title: 'CA1820: Dize uzunluğunu kullanarak boş dizeleri test | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- TestForEmptyStringsUsingStringLength
- CA1820
helpviewer_keywords:
- TestForEmptyStringsUsingStringLength
- CA1820
ms.assetid: da1e70c8-b1dc-46b9-8b8f-4e6e48339681
caps.latest.revision: 23
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bebd3b78881f9e1a2f4908ea667f80cbd7b98dd6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54776854"
---
# <a name="ca1820-test-for-empty-strings-using-string-length"></a>CA1820: Dize uzunluğunu kullanarak boş dizeleri test edin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TestForEmptyStringsUsingStringLength|
|CheckId|CA1820|
|Kategori|Microsoft.Performance|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir dize kullanarak boş bir dize karşılaştırma <xref:System.Object.Equals%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 Karşılaştırma dizeleri kullanarak <xref:System.String.Length%2A?displayProperty=fullName> özelliği veya <xref:System.String.IsNullOrEmpty%2A?displayProperty=fullName> yöntemdir kullanılmasından önemli ölçüde daha hızlı <xref:System.Object.Equals%2A>. Bunun nedeni, <xref:System.Object.Equals%2A> ya da daha fazla MSIL yönergeleri yürüten <xref:System.String.IsNullOrEmpty%2A> veya yönerge almak için yürütülen sayısını <xref:System.String.Length%2A> özellik değer ve sıfır olarak karşılaştırır.

 Bilmeniz gereken, <xref:System.Object.Equals%2A> ve <xref:System.String.Length%2A> == 0 null dizeler için farklı davranır. Değeri alınacak çalışırsanız <xref:System.String.Length%2A> boş bir dize özelliği, ortak dil çalışma zamanı oluşturur bir <xref:System.NullReferenceException?displayProperty=fullName>. Boş bir dize ve boş bir dize arasında bir karşılaştırma gerçekleştirmek, ortak dil çalışma zamanı bir özel durum oluşturmaz; Karşılaştırma döndürür `false`. Null sınaması, bu iki yaklaşımı göreli performansını önemli ölçüde etkilemez. Hedeflenirken [!INCLUDE[dnprdnlong](../includes/dnprdnlong-md.md)], kullanın <xref:System.String.IsNullOrEmpty%2A> yöntemi. Aksi takdirde kullanın <xref:System.String.Length%2A> karşılaştırma mümkün olduğunca ==.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için kullanılacak karşılaştırma değiştirme <xref:System.String.Length%2A> özelliği ve test için boş bir dize. Hedefleme, [!INCLUDE[dnprdnlong](../includes/dnprdnlong-md.md)], kullanın <xref:System.String.IsNullOrEmpty%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Performans sorunu değilse bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, boş bir dize aramak için kullanılan farklı teknikleri gösterir.

 [!code-csharp[FxCop.Performance.StringTest#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.StringTest/cs/FxCop.Performance.StringTest.cs#1)]
