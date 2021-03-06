---
title: 'CA1403: Otomatik Yerleşim türleri COM görünebilir olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- AutoLayoutTypesShouldNotBeComVisible
- CA1403
helpviewer_keywords:
- CA1403
- AutoLayoutTypesShouldNotBeComVisible
ms.assetid: a7007714-f9b4-4730-94e0-67d3dc68991f
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2420582ab342948d7774e1bb9e4b5947f44f8d2b
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65695434"
---
# <a name="ca1403-auto-layout-types-should-not-be-com-visible"></a>CA1403: Otomatik yerleşim türleri COM görünebilir olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|AutoLayoutTypesShouldNotBeComVisible|
|CheckId|CA1403|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir Bileşen Nesne Modeli (COM) görünebilir değer türü ile işaretlenmiş <xref:System.Runtime.InteropServices.StructLayoutAttribute?displayProperty=fullName> özniteliğini <xref:System.Runtime.InteropServices.LayoutKind?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Runtime.InteropServices.LayoutKind> Yerleşim türleri, ortak dil çalışma zamanı tarafından yönetilir. Belirli bir düzeni beklediğiniz COM istemcilerini kesintiye uğratır .NET Framework sürümleri arasında bu tür yerleşimi değiştirebilirsiniz. Unutmayın <xref:System.Runtime.InteropServices.StructLayoutAttribute> özniteliği belirtilmezse, C#, [!INCLUDE[vbprvb](../includes/vbprvb-md.md)], ve C++ Derleyicileri belirtin <xref:System.Runtime.InteropServices.LayoutKind> değer türleri için Düzen.

 Tersi durumda işaretlenmiş sürece tüm genel türlere COM görünür; Tüm özel ve genel türler COM'a görünmez Ancak, hatalı pozitif sonuçları azaltmak için bu kural türünü açıkça belirtilen COM görünürlüğünü gerektirir; derlemeyi içeren ile işaretlenmelidir <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> kümesine `false` ve türü ile işaretlenmelidir <xref:System.Runtime.InteropServices.ComVisibleAttribute> kümesine `true`.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için değerini değiştirmek <xref:System.Runtime.InteropServices.StructLayoutAttribute> özniteliğini <xref:System.Runtime.InteropServices.LayoutKind> veya <xref:System.Runtime.InteropServices.LayoutKind>, veya tür COM tarafından görünmez yapma

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kuralını ihlal eden bir tür ile kural karşılayan bir tür gösterir.

 [!code-csharp[FxCop.Interoperability.AutoLayout#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.AutoLayout/cs/FxCop.Interoperability.AutoLayout.cs#1)]
 [!code-vb[FxCop.Interoperability.AutoLayout#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.AutoLayout/vb/FxCop.Interoperability.AutoLayout.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1408: AutoDual ClassInterfaceType kullanma](../code-quality/ca1408-do-not-use-autodual-classinterfacetype.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Sınıf arabirimine giriş](https://msdn.microsoft.com/733c0dd2-12e5-46e6-8de1-39d5b25df024) [birlikte çalışma için .NET türlerini niteleme](https://msdn.microsoft.com/library/4b8afb52-fb8d-4e65-b47c-fd82956a3cdd) [yönetilmeyen kod ile birlikte](https://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)
