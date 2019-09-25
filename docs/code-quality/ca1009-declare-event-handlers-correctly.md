---
title: 'CA1009: Olay işleyicileri doğru olarak bildirin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1009
- DeclareEventHandlersCorrectly
helpviewer_keywords:
- CA1009
- DeclareEventHandlersCorrectly
ms.assetid: ab65c471-1449-49d2-9896-7b9af74284b4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: e923730213ca31a4429d8547fdaaf980692f9a96
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236485"
---
# <a name="ca1009-declare-event-handlers-correctly"></a>CA1009: Olay işleyicileri doğru olarak bildirin

|||
|-|-|
|TypeName|DeclareEventHandlersCorrectly|
|CheckId|CA1009|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak veya korumalı bir olayı işleyen bir temsilcinin doğru imza, dönüş türü veya parametre adı yoktur.

## <a name="rule-description"></a>Kural açıklaması
Olay işleyicisi yöntemleri iki parametre alır. İlki türdür <xref:System.Object?displayProperty=fullName> ve ' sender ' olarak adlandırılmıştır. Bu olayda oluşan nesnedir. İkinci parametre türündedir <xref:System.EventArgs?displayProperty=fullName> ve ' e ' olarak adlandırılmıştır. Bu olay ile ilişkilendirilmiş olan verilerdir. Örneğin, bir dosya her açıldığında olay ortaya çıktığında, olay verileri genellikle dosyanın adını içerir.

Olay işleyicisi yöntemleri bir değer döndürmemelidir. C# Programlama dilinde bu, dönüş türü `void`tarafından belirtilir. Bir olay işleyicisi, birden çok nesnede birden çok yöntemi çağırabilir. Yöntemlerin bir değer döndürmesine izin veriliyorsa, her olay için birden çok dönüş değeri oluşur ve yalnızca çağrılan son metodun değeri kullanılabilir olur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini düzeltmek için, temsilcinin imzasını, dönüş türünü veya parametre adlarını düzeltin. Ayrıntılar için aşağıdaki örneğe bakın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, olayları işlemeye uygun bir temsilciyi gösterir. Bu olay işleyicisi tarafından çağrılabilen Yöntemler, tasarım yönergelerine göre belirtilen imzaya uyum sağlayabilir. `AlarmEventHandler`temsilcinin tür adıdır. `AlarmEventArgs`<xref:System.EventArgs>, olay verileri için temel sınıftan türetilir ve uyarı olay verilerini barındırır.

[!code-cpp[FxCop.Design.EventsTwoParams#1](../code-quality/codesnippet/CPP/ca1009-declare-event-handlers-correctly_1.cpp)]
[!code-csharp[FxCop.Design.EventsTwoParams#1](../code-quality/codesnippet/CSharp/ca1009-declare-event-handlers-correctly_1.cs)]
[!code-vb[FxCop.Design.EventsTwoParams#1](../code-quality/codesnippet/VisualBasic/ca1009-declare-event-handlers-correctly_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA2109 Görünür olay işleyicilerini gözden geçirme](../code-quality/ca2109-review-visible-event-handlers.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.EventArgs?displayProperty=fullName>
- <xref:System.Object?displayProperty=fullName>
- [Olayları işleme ve oluşturma](/dotnet/standard/events/index)