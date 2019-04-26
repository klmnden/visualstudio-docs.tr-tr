---
title: 'CA3005: LDAP ekleme güvenlik açıkları için inceleme kodu'
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
ms.openlocfilehash: 38c28153fa513c4f4db5b3a7833d279674f66734
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541304"
---
# <a name="ca3005-review-code-for-ldap-injection-vulnerabilities"></a>CA3005: LDAP ekleme güvenlik açıkları için inceleme kodu

|||
|-|-|
|TypeName|ReviewCodeForLdapInjectionVulnerabilities|
|CheckId|CA3005|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Potansiyel olarak güvenilmeyen HTTP istek girişi bir LDAP deyimi ulaşır.

## <a name="rule-description"></a>Kural açıklaması

Güvenilmeyen girdisiyle çalışırken, Basit Dizin Erişim Protokolü (LDAP) ekleme saldırıları oluşturduğunu unutmayın. Bir saldırgan, olası kötü amaçlı LDAP deyimleri bilgi dizinleri karşı çalıştırabilirsiniz. Kullanıcı girişi dizin hizmetlerine erişmek için dinamik LDAP ifadeleri oluşturmak için kullandıkları uygulamalarda özellikle savunmasızdır.

Bu kural, bir LDAP deyimi ulaşmasını HTTP isteklerinden alınan giriş bulmayı dener.

> [!NOTE]
> Bu kural, derlemeler arasında veri izleyemezsiniz. Örneğin, bir derleme HTTP istek girişi okur ve bir LDAP deyimi yürütür, başka bir derlemeye geçtikten sonra bu kural bir uyarı üretir olmaz.

> [!NOTE]
> Derinlikte bu kural veri akışı yöntem çağrıları arasında çözümler için yapılandırılabilir bir sınır yoktur. Bkz: [Çözümleyicisi yapılandırma](https://github.com/dotnet/roslyn-analyzers/blob/master/docs/Analyzer%20Configuration.md#dataflow-analysis) sınırı nasıl yapılandıracağınızı öğrenmek için `.editorconfig` dosyaları.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

LDAP deyimleri kullanıcı tarafından denetlenen bölümü için aşağıdakilerden birini göz önünde bulundurun:
- Özel olmayan karakterleri güvenli bir listesini sağlar.
- Özel karakter izin verme
- Özel karakterlerden kaçının.

Bkz: [OWASP'ın LDAP ekleme önleme kural sayfası](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/LDAP_Injection_Prevention_Cheat_Sheet.md) daha fazla kılavuzluk için.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Girişi doğrulanması veya güvenli olacak şekilde Atlanan biliyorsanız, bu uyarının gösterilmemesi uygundur.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;
using System.DirectoryServices;

public partial class WebForm : System.Web.UI.Page
{
    protected void Page_Load(object sender, EventArgs e)
    {
        string userName = Request.Params["user"];
        string filter = "(uid=" + userName + ")";  // searching for the user entry 

        // In this example, if we send the * character in the user parameter which will
        // result in the filter variable in the code to be initialized with (uid=*). 
        // The resulting LDAP statement will make the server return any object that 
        // contains a uid attribute.
        DirectorySearcher searcher = new DirectorySearcher(filter);
        SearchResultCollection results = searcher.FindAll();

        // Iterate through each SearchResult in the SearchResultCollection.
        foreach (SearchResult searchResult in results)
        {
            // ...
        }
    }
}
```

```vb
Imports System
Imports System.DirectoryServices

Partial Public Class WebForm
    Inherits System.Web.UI.Page

    Protected Sub Page_Load(send As Object, e As EventArgs)
        Dim userName As String = Me.Request.Params(""user"")
        Dim filter As String = ""(uid="" + userName + "")""    ' searching for the user entry

        ' In this example, if we send the * character in the user parameter which will
        ' result in the filter variable in the code to be initialized with (uid=*). 
        ' The resulting LDAP statement will make the server return any object that 
        ' contains a uid attribute.
        Dim searcher As DirectorySearcher = new DirectorySearcher(filter)
        Dim results As SearchResultCollection = searcher.FindAll()

        ' Iterate through each SearchResult in the SearchResultCollection.
        For Each searchResult As SearchResult in results
            ' ...
        Next searchResult
    End Sub
End Class
```
