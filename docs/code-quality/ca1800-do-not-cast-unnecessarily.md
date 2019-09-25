---
title: 'CA1800: Gereksiz tür dönüştürmeler yapmayın'
ms.date: 10/26/2017
ms.topic: reference
f1_keywords:
- CA1800
- DoNotCastUnnecessarily
helpviewer_keywords:
- DoNotCastUnnecessarily
- CA1800
ms.assetid: b79a010a-6627-421e-8955-6007e32fa808
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: 85d168e97f422a3965096a334cb2a448406604f9
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233835"
---
# <a name="ca1800-do-not-cast-unnecessarily"></a>CA1800: Gereksiz tür dönüştürmeler yapmayın

|||
|-|-|
|TypeName|DoNotCastUnnecessarily|
|CheckId|CA1800|
|Kategori|Microsoft. Performance|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir yöntem bağımsız değişkenlerinin veya yerel değişkenlerinin birinde yinelenen yayınları gerçekleştirir.

Bu kurala göre tüm analizler için, sınanan derlemenin hata ayıklama bilgileri kullanılarak oluşturulması gerekir ve ilişkili program veritabanı (. pdb) dosyası kullanılabilir olmalıdır.

## <a name="rule-description"></a>Kural açıklaması
Özellikle yayınlar sıkıştırılmış yineleme deyiminde gerçekleştirildiğinde yinelenen yayınların performansını azaltır. Açık yinelenen atama işlemleri için, dönüştürme sonucunu yerel bir değişkende depolayın ve yinelenen atama işlemleri yerine yerel değişkeni kullanın.

İşleç, gerçek atama gerçekleştirilmeden önce dönüştürmenin başarılı olup olmadığını test etmek için kullanılıyorsa, bunun yerine `as` işlecin sonucunu test etmeyi düşünün. C# `is` Bu, `is` işleci tarafından gerçekleştirilen örtük atama işlemi olmadan aynı işlevselliği sağlar. Ya da, C# 7,0 ve sonraki sürümlerde, tür `is` dönüştürmeyi denetlemek ve ifadeyi tek bir adımda bu türden bir değişkene dönüştürmek için [model eşleme](/dotnet/csharp/language-reference/keywords/is#pattern-matching-with-is) ile işlecini kullanın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, Yöntem uygulamasını değiştirerek atama işlemlerinin sayısını en aza indirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Performans sorunu değilse, bu kuraldan bir uyarının veya kuralı tamamen yok saymak güvenlidir.

## <a name="examples"></a>Örnekler
Aşağıdaki örnek, C# `is` işlecini kullanarak kuralı ihlal eden bir yöntemi gösterir. İkinci bir yöntem `is` işleci bir test ile değiştirerek, işleci bir test `as` ile değiştirerek, iki ' dan birine yineleme başına dönüştürme işlemi sayısını azaltan kuralını karşılar. Ayrıca, tür dönüştürme başarılı olursa, istenen türde `is` bir değişken oluşturmak için, bir üçüncü Yöntem aynı zamanda, [stili eşleştirme](/dotnet/csharp/language-reference/keywords/is#pattern-matching-with-is) ile kullanarak kuralı karşılar.

[!code-csharp[FxCop.Performance.UnnecessaryCastsAsIs#1](../code-quality/codesnippet/CSharp/ca1800-do-not-cast-unnecessarily_1.cs)]

Aşağıdaki örnek, bir yöntemi `start_Click`gösterir, bu, kuralı ihlal eden birden çok yinelenen açık oluşturmaya sahiptir ve bir `reset_Click`yöntemi, bir yerel değişkende dönüştürmeyi depolayarak kuralını karşılayan bir yöntemi gösterir.

[!code-vb[FxCop.Performance.UnnecessaryCasts#1](../code-quality/codesnippet/VisualBasic/ca1800-do-not-cast-unnecessarily_2.vb)]
[!code-csharp[FxCop.Performance.UnnecessaryCasts#1](../code-quality/codesnippet/CSharp/ca1800-do-not-cast-unnecessarily_2.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- [as (C# başvuru)](/dotnet/csharp/language-reference/keywords/as)
- [, (C# başvuru)](/dotnet/csharp/language-reference/keywords/is)