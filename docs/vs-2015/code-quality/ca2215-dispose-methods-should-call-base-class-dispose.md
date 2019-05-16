---
title: 'CA2215: Atma yöntemleri taban sınıf atmayı çağırmalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2215
- DisposeMethodsShouldCallBaseClassDispose
- Dispose methods should call base class dispose
helpviewer_keywords:
- DisposeMethodsShouldCallBaseClassDispose
- CA2215
ms.assetid: c772e7a6-a87e-425c-a70e-912664ae9042
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bc934afd9289a6bce425084f3588a7e912baf9b9
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65681187"
---
# <a name="ca2215-dispose-methods-should-call-base-class-dispose"></a>CA2215: Atma metotları taban sınıf atmayı çağırmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DisposeMethodsShouldCallBaseClassDispose|
|CheckId|CA2215|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Uygulayan bir tür <xref:System.IDisposable?displayProperty=fullName> ayrıca uygulayan bir tür tarafından devralındığında <xref:System.IDisposable>. <xref:System.IDisposable.Dispose%2A> Türetilen türün yöntemi çağırmaz <xref:System.IDisposable.Dispose%2A> üst türü yöntemi.

## <a name="rule-description"></a>Kural Tanımı
 Bir tür atılabilen bir türden devralınırsa, çağırmalıdır <xref:System.IDisposable.Dispose%2A> yöntemi kendi içinde temel türün <xref:System.IDisposable.Dispose%2A> yöntemi. Temel tür yöntem çağırma Dispose taban türü tarafından oluşturulan tüm kaynakların serbest bırakıldığından sağlar.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için çağrı `base`.<xref:System.IDisposable.Dispose%2A> içinde <xref:System.IDisposable.Dispose%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Varsa bu kuraldan bir uyarıyı bastırmak güvenlidir çağrısı `base`.<xref:System.IDisposable.Dispose%2A> daha ayrıntılı bir çağırma kuralı denetimleri'den oluşur.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `TypeA` uygulayan <xref:System.IDisposable>.

 [!code-csharp[FxCop.Usage.IDisposablePattern#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.IDisposablePattern/cs/FxCop.Usage.IDisposablePattern.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `TypeB` türünden devralan `TypeA` ve doğru bir şekilde çağıran kendi <xref:System.IDisposable.Dispose%2A> yöntemi.

 [!code-vb[FxCop.Usage.IDisposableBaseCalled#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.IDisposableBaseCalled/vb/FxCop.Usage.IDisposableBaseCalled.vb#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.IDisposable?displayProperty=fullName> [Dispose deseni](https://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
