---
title: 'CA3012: Normal ifade ekleme güvenlik açıkları için inceleme kodu'
ms.date: 04/03/2019
ms.topic: reference
author: dotpaul
ms.author: paulming
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 114b44ec566554c81f5caf3b8ac474f9c5a75c07
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60106260"
---
# <a name="ca3012-review-code-for-regex-injection-vulnerabilities"></a>CA3012: Normal ifade ekleme güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForRegexInjectionVulnerabilities|
|CheckId|CA3012|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP istek girişi, normal bir ifade ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilmeyen girdisiyle çalışırken, normal ifade ekleme saldırıları oluşturduğunu unutmayın. Bir saldırganın normal ifade ekleme, normal bir ifade, istenmeyen sonuçları eşleşen normal ifade yapma veya bir hizmet reddi saldırısına kaynaklanan aşırı CPU kullanma regex yapmak için kötü amaçlı olarak değiştirmek için kullanabilirsiniz.

Bu kural, bir normal ifade ulaşmasını HTTP isteklerinden alınan giriş bulmayı dener.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve normal bir ifade oluşturur, başka bir derlemeye geçtikten sonra bu kural bir uyarı üretir olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Regex eklemelerini karşı bazı risk azaltma işlemleri şunlardır:

- Her zaman bir [eşleşmesi zaman aşımı](/dotnet/standard/base-types/best-practices#use-time-out-values) normal ifadeler kullanarak.
- Kullanıcı girişini temel alarak normal ifadeler kullanmaktan kaçının.
- Çağırarak kullanıcı girişi ile özel karakterleri kaçış <xref:System.Text.RegularExpressions.Regex.Escape%2A?displayProperty=fullName> veya başka bir yöntem.
- Kullanıcı girişi yalnızca özel dışı karakterler sağlar.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Kullanmakta olduğunuz biliyorsanız bir [eşleşmesi zaman aşımı](/dotnet/standard/base-types/best-practices#use-time-out-values) ve özel karakterler kullanıcı girişi ücretsizdir, bu uyarının gösterilmemesi uygundur.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;
using System.Text.RegularExpressions;

public partial class WebForm : System.Web.UI.Page
{
    public string SearchableText { get; set; }

    protected void Page_Load(object sender, EventArgs e)
    {
        string findTerm = Request.Form["findTerm"];
        Match m = Regex.Match(SearchableText, "^term=" + findTerm);
    }
}
```

```vb
Imports System
Imports System.Text.RegularExpressions

Public Partial Class WebForm
    Inherits System.Web.UI.Page

    Public Property SearchableText As String

    Protected Sub Page_Load(sender As Object, e As EventArgs)
        Dim findTerm As String = Request.Form("findTerm")
        Dim m As Match = Regex.Match(SearchableText, "^term=" + findTerm)
    End Sub
End Class
```
