---
title: 'CA1403: Otomatik yerleşim türleri COM görünebilir olmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- AutoLayoutTypesShouldNotBeComVisible
- CA1403
helpviewer_keywords:
- CA1403
- AutoLayoutTypesShouldNotBeComVisible
ms.assetid: a7007714-f9b4-4730-94e0-67d3dc68991f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: d9c39e61af994e31a59e75872749464aee0b7093
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54977180"
---
# <a name="ca1403-auto-layout-types-should-not-be-com-visible"></a>CA1403: Otomatik yerleşim türleri COM görünebilir olmamalıdır

|||
|-|-|
|TypeName|AutoLayoutTypesShouldNotBeComVisible|
|CheckId|CA1403|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir Bileşen Nesne Modeli (COM) görünebilir değer türü ile işaretlenmiş <xref:System.Runtime.InteropServices.StructLayoutAttribute?displayProperty=fullName> özniteliğini <xref:System.Runtime.InteropServices.LayoutKind.Auto?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Runtime.InteropServices.LayoutKind> Yerleşim türleri, ortak dil çalışma zamanı tarafından yönetilir. Belirli bir düzeni beklediğiniz COM istemcileri keser .NET Framework sürümleri arasında bu tür yerleşimi değiştirebilirsiniz. Varsa <xref:System.Runtime.InteropServices.StructLayoutAttribute> özniteliği belirtilmezse, C#, Visual Basic ve C++ Derleyicileri belirtin [LayoutKind.Auto](<xref:System.Runtime.InteropServices.LayoutKind.Auto>) değer türleri için.

Tersi durumda işaretlenmiş sürece tüm genel ve genel olmayan türler COM görünür ve tüm genel olmayan ve genel türler COM'a görünmez Ancak, hatalı pozitif sonuçları azaltmak için bu kural türünü açıkça belirtilen COM görünürlüğünü gerektirir. Derlemeyi içeren ile işaretlenmelidir <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> kümesine `false` ve türü ile işaretlenmelidir <xref:System.Runtime.InteropServices.ComVisibleAttribute> kümesine `true`.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için değerini değiştirmek <xref:System.Runtime.InteropServices.StructLayoutAttribute> özniteliğini [LayoutKind.Explicit](<xref:System.Runtime.InteropServices.LayoutKind.Explicit>) veya [LayoutKind.Sequential](<xref:System.Runtime.InteropServices.LayoutKind.Sequential>), veya tür COM tarafından görünmez yapma

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralını ihlal eden bir tür ile kural karşılayan bir tür gösterir.

[!code-csharp[FxCop.Interoperability.AutoLayout#1](../code-quality/codesnippet/CSharp/ca1403-auto-layout-types-should-not-be-com-visible_1.cs)]
[!code-vb[FxCop.Interoperability.AutoLayout#1](../code-quality/codesnippet/VisualBasic/ca1403-auto-layout-types-should-not-be-com-visible_1.vb)]

## <a name="related-rules"></a>İlgili kuralları

[CA1408: AutoDual ClassInterfaceType kullanma](../code-quality/ca1408-do-not-use-autodual-classinterfacetype.md)

## <a name="see-also"></a>Ayrıca bkz.

- [İçin .NET türlerini nitelendirme Sınıflandır](/dotnet/framework/interop/qualifying-net-types-for-interoperation)
- [Yönetilmeyen kod ile birlikte çalışma](/dotnet/framework/interop/index)