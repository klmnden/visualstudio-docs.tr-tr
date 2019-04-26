---
title: 'CA3002: XSS güvenlik açıkları için inceleme kodu'
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
ms.openlocfilehash: a10f72297746a1e7bda3c69f8f7daf0efacd20bc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541278"
---
# <a name="ca3002-review-code-for-xss-vulnerabilities"></a>CA3002: XSS güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForXssVulnerabilities|
|CheckId|CA3002|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP istek girişi ham HTML çıktısı ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilir olmayan girişlere karşı web isteklerinden ile çalışırken, siteler arası betik (XSS) saldırıları oluşturduğunu unutmayın. XSS saldırının güvenilmeyen bir giriş sağlar saldırgan kötü amaçlı komut dosyalarını çalıştırmak ve erişemeyeceği web sayfanızın içeriği değiştirmek ham HTML çıktısını içine yerleştirir. Tipik bir teknik koyuyor `<script>` kötü amaçlı kod içinde giriş öğelerle. Daha fazla bilgi için [OWASP'ın XSS](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)).

Bu kural, ham HTML çıktısı ulaşmasını HTTP isteklerinden alınan giriş bulmayı dener.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve işlenmemiş HTML'yi veren başka bir derlemeye geçirir, bu kural bir uyarı üreten olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Ham HTML çıktısı yerine bir yöntem veya özellik, giriş bu ilk HTML olarak kodlar kullanın.
- HTML kodlama ham HTML çıktısı önce veri güvenilmeyen.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu, bu kuraldan bir uyarıyı bastırmak güvenli değil:
- Bildiğiniz giriş güvenli HTML içermeyen karakter kümesi bilinen karşı doğrulanır.
- Bu kural tarafından algılanmayan şekilde HTML olarak kodlanmış veriler, bildiğiniz.

> [!NOTE]
> Bu kural, HTML olarak kodlamak için bazı yöntemleri veya özellikleri hatalı pozitif sonuçları bildirebilir, giriş.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string input = Request.Form["in"];
        Response.Write("<HTML>" + input + "</HTML>");
    }
}
```

```vb
Imports System

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, e As EventArgs)
        Dim input As String = Me.Request.Form("in")
        Me.Response.Write("<HTML>" + input + "</HTML>")
    End Sub
End Class
```

### <a name="solution"></a>Çözüm

```csharp
using System;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string input = Request.Form["in"];

        // Example usage of System.Web.HttpServerUtility.HtmlEncode().
        Response.Write("<HTML>" + Server.HtmlEncode(input) + "</HTML>");
    }
}
```

```vb
Imports System

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, e As EventArgs)
        Dim input As String = Me.Request.Form("in")

        ' Example usage of System.Web.HttpServerUtility.HtmlEncode().
        Me.Response.Write("<HTML>" + Me.Server.HtmlEncode(input) + "</HTML>")
    End Sub
End Class
```