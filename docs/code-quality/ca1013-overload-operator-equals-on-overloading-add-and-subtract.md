---
title: 'CA1013: Toplama ve çıkarmayı aşırı yüklediğinizde eşittir işlecini aşırı yükleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- OverrideOperatorEqualsOnOverridingAddAndSubtract
- OverrideOperatorEqualsOnOverloadingAddAndSubtract
- CA1013
- OverloadOperatorEqualsOnOverloadingAddAndSubtract
helpviewer_keywords:
- OverrideOperatorEqualsOnOverloadingAddAndSubtract
- OverrideOperatorEqualsOnOverridingAddAndSubtract
- CA1013
- OverloadOperatorEqualsOnOverloadingAddAndSubtract
ms.assetid: 5bd28d68-c179-49ff-af47-5250b8b18a10
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 8c82e7303ea4016974be04c3d8745cb2011017f0
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923169"
---
# <a name="ca1013-overload-operator-equals-on-overloading-add-and-subtract"></a>CA1013: Toplama ve çıkarmayı aşırı yüklediğinizde eşittir işlecini aşırı yükleyin

|||
|-|-|
|TypeName|OverloadOperatorEqualsOnOverloadingAddAndSubtract|
|CheckId|CA1013|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir genel ya da korumalı tür eşitlik imlecini uygulamadan ekleme ya da çıkarma işleçlerini uygular.

## <a name="rule-description"></a>Kural açıklaması
Bir türün örnekleri toplama ve çıkarma gibi işlemler kullanılarak birleştirilebilmesi için `true` , aynı yapısal değerlere sahip olan her iki örnek için her zaman eşitlik tanımlamanız gerekir.

Eşitlik işlecinin aşırı yüklenmiş bir uygulamasında varsayılan eşitlik işlecini kullanamazsınız. Bunun yapılması, yığın taşmasına neden olur. Eşitlik işlecini uygulamak için uygulamanızdaki Object. Equals yöntemini kullanın. Aşağıdaki örnekte bakın.

```vb
If (Object.ReferenceEquals(left, Nothing)) Then
    Return Object.ReferenceEquals(right, Nothing)
Else
    Return left.Equals(right)
End If
```

```csharp
if (Object.ReferenceEquals(left, null))
    return Object.ReferenceEquals(right, null);
return left.Equals(right);
```

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için eşitlik işlecini, toplama ve çıkarma işleçleriyle matematik olarak tutarlı olacak şekilde uygulayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Eşitlik işlecinin varsayılan uygulanması tür için doğru davranışı sağlıyorsa, bu kuraldan bir uyarının görüntülenmesini güvenli hale getirir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden`BadAddableType`bir türü () tanımlar. Bu tür, eşitlik için aynı alan değerleri test `true` eden iki örnek oluşturmak için eşitlik işlecini uygulamalıdır. Tür `GoodAddableType` , düzeltilen uygulamayı gösterir. Bu türün aynı zamanda eşitsizlik işlecini ve diğer kuralları karşılamak için <xref:System.Object.Equals%2A> geçersiz kılmaları uyguladığını unutmayın. Ayrıca, uygulamanın tamamı de uygulanır <xref:System.Object.GetHashCode%2A>.

[!code-csharp[FxCop.Design.AddAndSubtract#1](../code-quality/codesnippet/CSharp/ca1013-overload-operator-equals-on-overloading-add-and-subtract_1.cs)]

## <a name="example"></a>Örnek
Aşağıdaki örnek, eşitlik operatörü için varsayılan ve doğru davranışı göstermek üzere bu konuda daha önce tanımlanan türlerin örneklerini kullanarak eşitlik için test eder.

[!code-csharp[FxCop.Design.TestAddAndSubtract#1](../code-quality/codesnippet/CSharp/ca1013-overload-operator-equals-on-overloading-add-and-subtract_2.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
Bad type:  {2,2} {2,2} are equal? No
Good type: {3,3} {3,3} are equal? Yes
Good type: {3,3} {3,3} are == ?   Yes
Bad type:  {2,2} {9,9} are equal? No
Good type: {3,3} {9,9} are == ?   No
```

## <a name="see-also"></a>Ayrıca bkz.

- [Eşitlik İşleçleri](/dotnet/standard/design-guidelines/equality-operators)