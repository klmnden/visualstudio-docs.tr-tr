---
title: 'CA1816: GC çağırın. IDisposable.Dispose doğru | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1816
- DisposeMethodsShouldCallSuppressFinalize
helpviewer_keywords:
- DisposeMethodsShouldCallSuppressFinalize
- CA1816
ms.assetid: 47915fbb-103f-4333-b157-1da16bf49660
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 031003e4989e6018a250045f5fa8550a7ec2033a
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65683028"
---
# <a name="ca1816-call-gcsuppressfinalize-correctly"></a>CA1816: GC.SuppressFinalize'ı doğru çağırın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|CallGCSuppressFinalizeCorrectly|
|CheckId|CA1816|
|Kategori|Microsoft. Kullanım|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

- Uygulaması olan bir yöntemin <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> arama <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>.

- Uygulaması olmayan bir yöntem <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> çağrıları <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>.

- Bir yöntemi çağıran <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> ve bu (Visual Basic'te Me) dışında bir şey geçirir.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> Yöntemi nesnenin çöp toplama için kullanılabilir hale gelmeden önce herhangi bir zamanda kaynakları serbest kullanıcılar olanak sağlar. Varsa <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> yöntemi çağrıldığında, bu nesnenin kaynakları serbest bırakır. Bu, sonlandırma gereksiz kılar. <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> çağırmalıdır <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> böylece nesnenin Sonlandırıcısı çöp toplayıcı çağırmaz.

 Önlemek için sonlandırıcılar ile yeniden uygulamak, [System.IDisposable] (sahip türetilmiş türler<!-- TODO: review code entity reference <xref:assetId:///System.IDisposable?qualifyHint=True&amp;autoUpgrade=False>  -->) ve çağırmak için korumasız türleri sonlandırıcılar olmadan hala çağırmalıdır <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için:

 Yöntem uygulaması ise <xref:System.IDisposable.Dispose%2A>, bir çağrı ekleyin <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>.

 Yöntem uygulaması değilse <xref:System.IDisposable.Dispose%2A>, çağrısını kaldırın ya da <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> veya türün taşıma <xref:System.IDisposable.Dispose%2A> uygulaması.

 Tüm çağrıları değiştirme <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> bu (Visual Basic'te Me) geçirilecek.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Kullanarak deliberating, yalnızca bu kuraldan bir uyarıyı bastırmak <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName> diğer nesnelerin ömrünü denetlemek için. Uygulaması, bu kuraldan bir uyarıyı bastırmayın <xref:System.IDisposable.Dispose%2A> arama <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>. Bu durumda, sonlandırma bastırmak başarısız olan performansı düşürür ve hiçbir avantaj sağlar.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bir yöntemi, yanlış çağrıları gösterir <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>.

 [!code-csharp[FxCop.Usage.CallGCSuppressFinalizeCorrectly#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.CallGCSuppressFinalizeCorrectly/CS/FxCop.Usage.CallGCSuppressFinalizeCorrectly.cs#1)]
 [!code-vb[FxCop.Usage.CallGCSuppressFinalizeCorrectly#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.CallGCSuppressFinalizeCorrectly/VB/FxCop.Usage.CallGCSuppressFinalizeCorrectly.vb#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek bir yöntem çağrıları, doğru bir şekilde gösterir <xref:System.GC.SuppressFinalize%2A?displayProperty=fullName>.

 [!code-csharp[FxCop.Usage.CallGCSuppressFinalizeCorrectly2#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.CallGCSuppressFinalizeCorrectly2/CS/FxCop.Usage.CallGCSuppressFinalizeCorrectly2.cs#1)]
 [!code-vb[FxCop.Usage.CallGCSuppressFinalizeCorrectly2#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.CallGCSuppressFinalizeCorrectly2/VB/FxCop.Usage.CallGCSuppressFinalizeCorrectly2.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2215: Atma yöntemleri taban sınıf atmayı çağırmalıdır](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)

 [CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Dispose Deseni](https://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
