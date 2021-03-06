---
title: 'CA3006: İşlem komutu ekleme güvenlik açıkları için inceleme kodu'
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
ms.openlocfilehash: 986607d7f42f49c99396bbb021c48bad549930c9
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237287"
---
# <a name="ca3006-review-code-for-process-command-injection-vulnerabilities"></a>CA3006: İşlem komutu ekleme güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|Belgeınlist Codeforprocesscommandinjectionaçıklardan|
|CheckId|CA3006|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Güvenilir olmayan HTTP isteği girişi bir işlem komutuna ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilmeyen girişle çalışırken, komut ekleme saldırılarına karşı bir sorun yaşının. Bir komut ekleme saldırısı, temel işletim sisteminde kötü amaçlı komutlar yürütebilir ve sunucunuzun güvenliğini ve bütünlüğünü tehlikeye atabilirler.

Bu kural, HTTP isteklerinden bir işlem komutuna ulaşan girişi bulmaya çalışır.

> [!NOTE]
> Bu kural derlemeler genelinde verileri izleyemez. Örneğin, bir derleme HTTP istek girişini okur ve sonra işlemi başlatan başka bir derlemeye geçirir, bu kural bir uyarı oluşturmaz.

> [!NOTE]
> Bu kuralın, yöntem çağrılarında veri akışını ne kadar analiz edip bu kurala ilişkin yapılandırılabilir bir sınır vardır. Bir EditorConfig dosyasında sınırı yapılandırma hakkında bilgi için bkz. [çözümleyici yapılandırması](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) .

## <a name="how-to-fix-violations"></a>İhlalleri çözme

- Mümkünse, işlem kullanıcı girişine göre başlatılmaktan kaçının.
- Girişin bilinen bir dizi güvenli karakter ve uzunluğa karşı doğrulanması.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Girişin doğrulandığını veya güvenli olduğunu biliyorsanız, bu uyarıyı bastırmak güvenlidir.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>Edildiği

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
