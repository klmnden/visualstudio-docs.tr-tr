---
title: 'CA1021: out parametrelerinden kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1021
- AvoidOutParameters
helpviewer_keywords:
- AvoidOutParameters
- CA1021
ms.assetid: 970f2304-842c-4fb7-9734-f3871da8d479
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cf9475ad208a229057700fa2965984fbdcb17abf
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923097"
---
# <a name="ca1021-avoid-out-parameters"></a>CA1021: out parametrelerinden kaçının

|||
|-|-|
|TypeName|AvoidOutParameters|
|CheckId|CA1021|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak türde ortak veya korumalı yöntemin bir `out` parametresi vardır.

## <a name="rule-description"></a>Kural açıklaması
Türlerin başvuruya göre geçirilmesi (veya `out` `ref`kullanılarak) işaretçilerle deneyim gerektirir, değer türlerinin ve başvuru türlerinin nasıl farklı olduğunu ve birden çok dönüş değeri ile yöntemleri işleme. Ayrıca, ve `ref` parametreleri arasındaki `out` fark yaygın olarak anlaşılmaz.

Başvuru türü "başvuruya göre" geçirildiğinde, yöntemi nesnenin farklı bir örneğini döndürmek için parametresini kullanmayı amaçladığı. Başvuru türü başvuruya göre geçirilmesi, çift işaretçi, işaretçi işaretçisi veya çift yöneltme kullanma olarak da bilinir. "Değere göre" olarak geçen varsayılan çağırma kuralını kullanarak, başvuru türü alan bir parametre zaten nesneye bir işaretçi alır. İşaret ettiği nesne değil, işaretçi değere göre geçirilir. Değere göre geçirme yöntemi, yöntemin, başvuru türünün yeni bir örneğine işaret eden işaretçiyi değiştiremeyeceği anlamına gelir. Ancak, gösterdiği nesnenin içeriğini değiştirebilir. Çoğu uygulama için bu yeterlidir ve istenen davranışı verir.

Bir yöntemin farklı bir örnek döndürmesi gerekiyorsa, bunu gerçekleştirmek için yönteminin dönüş değerini kullanın. Dizeler üzerinde çalışan ve bir dizenin yeni bir örneğini döndüren çeşitli yöntemler için sınıfınabakın.<xref:System.String?displayProperty=fullName> Bu model kullanıldığında, çağıran özgün nesnenin korunup korunmayacağına karar vermelidir.

Dönüş değerleri çok fazla ve yoğun olarak kullanıldığından, `out` ve `ref` parametrelerinin doğru uygulaması ara tasarım ve kodlama becerileri gerektirir. Genel bir hedef kitle için tasarlayan kitaplık mimarları, kullanıcıların, veya `out` `ref` parametreleriyle birlikte çalışmasını beklememelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın bir değer türünden kaynaklanan ihlalini onarmak için, yönteminin dönüş değeri olarak nesneyi döndürmesini sağlayabilirsiniz. Yöntemin birden çok değer döndürmesi gerekiyorsa, değerleri tutan bir nesnenin tek bir örneğini döndürecek şekilde yeniden tasarlayamalıdır.

Bir başvuru türü nedeniyle oluşan bu kuralın ihlalini onarmak için, istenen davranışın başvurunun yeni bir örneğini döndürmesinin olduğundan emin olun. Eğer ise, yöntemi bunu yapmak için dönüş değerini kullanmalıdır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı gizlemek güvenlidir. Ancak, bu tasarım kullanılabilirlik sorunlarına neden olabilir.

## <a name="example"></a>Örnek
Aşağıdaki kitaplıkta, bir kullanıcının geri bildirimlerine yanıtlar üreten bir sınıfın iki uygulaması gösterilmektedir. İlk uygulama (`BadRefAndOut`), kitaplık kullanıcısını üç dönüş değerini yönetmeye zorlar. İkinci uygulama (`RedesignedRefAndOut`), verileri tek bir birim olarak yöneten bir kapsayıcı sınıfının (`ReplyData`) örneğini döndürerek Kullanıcı deneyimini basitleştirir.

[!code-csharp[FxCop.Design.NoRefOrOut#1](../code-quality/codesnippet/CSharp/ca1021-avoid-out-parameters_1.cs)]

## <a name="example"></a>Örnek
Aşağıdaki uygulama, kullanıcının deneyimini gösterir. Yeniden tasarlanan kitaplığa (`UseTheSimplifiedClass` Yöntem) yapılan çağrı daha basittir ve yöntemi tarafından döndürülen bilgiler kolayca yönetilir. İki yöntemden oluşan çıkış aynı.

[!code-csharp[FxCop.Design.TestNoRefOrOut#1](../code-quality/codesnippet/CSharp/ca1021-avoid-out-parameters_2.cs)]

## <a name="example"></a>Örnek
Aşağıdaki örnek kitaplık, başvuru türleri `ref` parametrelerinin nasıl kullanıldığını gösterir ve bu işlevselliği uygulamak için daha iyi bir yol gösterir.

[!code-csharp[FxCop.Design.RefByRefNo#1](../code-quality/codesnippet/CSharp/ca1021-avoid-out-parameters_3.cs)]

## <a name="example"></a>Örnek
Aşağıdaki uygulama, davranışı göstermek için kitaplıktaki her yöntemi çağırır.

[!code-csharp[FxCop.Design.TestRefByRefNo#1](../code-quality/codesnippet/CSharp/ca1021-avoid-out-parameters_4.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
Changing pointer - passed by value:
12345
12345
Changing pointer - passed by reference:
12345
12345 ABCDE
Passing by return value:
12345 ABCDE
```

## <a name="try-pattern-methods"></a>Model yöntemlerini deneyin

### <a name="description"></a>Açıklama
Bu ihlalin **bir şeyi\<deneyin >** <xref:System.Int32.TryParse%2A?displayProperty=fullName>modelini uygulayan yöntemler. Aşağıdaki örnek, <xref:System.Int32.TryParse%2A?displayProperty=fullName> yöntemini uygulayan bir yapıyı (değer türü) gösterir.

### <a name="code"></a>Kod
[!code-csharp[FxCop.Design.TryPattern#1](../code-quality/codesnippet/CSharp/ca1021-avoid-out-parameters_5.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA1045 Türleri başvuruya göre geçirmeyin](../code-quality/ca1045-do-not-pass-types-by-reference.md)