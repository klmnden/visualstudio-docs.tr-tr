---
title: 'CA3007: Açık yeniden yönlendirme güvenlik açıkları için inceleme kodu'
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
ms.openlocfilehash: dbafb6c05a3dba72d1614d6a955e20030a50c6ea
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60096718"
---
# <a name="ca3007-review-code-for-open-redirect-vulnerabilities"></a>CA3007: Açık yeniden yönlendirme güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForOpenRedirectVulnerabilities|
|CheckId|CA3007|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP istek girişi HTTP yanıt yeniden yönlendirmesi ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilmeyen girdisiyle çalışırken, açık yeniden yönlendirme güvenlik açıklarını gösteren oluşturduğunu unutmayın. Bir saldırgan, Web sitenizi meşru bir URL görünümünü sağlar, ancak duymayan bir ziyaretçi için bir kimlik avı veya diğer kötü amaçlı Web sayfası yeniden yönlendirme için kullanılacak bir açık yeniden yönlendirme güvenlik açığından yararlanabilir.

Bu kural, bir HTTP yeniden yönlendirme URL'si ulaşmasını HTTP isteklerinden alınan giriş bulmayı dener.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve bir HTTP yeniden yönlendirme ile yanıt veren başka bir derlemeye geçirir, bu kural bir uyarı üreten olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Açık yeniden yönlendirme güvenlik açıklarını düzeltme için aşağıdaki yaklaşımlardan şunlardır:

- Yeniden yönlendirmeleri başlatmak kullanıcılara izin verme.
- Kullanıcılar bir yeniden yönlendirme senaryosunda herhangi bir bölümünü URL'yi belirtmek izin verme.
- Yeniden yönlendirmeleri, bir önceden tanımlanmış "izin" URL'lerin listesini sınırlayın.
- Doğrulama URL'lerini yönlendirmek.
- Varsa bir bildirim sayfası kullandığınızda Kullanıcılar sitenizi uzağa Rehbere yönlendiriliyorsunuz göz önünde bulundurun.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Hedeflenen URL'lere sınırlanması giriş doğruladınız biliyorsanız, bu uyarının gösterilmemesi uygundur.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string input = Request.Form["url"];
        this.Response.Redirect(input);
    }
}
```

```vb
Imports System

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, eventArgs As EventArgs)
        Dim input As String = Me.Request.Form("url")
        Me.Response.Redirect(input)
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
        if (String.IsNullOrWhiteSpace(input))
        {
            this.Response.Redirect("https://example.org/login.html");
        }
    }
}
```

```vb
Imports System

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, eventArgs As EventArgs)
        Dim input As String = Me.Request.Form("in")
        If String.IsNullOrWhiteSpace(input) Then
            Me.Response.Redirect("https://example.org/login.html")
        End If
    End Sub
End Class
```
