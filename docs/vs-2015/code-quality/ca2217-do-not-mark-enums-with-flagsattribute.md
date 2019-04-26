---
title: 'CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotMarkEnumsWithFlags
- CA2217
helpviewer_keywords:
- DoNotMarkEnumsWithFlags
- CA2217
ms.assetid: 1b6f626c-66bf-45b0-a3e2-7c41ee9ceda7
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 70078d89f2de8038e4a1143679d0614a5479a2b8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62540660"
---
# <a name="ca2217-do-not-mark-enums-with-flagsattribute"></a>CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotMarkEnumsWithFlags|
|CheckId|CA2217|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir sabit listesi ile işaretlenmiş <xref:System.FlagsAttribute> ve varsa veya sabit listesi üzerinde iki ya da diğer bir birleşimini tabanların olmayan daha fazla değer tanımlı değerler.

## <a name="rule-description"></a>Kural Tanımı
 Bir numaralandırma olmalıdır <xref:System.FlagsAttribute> yalnızca her değer numaralandırmada tanımlanan ikinin üssü veya bir birleşimini tanımlı değerler sunar.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için kaldırmak <xref:System.FlagsAttribute> gelen sabit listesi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir numaralandırma ne iki gücünü ya da herhangi bir tanımlı değerlerin bir birleşimi olan 3 değeri içeren renk, gösterir. Color sabit listesi ile işaretli olmamalıdır <xref:System.FlagsAttribute>.

 [!code-cpp[FxCop.Usage.EnumNoFlags#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Usage.EnumNoFlags/cpp/FxCop.Usage.EnumNoFlags.cpp#1)]
 [!code-csharp[FxCop.Usage.EnumNoFlags#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.EnumNoFlags/cs/FxCop.Usage.EnumNoFlags.cs#1)]
 [!code-vb[FxCop.Usage.EnumNoFlags#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.EnumNoFlags/vb/FxCop.Usage.EnumNoFlags.vb#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek System.FlagsAttribute ile işaretlenen gereksinimleri karşılayan bir numaralandırma gün gösterir.

 [!code-cpp[FxCop.Usage.EnumNoFlags2#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Usage.EnumNoFlags2/cpp/FxCop.Usage.EnumNoFlags2.cpp#1)]
 [!code-csharp[FxCop.Usage.EnumNoFlags2#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.EnumNoFlags2/cs/FxCop.Usage.EnumNoFlags2.cs#1)]
 [!code-vb[FxCop.Usage.EnumNoFlags2#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.EnumNoFlags2/vb/FxCop.Usage.EnumNoFlags2.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.FlagsAttribute?displayProperty=fullName>
