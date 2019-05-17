---
title: 'CA3003: Dosya yolu ekleme güvenlik açıkları için inceleme kodu'
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
ms.openlocfilehash: b81bd810bac142bdec23074e69bbd3840043c8f6
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65841402"
---
# <a name="ca3003-review-code-for-file-path-injection-vulnerabilities"></a>CA3003: Dosya yolu ekleme güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForFilePathInjectionVulnerabilities|
|CheckId|CA3003|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP istek girişi dosya işlemi yolunu ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilir olmayan girişlere karşı web isteklerinden ile çalışırken, kullanıcı tarafından denetlenen giriş dosyalara olan yolları belirtirken kullanarak oluşturduğunu unutmayın. Bir saldırganın hassas veri bilgilerini açığa çıkmasına neden olabilecek istenmeyen bir dosyayı okumak mümkün olabilir. Veya, bir saldırganın hassas verilerin yetkisiz değişiklik kaynaklanan veya sunucunun güvenlikten ödün istenmeyen bir dosyaya yazmak mümkün olabilir. Ortak bir saldırganın teknik [yol çapraz geçişi](https://www.owasp.org/index.php/Path_Traversal) hedeflenen dizin dışındaki dosyalara erişmek için.

Bu kural, bir yolda bir dosya işlemi ulaşmasını HTTP isteklerinden alınan giriş bulmayı dener.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve bir dosyaya yazar başka bir derlemeye geçirir, bu kural bir uyarı üreten olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı bir EditorConfig dosyasında nasıl yapılandıracağınızı öğrenmek için.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Mümkünse, dosya yolları kullanıcı girişi açıkça bilinen ve güvenli bir listeye göre sınırlayın.  Örneğin, uygulamanız yalnızca "red.txt", "green.txt" veya "blue.txt" erişmesi gerekiyorsa, yalnızca bu değerlere izin.
- Güvenilmeyen dosya adları için denetleyin ve ad biçimlendirilmemiş doğrulayın.
- Yolları belirtirken tam yol adları kullanın.
- Path ortam değişkenleri gibi potansiyel olarak tehlikeli olabilecek yapıları kaçının.
- Yalnızca uzun dosya adları kabul edin ve kısa adları kullanıcının gönderdiğini, uzun adını doğrulayın.
- Son kullanıcı girişi için geçerli karakterler kısıtlayın.
- Burada MAX_PATH uzunluk aşıldığında adları reddeder.
- Dosya adları, tam anlamıyla, yorumlama olmadan işleyin.
- Dosya adında bir dosya veya bir cihazı temsil edip etmediğini belirler.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Önceki bölümde açıklandığı gibi giriş onayladıysanız Bu uyarının gösterilmemesi uygundur.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;
using System.IO;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string userInput = Request.Params["UserInput"];
        // Assume the following directory structure:
        //   wwwroot\currentWebDirectory\user1.txt
        //   wwwroot\currentWebDirectory\user2.txt
        //   wwwroot\secret\allsecrets.txt
        // There is nothing wrong if the user inputs:
        //   user1.txt
        // However, if the user input is:
        //   ..\secret\allsecrets.txt
        // Then an attacker can now see all the secrets.

        // Avoid this:
        using (File.Open(userInput, FileMode.Open))
        {
            // Read a file with the name supplied by user
            // Input through request's query string and display
            // The content to the webpage.
        }
    }
}
```

```vb
Imports System
Imports System.IO

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(sender As Object, e As EventArgs)
        Dim userInput As String = Me.Request.Params("UserInput")
        ' Assume the following directory structure:
        '   wwwroot\currentWebDirectory\user1.txt
        '   wwwroot\currentWebDirectory\user2.txt
        '   wwwroot\secret\allsecrets.txt
        ' There is nothing wrong if the user inputs:
        '   user1.txt
        ' However, if the user input is:
        '   ..\secret\allsecrets.txt
        ' Then an attacker can now see all the secrets.

        ' Avoid this:
        Using File.Open(userInput, FileMode.Open)
            ' Read a file with the name supplied by user
            ' Input through request's query string and display
            ' The content to the webpage.
        End Using
    End Sub
End Class
```
