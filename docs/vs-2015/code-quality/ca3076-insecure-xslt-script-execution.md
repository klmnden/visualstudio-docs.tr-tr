---
title: 'CA3076: Güvensiz XSLT betiği yürütme | Microsoft Docs'
ms.date: 11/15/2016
ms.technology: vs-ide-code-analysis
ms.topic: reference
ms.assetid: 53cb7a46-c564-488f-bc51-0e210a7853c9
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 0a6b1efa5b5ee84092531a67421d03583afc3578
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65680728"
---
# <a name="ca3076-insecure-xslt-script-execution"></a>CA3076: Güvensiz XSLT Betiği Yürütme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|InsecureXSLTScriptExecution|
|CheckId|CA3076|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Yürütüyorsa [Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT)](https://support.microsoft.com/kb/313997) .NET uygulamalarında endpoınt, işlemci olabilir [güvenilmeyen URI başvuruları çözümlemek](https://msdn.microsoft.com/ba3e4d4f-1ee7-4226-a51a-78a1f1b5bd8a) , ifşa hassas saldırganlar, hizmet reddi ve siteler arası saldırıları için önde gelen bilgileri.

## <a name="rule-description"></a>Kural Tanımı
 [XSLT](https://msdn.microsoft.com/6377ce5f-3c45-42a6-b7a9-ec8da588b60c) XML verileri dönüştürmeye ilişkin bir World Wide Web Consortium (W3C) standart'tır. XSLT genellikle diğer biçimlere HTML, metin uzunluğu, virgülle ayrılmış metin veya farklı bir XML biçimi sabit gibi XML verileri dönüştürmek için stil sayfaları yazmak için kullanılır. Varsayılan olarak yasaklanmış olsa da, projeniz için etkinleştirmeyi tercih edebilirsiniz.

 Tetikleyiciler olduğunda bu kural, değil ifşa eden bir saldırı yüzeyini emin olmak için XslCompiledTransform.<xref:System.Xml.Xsl.XslCompiledTransform.Load%2A> güvenli olmayan birleşim örneğini alır <xref:System.Xml.Xsl.XsltSettings> ve <xref:System.Xml.XmlResolver>, kötü amaçlı betik işlemesini sağlar.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?

- Güvenli olmayan XsltSettings bağımsız değişken XsltSettings ile değiştirin.<xref:System.Xml.Xsl.XsltSettings.Default%2A> veya bir örnekle, belge işlev ve betik yürütme devre dışı bıraktı.

- Değiştirin <xref:System.Xml.XmlResolver> bağımsız değişkeni null ile veya bir <xref:System.Xml.XmlSecureResolver> örneği.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Giriş güvenilir bir kaynaktan olduğu biliniyorsa emin olmadığınız sürece, bir kuraldan bu uyarıyı bastırmayın.

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

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

### <a name="solution"></a>Çözüm

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

### <a name="violation"></a>İhlali

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

### <a name="solution"></a>Çözüm

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
