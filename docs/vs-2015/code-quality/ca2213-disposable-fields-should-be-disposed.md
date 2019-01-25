---
title: 'CA2213: Atılabilen alanlar elden | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DisposableFieldsShouldBeDisposed
- CA2213
helpviewer_keywords:
- CA2213
- DisposableFieldsShouldBeDisposed
ms.assetid: e99442c9-70e2-47f3-b61a-d8ac003bc6e5
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: d89e714ceb0a6d0e3d99be05f6c6936622c035ab
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786794"
---
# <a name="ca2213-disposable-fields-should-be-disposed"></a>CA2213: Atılabilen alanlar atılmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DisposableFieldsShouldBeDisposed|
|CheckId|CA2213|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Uygulayan bir tür <xref:System.IDisposable?displayProperty=fullName> ayrıca uygulayan türler alanlar bildirir <xref:System.IDisposable>. <xref:System.IDisposable.Dispose%2A> Alanının yöntemi çağrılmaz <xref:System.IDisposable.Dispose%2A> bildirim türü yöntemi.

## <a name="rule-description"></a>Kural Tanımı
 Bir tür için kendi yönetilmeyen tüm kaynaklarını atma sorumludur; Bu uygulama tarafından gerçekleştirilir <xref:System.IDisposable>. Tek kullanımlık bir tür olup olmadığını görmek için bu kural denetler `T` bir alan bildirir `F` atılabilir bir türün diğer bir deyişle bir örneğini `FT`. Her bir alan için `F`, kural için bir çağrı bulmaya çalışır `FT.Dispose`. Kural çağrılan yöntemler arar `T.Dispose`ve daha düşük bir düzey (çağrılan yöntemler tarafından çağrılan yöntemler `FT.Dispose`).

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için çağrı <xref:System.IDisposable.Dispose%2A> uygulayan türler alanlar üzerinde <xref:System.IDisposable> sorumlu ve tutulan alanı tarafından yönetilmeyen kaynakları serbest bırakmak.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Kaynağı serbest bırakarak alanı tarafından tutulan için sorumlu olduğunuz değil veya bu kuraldan bir uyarıyı bastırmak güvenlidir çağrısı <xref:System.IDisposable.Dispose%2A> kural denetimleri daha derin arama düzeyinde gerçekleşir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `TypeA` uygulayan <xref:System.IDisposable> (`FT` önceki tartışmada).

 [!code-csharp[FxCop.Usage.IDisposablePattern#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.IDisposablePattern/cs/FxCop.Usage.IDisposablePattern.cs#1)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `TypeB` , ihlal bu kural bir alan bildirerek `aFieldOfADisposableType` (`F` önceki tartışmada) tek kullanımlık bir tür olarak (`TypeA`) ve değil çağırma <xref:System.IDisposable.Dispose%2A> alanı. `TypeB` karşılık gelen `T` önceki tartışmada.

 [!code-csharp[FxCop.Usage.IDisposableFields#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.IDisposableFields/cs/FxCop.Usage.IDisposableFields.cs#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.IDisposable?displayProperty=fullName> [Dispose deseni](http://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
