---
title: 'CA1012: Soyut türlerin oluşturucuları olmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- AbstractTypesShouldNotHaveConstructors
- CA1012
helpviewer_keywords:
- CA1012
ms.assetid: 09f458ac-dd88-4cd7-a47f-4106c1e80ece
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: dd35cd7b084deb34b23b49ebc04517733c5478c9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006797"
---
# <a name="ca1012-abstract-types-should-not-have-constructors"></a>CA1012: Soyut türlerin oluşturucuları olmamalıdır

|||
|-|-|
|TypeName|AbstractTypesShouldNotHaveConstructors|
|CheckId|CA1012|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Genel bir türü soyuttur ve ortak yapıcıya sahip.

## <a name="rule-description"></a>Kural açıklaması
 Soyut türler üzerindeki kurucular yalnızca türetilen türler tarafından çağrılabilir. Ortak yapıcılar türün bir örneğini yaptığından ve siz bir soyut türün örneğini yapamayacağınızdan, soyut sınıf hatalı biçimde dizayn edilmiş ortak yapıcıya sahip olur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için korumalı Oluşturucu olun veya türü soyut olarak bildirmeyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Soyut tür, genel bir oluşturucusu vardır.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal soyut bir tür içeriyor.

 [!code-vb[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_1.vb)]
 [!code-csharp[FxCop.Design.AbstractTypeBad#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_1.cs)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek önceki ihlali oluşturucudan erişilebilirliğini değiştirerek giderir `public` için `protected`.

 [!code-csharp[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/CSharp/ca1012-abstract-types-should-not-have-constructors_2.cs)]
 [!code-vb[FxCop.Design.AbstractTypeGood#1](../code-quality/codesnippet/VisualBasic/ca1012-abstract-types-should-not-have-constructors_2.vb)]