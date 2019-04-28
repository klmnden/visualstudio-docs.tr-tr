---
title: 'CA3076: Güvensiz XSLT Betiği Yürütme'
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5f98b022aef49a4d98ad4864793aa55732f8de6c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62541096"
---
# <a name="ca3076-insecure-xslt-script-execution"></a>CA3076: Güvensiz XSLT Betiği Yürütme

|||
|-|-|
|TypeName|InsecureXSLTScriptExecution|
|CheckId|CA3076|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) .NET uygulamalarında endpoınt çalışırsa, saldırganların hizmet reddi ve siteler arası lideri, hassas bilgileri ifşa güvenilmeyen URI başvuruları işlemci çözebilir saldırıları. Daha fazla bilgi için [XSLT güvenlik Considerations(.NET Guide)](/dotnet/standard/data/xml/xslt-security-considerations).

## <a name="rule-description"></a>Kural açıklaması

**XSLT** XML verileri dönüştürmeye ilişkin bir World Wide Web Consortium (W3C) standart'tır. XSLT genellikle diğer biçimlere HTML, sabit uzunluklu metin, virgülle ayrılmış metin ya da farklı bir XML biçimi gibi XML verileri dönüştürmek için stil sayfaları yazmak için kullanılır. Varsayılan olarak yasaklanmış olsa da, projeniz için etkinleştirmeyi tercih edebilirsiniz.

Tetikleyiciler olduğunda bu kural, değil ifşa eden bir saldırı yüzeyini emin olmak için XslCompiledTransform.<xref:System.Xml.Xsl.XslCompiledTransform.Load%2A> güvenli olmayan birleşim örneğini alır <xref:System.Xml.Xsl.XsltSettings> ve <xref:System.Xml.XmlResolver>, kötü amaçlı betik işlemesini sağlar.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Güvenli olmayan XsltSettings bağımsız değişken XsltSettings ile değiştirin.<xref:System.Xml.Xsl.XsltSettings.Default%2A> veya bir örnekle, belge işlev ve betik yürütme devre dışı bıraktı.

- Değiştirin <xref:System.Xml.XmlResolver> bağımsız değişkeni null ile veya bir <xref:System.Xml.XmlSecureResolver> örneği.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Giriş güvenilir bir kaynaktan olduğu biliniyorsa emin olmadığınız sürece, bir kuraldan bu uyarıyı bastırmayın.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation-that-uses-xsltsettingstrustedxslt"></a>XsltSettings.TrustedXslt kullanan ihlali

```csharp
using System.Xml;
using System.Xml.Xsl;

namespace TestNamespace
{
    class TestClass
    {
         void TestMethod()
        {
             XslCompiledTransform xslCompiledTransform = new XslCompiledTransform();
             var settings = XsltSettings.TrustedXslt;
             var resolver = new XmlUrlResolver();
             xslCompiledTransform.Load("testStylesheet", settings, resolver); // warn
        }
    }
}
```

### <a name="solution-that-uses-xsltsettingsdefault"></a>XsltSettings.Default kullanan bir çözüm

```csharp
using System.Xml;
using System.Xml.Xsl;

namespace TestNamespace
{
    class TestClass
    {
        void TestMethod()
        {
            XslCompiledTransform xslCompiledTransform = new XslCompiledTransform();
            var settings = XsltSettings.Default;
            var resolver = new XmlUrlResolver();
            xslCompiledTransform.Load("testStylesheet", settings, resolver);
        }
    }
}
```

### <a name="violationmdashdocument-function-and-script-execution-not-disabled"></a>İhlali&mdash;belge işlev ve betik yürütme devre dışı

```csharp
using System.Xml;
using System.Xml.Xsl;

namespace TestNamespace
{
    class TestClass
    {
        private static void TestMethod(XsltSettings settings)
        {
            try
            {
                XslCompiledTransform xslCompiledTransform = new XslCompiledTransform();
                var resolver = new XmlUrlResolver();
                xslCompiledTransform.Load("testStylesheet", settings, resolver); // warn
            }
            catch { throw; }
            finally { }
        }
    }
}
```

### <a name="solutionmdashdisable-document-function-and-script-execution"></a>Çözüm&mdash;belge işlev ve betik yürütme devre dışı bırak

```csharp
using System.Xml;
using System.Xml.Xsl;

namespace TestNamespace
{
    class TestClass
    {
        private static void TestMethod(XsltSettings settings)
        {
            try
            {
                XslCompiledTransform xslCompiledTransform = new XslCompiledTransform();
                settings.EnableDocumentFunction = false;
                settings.EnableScript = false;
                var resolver = new XmlUrlResolver();
                xslCompiledTransform.Load("testStylesheet", settings, resolver);
            }
            catch { throw; }
            finally { }
        }
    }
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [XSLT güvenlik konuları (.NET Kılavuzu)](/dotnet/standard/data/xml/xslt-security-considerations)