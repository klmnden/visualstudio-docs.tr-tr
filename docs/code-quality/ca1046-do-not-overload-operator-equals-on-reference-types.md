---
title: 'CA1046: Eşittir işlecini başvuru türlerinde aşırı yüklemeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotOverloadOperatorEqualsOnReferenceTypes
- CA1046
helpviewer_keywords:
- CA1046
- DoNotOverloadOperatorEqualsOnReferenceTypes
ms.assetid: c1dfbfe3-63f9-4005-a81a-890427b77e79
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9f9304fcd86a9b36a729b1436fe16471b449ac0d
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55953769"
---
# <a name="ca1046-do-not-overload-operator-equals-on-reference-types"></a>CA1046: Eşittir işlecini başvuru türlerinde aşırı yüklemeyin

|||
|-|-|
|TypeName|DoNotOverloadOperatorEqualsOnReferenceTypes|
|CheckId|CA1046|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir ortak veya iç içe geçmiş genel başvuru türü eşitlik işlecini aşırı yüklemeleri.

## <a name="rule-description"></a>Kural açıklaması
 Başvuru türleri için, varsayılan eşitlik işleci neredeyse her zaman doğrudur. Varsayılan olarak, yalnızca aynı nesneye gelirseniz iki başvuru eşit olur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için eşitlik işlecini uygulamasını kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Başvuru türü davranacağını gibi yerleşik değer türünde olduğunda bu kuraldan bir uyarıyı bastırmak güvenlidir. Ekleme veya çıkarma türü örneklerinde yapmak için anlamlı olması durumunda, eşitlik işlecini uygulamak ve ihlalin bastırmak muhtemelen doğrudur.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, iki başvuru karşılaştırılırken varsayılan davranış gösterir.

 [!code-csharp[FxCop.Design.RefTypesNoEqualityOp#1](../code-quality/codesnippet/CSharp/ca1046-do-not-overload-operator-equals-on-reference-types_1.cs)]

## <a name="example"></a>Örnek

Aşağıdaki uygulama bazı başvuruları karşılaştırır.

[!code-csharp[FxCop.Design.TestRefTypesNoEqualityOp#1](../code-quality/codesnippet/CSharp/ca1046-do-not-overload-operator-equals-on-reference-types_2.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
a = new (2,2) and b = new (2,2) are equal? No
c and a are equal? Yes
b and a are == ? No
c and a are == ? Yes
```

## <a name="related-rules"></a>İlgili kuralları

[CA1013: Aşırı yükleme aşırı yükleme eşittir işlecini ekleme ve çıkarma](../code-quality/ca1013-overload-operator-equals-on-overloading-add-and-subtract.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Object.Equals%2A?displayProperty=fullName>
- [Eşitlik İşleçleri](/dotnet/standard/design-guidelines/equality-operators)