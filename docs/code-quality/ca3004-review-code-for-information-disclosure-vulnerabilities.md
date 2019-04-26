---
title: 'CA3004: Bilgilerin açığa çıkmasıyla ilgili güvenlik açıkları için inceleme kodu'
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
ms.openlocfilehash: 82f763d9a6b1ec27975aa80054456a6bbbaeaa2b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541277"
---
# <a name="ca3004-review-code-for-information-disclosure-vulnerabilities"></a>CA3004: Bilgilerin açığa çıkmasıyla ilgili güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForInformationDisclosureVulnerabilities|
|CheckId|CA3004|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Özel durum iletisi, yığın izlemesi veya dize gösterimi web çıkış ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Özel durum bilgilerini açığa çıkarmaktan saldırganlar yardımcı olur, uygulamanızın iç işlevleri hakkında bilgi bulmak diğer güvenlik açıklarından yararlanma saldırganlar sağlar.

Bu kural, bir özel durum iletisi, yığın izlemesi veya çıkış için bir HTTP yanıtı olan dize gösterimi bulmaya çalışır.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir bütünleştirilmiş kod bir özel durumu yakalar ve özel durum veren başka bir derlemeye geçirir, bu kural bir uyarı üreten olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Özel durum bilgilerini HTTP yanıtları için çıktı yok. Bunun yerine, genel bir hata iletisi sağlayın. Bkz: [OWASP'ın hata işleme sayfası](https://www.owasp.org/index.php/Error_Handling) daha fazla kılavuzluk için.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Web çıkışınızı uygulamanızın güven sınırı içinde ve dışında hiçbir zaman kullanıma sunulan, bu uyarının gösterilmemesi için biliyorsanız. Bu nadir olarak rastlanıyor. Uygulamanızın güven sınırı ve veri akışlarını, zaman içinde değişebilir dikkate alın.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs eventArgs)
    {
        try
        {
            object o = null;
            o.ToString();
        }
        catch (Exception e)
        {
            this.Response.Write(e.ToString());
        }
    }
}
```

```vb
Imports System

Partial Public Class WebForm 
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, eventArgs As EventArgs)
        Try
            Dim o As Object = Nothing
            o.ToString()
        Catch e As Exception
            Me.Response.Write(e.ToString())
        End Try
    End Sub
End Class
```

### <a name="solution"></a>Çözüm

```csharp
using System;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs eventArgs)
    {
        try
        {
            object o = null;
            o.ToString();
        }
        catch (Exception e)
        {
            this.Response.Write("An error occurred. Please try again later.");
        }
    }
}
```

```vb
Imports System

Partial Public Class WebForm 
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, eventArgs As EventArgs)
        Try
            Dim o As Object = Nothing
            o.ToString()
        Catch e As Exception
            Me.Response.Write("An error occurred. Please try again later.")
        End Try
    End Sub
End Class
```