---
title: 'CA3076: Güvensiz XSLT Betiği Yürütme'
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1c6c5df0109a8cff3cefcc308ea27077ef0fbe03
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237075"
---
# <a name="ca3076-insecure-xslt-script-execution"></a>CA3076: Güvensiz XSLT Betiği Yürütme

|||
|-|-|
|TypeName|Insecurexsltscriptexecution|
|CheckId|CA3076|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

.NET uygulamalarında Genişletilebilir Stil sayfaları Dil Dönüşümleri (XSLT) çalıştırıyorsanız, işlemci güvenilir bilgileri saldırganlar 'e açığa çıkarabilecek güvenilmeyen URI başvurularını çözümleyebilir, hizmet reddi ve siteler arası saldırıları. Daha fazla bilgi için bkz. [XSLT güvenlik konuları (. net Guide)](/dotnet/standard/data/xml/xslt-security-considerations).

## <a name="rule-description"></a>Kural açıklaması

**XSLT** , XML verilerini dönüştürmek için bir World WIDE Web KONSORSIYUMU (W3C) standardıdır. XSLT genellikle, XML verilerini HTML, sabit uzunlukta metin, virgülle ayrılmış metin veya farklı bir XML biçimi gibi diğer biçimlere dönüştürmek üzere stil sayfaları yazmak için kullanılır. Varsayılan olarak yasaklanmış olmasına karşın, bunu projeniz için etkinleştirmeyi tercih edebilirsiniz.

Bir saldırı yüzeyi açığa çıkarmadığından emin olmak için, bu kural XslCompiledTransform her seferinde tetiklenir.<xref:System.Xml.Xsl.XslCompiledTransform.Load%2A> , <xref:System.Xml.Xsl.XsltSettings> ve<xref:System.Xml.XmlResolver>kötü amaçlı betik işlemeye izin veren güvenli olmayan birleşim örneklerini alır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

- Güvenli olmayan XsltSettings bağımsız değişkenini XsltSettings ile değiştirin.<xref:System.Xml.Xsl.XsltSettings.Default%2A> ya da belge işlev ve betik yürütmeyi devre dışı bırakmış bir örnekle.

- Bağımsız değişkeni null veya bir <xref:System.Xml.XmlSecureResolver> örnekle değiştirin. <xref:System.Xml.XmlResolver>

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Girişin güvenilen bir kaynaktan geldiğinden emin olmadığınız için, bu uyarıdan bir kuralı engellemez.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation-that-uses-xsltsettingstrustedxslt"></a>XsltSettings. TrustedXslt kullanan ihlal

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

### <a name="solution-that-uses-xsltsettingsdefault"></a>XsltSettings. Default kullanan çözüm

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

### <a name="violationmdashdocument-function-and-script-execution-not-disabled"></a>İhlalin&mdash;belge işlevi ve betiği yürütme devre dışı değil

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

### <a name="solutionmdashdisable-document-function-and-script-execution"></a>Çözüm&mdash;belge işlevini ve betik yürütmeyi devre dışı bırak

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

- [XSLT güvenlik konuları (. NET Kılavuzu)](/dotnet/standard/data/xml/xslt-security-considerations)