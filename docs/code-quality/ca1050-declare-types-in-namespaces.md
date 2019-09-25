---
title: 'CA1050: Ad alanlarında türler bildirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1050
- DeclareTypesInNamespaces
helpviewer_keywords:
- DeclareTypesInNamespaces
- CA1050
ms.assetid: 1002748d-ac8d-404f-85dd-7a12d1ad3e05
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 8127c68cfe7eb541b8adea8affad99027e0c1fe7
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235746"
---
# <a name="ca1050-declare-types-in-namespaces"></a>CA1050: Ad alanlarında türler bildirin

|||
|-|-|
|TypeName|DeclareTypesInNamespaces|
|CheckId|CA1050|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir tür, adlandırılmış bir ad alanının kapsamı dışında tanımlanır.

## <a name="rule-description"></a>Kural açıklaması
Türler ad çakışmalarını engellemek için ad alanlarında ve bir nesne hiyerarşisinde ilgili türleri düzenlemenin bir yolu olarak belirtilir. Adlandırılmış ad alanı dışında olan türler, kodda başvurulmayacak genel bir ad alanında bulunur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, türü bir ad alanına yerleştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı bastırmanız gerekmese de, derleme diğer derlemelerle birlikte hiçbir zaman kullanılmaz.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bir ad alanı dışında yanlış bir şekilde bildirilmeli bir kitaplık ve bir ad alanında bildirildiği aynı ada sahip bir tür gösterir.

[!code-csharp[FxCop.Design.TypesLiveInNamespaces#1](../code-quality/codesnippet/CSharp/ca1050-declare-types-in-namespaces_1.cs)]
[!code-vb[FxCop.Design.TypesLiveInNamespaces#1](../code-quality/codesnippet/VisualBasic/ca1050-declare-types-in-namespaces_1.vb)]

## <a name="example"></a>Örnek
Aşağıdaki uygulama daha önce tanımlanan kitaplığı kullanır. Ad alanı tarafından nitelendirilmediği zaman `Test` , bir ad alanı dışında belirtilen türün oluşturulduğunu unutmayın. Ayrıca, içindeki `Test` `Goodspace`türüne erişmek için, ad alanı adının gerekli olduğunu unutmayın.

[!code-csharp[FxCop.Design.TestTypesLive#1](../code-quality/codesnippet/CSharp/ca1050-declare-types-in-namespaces_2.cs)]
[!code-vb[FxCop.Design.TestTypesLive#1](../code-quality/codesnippet/VisualBasic/ca1050-declare-types-in-namespaces_2.vb)]