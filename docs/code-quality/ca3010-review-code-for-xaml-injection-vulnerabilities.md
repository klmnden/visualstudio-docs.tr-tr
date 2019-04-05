---
title: 'CA3010: XAML ekleme güvenlik açıklarına yönelik kod gözden geçirme'
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
ms.openlocfilehash: c6d8a94dbda7cbf61ac918025aee176cb95781b2
ms.sourcegitcommit: b6177ce198c7c5a00030604c9d4faa735405d5df
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59018898"
---
# <a name="ca3010-review-code-for-xaml-injection-vulnerabilities"></a>CA3010: XAML ekleme güvenlik açıklarına yönelik kod gözden geçirme

|||
|-|-|
|TypeName|ReviewCodeForXamlInjectionVulnerabilities|
|CheckId|CA3010|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP isteği giriş ulaştığında bir <xref:System.Windows.Markup.XamlReader?displayProperty=fullName> yükleme yöntemi.

## <a name="rule-description"></a>Kural açıklaması

Güvenilmeyen girdisiyle çalışırken, XAML ekleme saldırıları oluşturduğunu unutmayın. XAML doğrudan nesne örneklemesini ve yürütme temsil eden bir biçimlendirme dilidir. XAML içinde oluşturulan öğeler, sistem kaynakları (örneğin, ağ erişimi ve dosya sistemi g/ç) ile etkileşim kurabilir anlamına gelir. Bir saldırganın giriş kontrol edebilirsiniz, bir <xref:System.Windows.Markup.XamlReader?displayProperty=nameWithType> saldırgan kodu yürütmeden sonra Yük yöntem çağrısı.

Bu kural, HTTP isteklerinden alınan ulaştığında giriş bulmayı dener bir <xref:System.Windows.Markup.XamlReader?displayProperty=nameWithType> yükleme yöntemi.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve XAML yükleyen başka bir derlemeye geçtikten sonra bu kural bir uyarı üreten olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Güvenilmeyen XAML yükleme.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıları bastırma yok.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;
using System.IO;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string input = Request.Form["in"];
        byte[] bytes = Convert.FromBase64String(input);
        MemoryStream ms = new MemoryStream(bytes);
        System.Windows.Markup.XamlReader.Load(ms);
    }
}
```

```vb
Imports System
Imports System.IO

Public Partial Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, e As EventArgs)
        Dim input As String = Request.Form("in")
        Dim bytes As Byte() = Convert.FromBase64String(input)
        Dim ms As MemoryStream = New MemoryStream(bytes)
        System.Windows.Markup.XamlReader.Load(ms)
    End Sub
End Class
```
