---
title: 'CA1009: Olay işleyicilerini doğru bildirin | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1009
- DeclareEventHandlersCorrectly
helpviewer_keywords:
- CA1009
- DeclareEventHandlersCorrectly
ms.assetid: ab65c471-1449-49d2-9896-7b9af74284b4
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ba96dbced72ae4d1cd51e05f55670186eb72def6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53893493"
---
# <a name="ca1009-declare-event-handlers-correctly"></a>CA1009: Olay işleyicilerini doğru bildirin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DeclareEventHandlersCorrectly|
|CheckId|CA1009|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı bir olay işleme bir temsilci türü veya parametre adları, doğru imzaya sahip değil.

## <a name="rule-description"></a>Kural Tanımı
 Olay işleyicisi yöntemleri iki parametre alır. İlk türünde <xref:System.Object?displayProperty=fullName> ve 'sender' olarak adlandırılır. Bu olayda oluşan nesnedir. İkinci parametre türüdür <xref:System.EventArgs?displayProperty=fullName> ve 'e' olarak adlandırılır. Bu olay ile ilişkilendirilmiş olan verilerdir. Örneğin, olay verileri, genellikle her bir dosya açıldığında olay tetiklenir, dosya adını içerir.

 Olay işleyicisi yöntemleri bir değer döndürmemelidir. C# programlama diliyle, bu dönüş türü tarafından belirtilen `void`. Bir olay işleyicisi, birden çok nesne içinde birden çok yöntem çağırabilirsiniz. Yöntem bir değer döndürmek için izin verilirse, birden çok değer, her olay için ortaya çıkabilecek ve yalnızca son yöntemi çağrıldı değerini kullanılabilir olur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için imza, dönüş türü veya temsilcinin parametre adları düzeltin. Ayrıntılar için aşağıdaki örneğe bakın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, olayları işlemek için uygun olan bir temsilci gösterir. Bu olay işleyicisi tarafından çağrılan yöntemler tasarım yönergeleri ile ortaya belirtilen imzaya uymanız. `AlarmEventHandler` metot temsilcisinin tür adıdır. `AlarmEventArgs` Olay verileri için bir temel sınıftan türetilen <xref:System.EventArgs>, ve alarm olay verilerini tutar.

 [!code-cpp[FxCop.Design.EventsTwoParams#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.EventsTwoParams/cpp/FxCop.Design.EventsTwoParams.cpp#1)]
 [!code-csharp[FxCop.Design.EventsTwoParams#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.EventsTwoParams/cs/FxCop.Design.EventsTwoParams.cs#1)]
 [!code-vb[FxCop.Design.EventsTwoParams#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.EventsTwoParams/vb/FxCop.Design.EventsTwoParams.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2109: Görünen olay işleyicileri gözden geçirin](../code-quality/ca2109-review-visible-event-handlers.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.EventArgs?displayProperty=fullName><xref:System.Object?displayProperty=fullName>
 [NIB: Olaylar ve temsilciler](http://msdn.microsoft.com/en-us/d98fd58b-fa4f-4598-8378-addf4355a115)
