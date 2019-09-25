---
title: 'CA1414: Boole P-Invoke bağımsız değişkenlerini MarshalAs ile işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1414
- MarkBooleanPInvokeArgumentsWithMarshalAs
helpviewer_keywords:
- CA1414
- MarkBooleanPInvokeArgumentsWithMarshalAs
ms.assetid: c0c84cf5-7701-4897-9114-66fc4b895699
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 22e62a1e3209399be4b10a3ec28db4afdd6f0f20
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234667"
---
# <a name="ca1414-mark-boolean-pinvoke-arguments-with-marshalas"></a>CA1414: Boolean P/Invoke bağımsız değişkenlerini MarshalAs ile işaretleyin

|||
|-|-|
|TypeName|MarkBooleanPInvokeArgumentsWithMarshalAs|
|CheckId|CA1414|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Platform çağırma yöntemi bildirimi bir <xref:System.Boolean?displayProperty=fullName> parametre veya dönüş değeri içeriyor, <xref:System.Runtime.InteropServices.MarshalAsAttribute?displayProperty=fullName> ancak öznitelik parametreye veya dönüş değerine uygulanmıyor.

## <a name="rule-description"></a>Kural açıklaması
Platform çağırma yöntemi yönetilmeyen koda erişir ve içindeki veya `Declare` <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] anahtar sözcüğü kullanılarak tanımlanır. <xref:System.Runtime.InteropServices.MarshalAsAttribute>yönetilen ve yönetilmeyen kod arasında veri türlerini dönüştürmek için kullanılan sıralama davranışını belirtir. <xref:System.Byte?displayProperty=fullName> Ve<xref:System.Int32?displayProperty=fullName>gibi birçok basit veri türü, yönetilmeyen kodda tek bir gösterimine sahiptir ve sıralama davranışının belirtimini gerektirmez; ortak dil çalışma zamanı, doğru davranışı otomatik olarak sağlar.

<xref:System.Boolean> Veri türünün yönetilmeyen kodda birden çok temsili vardır. Belirtilmediğinde, <xref:System.Boolean> veri türü için varsayılan sıralama davranışı olur <xref:System.Runtime.InteropServices.UnmanagedType?displayProperty=fullName>. <xref:System.Runtime.InteropServices.MarshalAsAttribute> Bu, tüm koşullarda uygun olmayan 32 bitlik bir tamsayıdır. Yönetilmeyen yöntemin gerektirdiği Boolean temsili, uygun <xref:System.Runtime.InteropServices.UnmanagedType?displayProperty=fullName>şekilde belirlenmeli ve eşleştirilir. UnmanagedType. bool, her zaman 4 bayt olan Win32 BOOL türüdür. UnmanagedType. U1 veya diğer 1 baytlık C++ `bool` türler için kullanılmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için <xref:System.Runtime.InteropServices.MarshalAsAttribute> <xref:System.Boolean> parametreye veya dönüş değerine uygulayın. Özniteliğin değerini uygun <xref:System.Runtime.InteropServices.UnmanagedType>olarak ayarlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın. Varsayılan sıralama davranışı uygun olsa da, davranış açıkça belirtildiğinde kod daha kolay korunur.

## <a name="example"></a>Örnek

Aşağıdaki örnek, uygun <xref:System.Runtime.InteropServices.MarshalAsAttribute> özniteliklerle işaretlenmiş platform çağırma yöntemlerini gösterir.

[!code-csharp[FxCop.Interoperability.BoolMarshalAs#1](../code-quality/codesnippet/CSharp/ca1414-mark-boolean-p-invoke-arguments-with-marshalas_1.cs)]
[!code-vb[FxCop.Interoperability.BoolMarshalAs#1](../code-quality/codesnippet/VisualBasic/ca1414-mark-boolean-p-invoke-arguments-with-marshalas_1.vb)]
[!code-cpp[FxCop.Interoperability.BoolMarshalAs#1](../code-quality/codesnippet/CPP/ca1414-mark-boolean-p-invoke-arguments-with-marshalas_1.cpp)]

## <a name="related-rules"></a>İlgili kurallar
[CA1901 P/Invoke bildirimleri taşınabilir olmalıdır](../code-quality/ca1901-p-invoke-declarations-should-be-portable.md)

[CA2101 P/Invoke dize bağımsız değişkenleri için sıralama belirtin](../code-quality/ca2101-specify-marshaling-for-p-invoke-string-arguments.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Runtime.InteropServices.UnmanagedType?displayProperty=fullName>
- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)