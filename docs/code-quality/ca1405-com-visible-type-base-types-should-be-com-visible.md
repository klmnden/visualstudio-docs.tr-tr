---
title: 'CA1405: COM görünebilir tür taban türler COM görünebilir olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1405
- ComVisibleTypeBaseTypesShouldBeComVisible
helpviewer_keywords:
- CA1405
- ComVisibleTypeBaseTypesShouldBeComVisible
ms.assetid: a762ea2f-5285-4f73-bfb9-9eb10aea4290
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 8e4e5c4ed258bcc88fedbb6d015fed576d326a0f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234962"
---
# <a name="ca1405-com-visible-type-base-types-should-be-com-visible"></a>CA1405: COM görünebilir tür taban türler COM görünebilir olmalıdır

|||
|-|-|
|TypeName|ComVisibleTypeBaseTypesShouldBeComVisible|
|CheckId|CA1405|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Bağımlıdsondüzelme|

## <a name="cause"></a>Sebep
Bileşen nesne modeli (COM) görünür türü, COM görünebilir olmayan bir türden türetilir.

## <a name="rule-description"></a>Kural açıklaması
COM görünebilir bir tür üyeleri yeni bir sürüme eklediğinde, geçerli sürüme bağlanan COM istemcilerinin kesilmesini önlemek için katı kılavuzlara uymalıdır. COM tarafından görünmeyen bir tür, yeni üyeler eklendiğinde bu COM sürümü oluşturma kurallarını izlemek zorunda değildir. Ancak, com görünebilir bir tür, com görünmeyen türden türetiliyor ve <xref:System.Runtime.InteropServices.ClassInterfaceType?displayProperty=fullName> ya <xref:System.Runtime.InteropServices.ClassInterfaceType> da (varsayılan) bir sınıf arabirimini, temel türün tüm genel üyelerini (özellikle de com görünmez olarak işaretlenmedikleri sürece) COM 'a sunulur. Temel tür sonraki bir sürüme yeni üyeler eklerse, türetilmiş türün sınıf arabirimine bağlanan tüm COM istemcileri kesilebilir. Com tarafından görülebilen türler, com istemcilerinin bölünmesi olasılığını azaltmak için yalnızca COM görünebilir türlerden türetilmelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, temel türlerin COM görünebilir veya türetilmiş türü COM görünmez hale gelir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir.

[!code-vb[FxCop.Interoperability.ComBaseTypes#1](../code-quality/codesnippet/VisualBasic/ca1405-com-visible-type-base-types-should-be-com-visible_1.vb)]
[!code-csharp[FxCop.Interoperability.ComBaseTypes#1](../code-quality/codesnippet/CSharp/ca1405-com-visible-type-base-types-should-be-com-visible_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Runtime.InteropServices.ClassInterfaceAttribute?displayProperty=fullName>
- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)