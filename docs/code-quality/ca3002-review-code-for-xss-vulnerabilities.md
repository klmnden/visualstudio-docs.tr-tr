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
ms.openlocfilehash: 6bcf32401abdeae499097bc5187d11154e7dfc6e
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237413"
---
# <a name="ca3002-review-code-for-xss-vulnerabilities"></a>CA3002: XSS güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|Belgekodu Koduforxssaçıklarına|
|CheckId|CA3002|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Güvenilmeyen HTTP isteği girişi ham HTML çıktısına ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Web isteklerinden güvenilmeyen giriş ile çalışırken, siteler arası komut dosyası (XSS) saldırıları olması gerekir. Bir XSS saldırısı, güvenilmeyen bir girişi ham HTML çıktısına çıkarır ve saldırganın kötü amaçlı betikler yürütmesine veya Web sayfanızda içeriği kötü amaçlı olarak değiştirmesine olanak tanır. Tipik bir teknik, öğeleri `<script>` girişte kötü amaçlı kod ile yerleştirmektir. Daha fazla bilgi için bkz. [OWASP 'nın XSS](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)).

Bu kural, ham HTML çıktısına ulaşan HTTP isteklerinden girdi bulmaya çalışır.

> [!NOTE]
> Bu kural derlemeler genelinde verileri izleyemez. Örneğin, bir derleme HTTP istek girişini okur ve sonra ham HTML çıkışı yapan başka bir derlemeye geçerse, bu kural bir uyarı oluşturmaz.

> [!NOTE]
> Bu kuralın, yöntem çağrılarında veri akışını ne kadar analiz edip bu kurala ilişkin yapılandırılabilir bir sınır vardır. Bir EditorConfig dosyasında sınırı yapılandırma hakkında bilgi için bkz. [çözümleyici yapılandırması](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) .

## <a name="how-to-fix-violations"></a>İhlalleri çözme

- Ham HTML çıktısı yerine, ilk HTML kodlayan bir yöntemi veya özelliği kullanın.
- HTML-ham HTML yazmadan önce güvenilmeyen verileri kodla.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Şu durumlarda bu kuraldan bir uyarı bastırmak güvenlidir:
- Girişin HTML içermeyen, bilinen bir güvenli karakter kümesine göre doğrulanacağını bilirsiniz.
- Verilerin HTML kodlamalı olduğunu, bu kural tarafından algılanmadığı bir şekilde anlarsınız.

> [!NOTE]
> Bu kural, HTML-girişlerini kodlayan bazı yöntemler veya özellikler için hatalı pozitif sonuçlar bildirebilir.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>Edildiği

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