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
ms.openlocfilehash: 4965c9df3c2256511b8e44de8d388a9155d0d8f9
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237371"
---
# <a name="ca3004-review-code-for-information-disclosure-vulnerabilities"></a>CA3004: Bilgilerin açığa çıkmasıyla ilgili güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForInformationDisclosureVulnerabilities|
|CheckId|CA3004|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir özel durumun iletisi, yığın izlemesi veya dize temsili Web çıktısına ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Özel durum bilgilerini kapatma, saldırganlar uygulamanızın iç içgörüleri hakkında bilgi verir ve bu da saldırganların açıktan yararlanmaya yönelik diğer güvenlik açıklarını bulmasına yardımcı olabilir.

Bu kural bir HTTP yanıtına çıkış yapmak için bir özel durum iletisi, yığın izlemesi veya dize temsili bulmaya çalışır.

> [!NOTE]
> Bu kural derlemeler genelinde verileri izleyemez. Örneğin, bir derleme bir özel durumu yakalar ve sonra özel durumu çıkaran başka bir derlemeye geçerse, bu kural bir uyarı oluşturmaz.

> [!NOTE]
> Bu kuralın, yöntem çağrılarında veri akışını ne kadar analiz edip bu kurala ilişkin yapılandırılabilir bir sınır vardır. Bir EditorConfig dosyasında sınırı yapılandırma hakkında bilgi için bkz. [çözümleyici yapılandırması](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) .

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Özel durum bilgilerini HTTP yanıtlarına gönderme. Bunun yerine, genel bir hata iletisi sağlayın. Daha fazla rehberlik için bkz. [OWASP 'Nin hata işleme sayfası](https://www.owasp.org/index.php/Error_Handling) .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Web çıktınızın uygulamanızın güven sınırının içinde olduğunu ve hiç gösterilmediğini biliyorsanız, bu uyarıyı bastırmak normaldir. Bu çok nadir bir durumdur. Uygulamanızın güven sınırının ve veri akışlarının zaman içinde değişeceği göz önünde bulundurun.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>Edildiği

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