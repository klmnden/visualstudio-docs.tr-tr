---
title: 'CA1412: ComSource arabirimlerini IDispatch olarak işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MarkComSourceInterfacesAsIDispatch
- CA1412
helpviewer_keywords:
- CA1412
- MarkComSourceInterfacesAsIDispatch
ms.assetid: 131a7563-0410-443c-a8f5-52104250cfb4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: caaae787d5e4801f3fc3b8d881b386595fb2eca4
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234683"
---
# <a name="ca1412-mark-comsource-interfaces-as-idispatch"></a>CA1412: ComSource arabirimlerini IDispatch olarak işaretleyin

|||
|-|-|
|TypeName|MarkComSourceInterfacesAsIDispatch|
|CheckId|CA1412|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür, <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> özniteliğiyle işaretlenmiş ve en az bir belirtilen arabirim, `InterfaceIsDispatch` değer olarak ayarlanan <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> öznitelik ile işaretlenmemiş.

## <a name="rule-description"></a>Kural açıklaması

<xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute>, bir sınıfın bileşen nesne modeli (COM) istemcilerine sunduğu olay arabirimlerini belirlemek için kullanılır. Bu arabirimler, Visual Basic 6 com `InterfaceIsIDispatch` istemcilerinin olay bildirimleri almasını sağlamak için olarak sunulmalıdır. Varsayılan olarak, bir arabirim <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> özniteliğiyle işaretlenmemişse, Çift arabirim olarak sunulur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> özniteliği, özniteliği <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> ile belirtilen tüm arabirimler için değeri ınterfaceisidispatch olarak ayarlanacak şekilde ekleyin veya değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örnek, arayüzlerden birinin kuralı ihlal ettiğini gösteren bir sınıfı gösterir.

[!code-csharp[FxCop.Interoperability.MarkIDispatch#1](../code-quality/codesnippet/CSharp/ca1412-mark-comsource-interfaces-as-idispatch_1.cs)]
[!code-vb[FxCop.Interoperability.MarkIDispatch#1](../code-quality/codesnippet/VisualBasic/ca1412-mark-comsource-interfaces-as-idispatch_1.vb)]

## <a name="related-rules"></a>İlgili kurallar

[CA1408 Oto Dual ClassInterfaceType kullanmayın](../code-quality/ca1408-do-not-use-autodual-classinterfacetype.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)