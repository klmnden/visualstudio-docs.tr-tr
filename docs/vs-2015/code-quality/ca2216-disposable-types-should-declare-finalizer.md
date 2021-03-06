---
title: 'CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DisposableTypesShouldDeclareFinalizer
- CA2216
helpviewer_keywords:
- CA2216
- DisposableTypesShouldDeclareFinalizer
ms.assetid: 0cabcc5e-b526-452b-8c2a-0cbe3b93c0ef
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 8a033dbb152542e528b32e26f35a7d63dba30891
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65681165"
---
# <a name="ca2216-disposable-types-should-declare-finalizer"></a>CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DisposableTypesShouldDeclareFinalizer|
|CheckId|CA2216|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Uygulayan bir tür <xref:System.IDisposable?displayProperty=fullName>ve yönetilmeyen kaynakların kullanımını öneren alanlar, bir sonlandırıcı açıklandığı uygulamıyor <xref:System.Object.Finalize%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 Atılabilir türü aşağıdaki türlerde alanlar içeriyorsa bu kural ihlalini bildirilir:

- <xref:System.IntPtr?displayProperty=fullName>

- <xref:System.UIntPtr?displayProperty=fullName>

- <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için çağıran bir sonlandırıcı uygulamak, <xref:System.IDisposable.Dispose%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Türü uygulamazsa bu kuraldan bir uyarıyı bastırmak güvenlidir <xref:System.IDisposable> yönetilmeyen kaynakları serbest bırakmak amacıyla.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

 [!code-csharp[FxCop.Usage.DisposeNoFinalize#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.DisposeNoFinalize/cs/FxCop.Usage.DisposeNoFinalize.cs#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2115: GC çağırın. Yerel kaynaklar kullanırken KeepAlive](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)

 [CA1816: GC çağırın. IDisposable.Dispose doğru](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)

 [CA1049: Yerel kaynaklara sahip türler atılabilir olmalıdır](../code-quality/ca1049-types-that-own-native-resources-should-be-disposable.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.IDisposable?displayProperty=fullName><xref:System.IntPtr?displayProperty=fullName>
 <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName>
 <xref:System.UIntPtr?displayProperty=fullName>
 <xref:System.Object.Finalize%2A?displayProperty=fullName>
 [Dispose Deseni](https://msdn.microsoft.com/library/31a6c13b-d6a2-492b-9a9f-e5238c983bcb)
