---
title: 'CA2111: İşaretçiler görünür olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PointersShouldNotBeVisible
- CA2111
helpviewer_keywords:
- CA2111
- PointersShouldNotBeVisible
ms.assetid: b3a8d466-895b-43bc-a2df-5d7058fe915f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8a93f776ac6e133b0ebf79d1dfa56f802ff66e5f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232777"
---
# <a name="ca2111-pointers-should-not-be-visible"></a>CA2111: İşaretçiler görünür olmamalıdır

|||
|-|-|
|TypeName|PointersShouldNotBeVisible|
|CheckId|CA2111|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı <xref:System.IntPtr?displayProperty=fullName> veya <xref:System.UIntPtr?displayProperty=fullName> alan salt okunurdur.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.IntPtr>ve <xref:System.UIntPtr> yönetilmeyen belleğe erişmek için kullanılan işaretçi türleridir. Bir işaretçi özel, iç veya salt okunurdur değilse, kötü amaçlı kod işaretçinin değerini değiştirebilir, bu da, bellekteki rastgele konumlara erişime izin verebilir veya uygulama ya da sistem arızalarına neden olabilir.

İşaretçi alanını içeren türe erişimi güvenli hale getirmek istiyorsanız, bkz [. CA2112: Güvenli türler alanları](../code-quality/ca2112-secured-types-should-not-expose-fields.md)kullanıma sunmamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
İşaretçiyi salt okunurdur, iç veya özel yaparak güvenli hale getirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
İşaretçinin değerine bağlı değilseniz bu kuraldan bir uyarı gizleyin.

## <a name="example"></a>Örnek
Aşağıdaki kod, kuralı ihlal eden ve karşılayan işaretçileri gösterir. Özel olmayan işaretçilerin CA1051 kuralını [da ihlal ettiğini unutmayın: Görünür örnek alanlarını](../code-quality/ca1051-do-not-declare-visible-instance-fields.md)bildirmeyin.

[!code-csharp[FxCop.Security.PointersArePrivate#1](../code-quality/codesnippet/CSharp/ca2111-pointers-should-not-be-visible_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2112 Güvenli türler alanları kullanıma sunmamalıdır](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

[CA1051 Görünür örnek alanlarını bildirme](../code-quality/ca1051-do-not-declare-visible-instance-fields.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IntPtr?displayProperty=fullName>
- <xref:System.UIntPtr?displayProperty=fullName>