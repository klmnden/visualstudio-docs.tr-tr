---
title: 'CA1014: Derlemeleri CLSCompliantAttribute ile işaretle'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1014
- MarkAssembliesWithClsCompliant
helpviewer_keywords:
- CA1014
- MarkAssembliesWithClsCompliant
ms.assetid: 4fe57449-cf45-4745-bcd2-6345f1ed266d
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 387eb464959fba522e31f9586998335cb306d844
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236319"
---
# <a name="ca1014-mark-assemblies-with-clscompliantattribute"></a>CA1014: Derlemeleri CLSCompliantAttribute ile işaretle

|||
|-|-|
|TypeName|MarkAssembliesWithClsCompliant|
|CheckId|CA1014|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir bütünleştirilmiş koda <xref:System.CLSCompliantAttribute?displayProperty=fullName> uygulanmış özniteliği yok.

## <a name="rule-description"></a>Kural açıklaması
Ortak Dil Tanımlaması (CLS) ad kısıtlamalarını, veri türlerini ve karşıt programlama dillerini kullanırsa derlemelerin uyması zorunlu olan kuralları tanımlar. İyi tasarım, tüm derlemelerin ile birlikte <xref:System.CLSCompliantAttribute>CLS uyumluluğunu açıkça belirtmeyeceğini belirler. Öznitelik bir derlemede yoksa, derleme uyumlu değildir.

CLS uyumlu bir derlemenin uyumlu olmayan türler veya tür üyeleri içermesi mümkündür.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, derlemeye özniteliğini ekleyin. Tüm derlemeyi uyumsuz olarak işaretlemek yerine, hangi tür veya tür üyelerinin uyumlu olduğunu belirlemelisiniz ve bu öğeleri bu öğe olarak işaretleyebilirsiniz. Mümkünse, uyumsuz Üyeler için CLS uyumlu bir alternatif sağlamanız gerekir; böylece, en olası hedef kitle, derlemenizin tüm işlevlerine erişebilir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın. Derlemenin uyumlu olmasını istemiyorsanız, özniteliğini uygulayın ve değerini olarak `false`ayarlayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, tarafından CLS uyumlu olduğunu bildiren <xref:System.CLSCompliantAttribute?displayProperty=fullName> özniteliği uygulayan bir derlemeyi gösterir.

[!code-csharp[FxCop.Design.AssembliesCls#1](../code-quality/codesnippet/CSharp/ca1014-mark-assemblies-with-clscompliantattribute_1.cs)]
[!code-cpp[FxCop.Design.AssembliesCls#1](../code-quality/codesnippet/CPP/ca1014-mark-assemblies-with-clscompliantattribute_1.cpp)]
[!code-vb[FxCop.Design.AssembliesCls#1](../code-quality/codesnippet/VisualBasic/ca1014-mark-assemblies-with-clscompliantattribute_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.CLSCompliantAttribute?displayProperty=fullName>
- [Dil Bağımsızlığı ve Dilden Bağımsız Bileşenler](/dotnet/standard/language-independence-and-language-independent-components)