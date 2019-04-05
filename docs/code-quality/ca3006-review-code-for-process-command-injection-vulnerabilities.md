---
title: 'CA3006: İşlem komut ekleme güvenlik açıklarına yönelik kod gözden geçirme'
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
ms.openlocfilehash: da161e611ca1d802c8da16370907029233bfd785
ms.sourcegitcommit: b6177ce198c7c5a00030604c9d4faa735405d5df
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59018867"
---
# <a name="ca3006-review-code-for-process-command-injection-vulnerabilities"></a>CA3006: İşlem komut ekleme güvenlik açıklarına yönelik kod gözden geçirme

|||
|-|-|
|TypeName|ReviewCodeForProcessCommandInjectionVulnerabilities|
|CheckId|CA3006|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP istek girişi process komutu ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilmeyen girdisiyle çalışırken, komut ekleme saldırıları oluşturduğunu unutmayın. Bir komut ekleme saldırısına temel alınan işletim güvenliğini ve bütünlüğünü sunucunuzun ödün sistemde kötü amaçlı komutlar yürütebilir.

Bu kural, bir işlem komut ulaşmasını HTTP isteklerinden alınan giriş bulmayı dener.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve bir işlem başlatır, başka bir derlemeye geçtikten sonra bu kural bir uyarı üreten olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Mümkünse, kullanıcı girişini temel alarak işlemlerini başlatma kaçının.
- Giriş karakter ve uzunluğu ile ilgili bilinen bir güvenli kümesi karşı doğrulayın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Girişi doğrulanması veya güvenli olacak şekilde Atlanan biliyorsanız, bu uyarının gösterilmemesi güvenlidir.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;
using System.Diagnostics;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string input = Request.Form["in"];
        Process p = Process.Start(input);
    }
}
```

```vb
Imports System
Imports System.Diagnostics

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, eventArgs as EventArgs)
        Dim input As String = Me.Request.Form("in")
        Dim p As Process = Process.Start(input)
    End Sub
End Class
```
