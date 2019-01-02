---
title: 'Nasıl Yapılır: XSLT hata ayıklamayı Başlat'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: 170d4d3d0c952e13a5fefb74b23536f50be1e9a6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53925137"
---
# <a name="how-to-start-debugging-xslt"></a>Nasıl Yapılır: XSLT hata ayıklamayı Başlat

XSLT hata ayıklayıcı bir XSLT stil sayfası veya XSLT uygulamanın hatalarını ayıklamak için kullanılabilir. Hata ayıklama sırasında içine Adımlama, üzerinden Adımlama veya kodların dışına Adımlama aynı anda bir satır kod yürütebilir. XSLT hata ayıklayıcının bir Visual Studio olduğu gibi aynı hata ayıklayıcıları kodu Adımlama işlevselliği kullanmak için komutlar bulunmaktadır. XSLT hata ayıklayıcı, hata ayıklamayı başlattıktan sonra giriş belge ve XSLT çıkış göstermek için windows açılır.

## <a name="xml-editor"></a>XML Düzenleyicisi

XML Düzenleyicisi'nden hata ayıklayıcıyı başlatabilirsiniz. Bu, stil sayfası tasarladığınız gibi hatalarını ayıklamanızı sağlar.

### <a name="to-start-debugging-from-a-style-sheet"></a>Bir stil sayfası hata ayıklamayı başlatmak için

1. Stil sayfası XML düzenleyicisinde açın.

1. Seçin **hata ayıklama XSL** gelen **XML** menüsü.

### <a name="to-start-debugging-from-an-xml-input-document"></a>Giriş XML belgesinden hata ayıklamayı başlatmak için

1. XML belgesi bir XML düzenleyicisinde açın.

1. Seçin **hata ayıklama XSL** gelen **XML** menüsü.

## <a name="xslt-from-other-languages"></a>Diğer dillerdeki XSLT

Ayrıca, bir uygulamanın hatalarını ayıklama sırasında XSLT geçebilirsiniz. F11 bastığınızda bir <xref:System.Xml.Xsl.XslCompiledTransform.Transform%2A?displayProperty=fullName> çağrı, hata ayıklayıcı adım XSLT kodu.

> [!NOTE]
> XSLT içine Adımlama <xref:System.Xml.Xsl.XslTransform> sınıfı desteklenmiyor. <xref:System.Xml.Xsl.XslCompiledTransform> Hata ayıklama sırasında XSLT Adımlama destekleyen XSLT işlemci bir sınıftır.

### <a name="to-start-debugging-an-xslt-application"></a>XSLT uygulama hata ayıklama başlatılamıyor

1. Örneği oluşturulurken <xref:System.Xml.Xsl.XslCompiledTransform> nesne, ayarlama `enableDebug` parametresi `true` kodunuzda.

     Bu, hata ayıklama bilgilerini derlenen kod oluşturma için XSLT işlemci bildirir.

1. XSLT kodda ilerleyebilmeniz için F11 tuşuna basın.

     XSLT stil sayfası, yeni bir belge penceresi yüklenir ve XSLT hata ayıklayıcı başlatılır.

     Alternatif olarak, stil sayfası için bir kesme noktası ekleyin ve uygulamanızı çalıştırın.

### <a name="example"></a>Örnek

Bir C# XSLT programının bir örnek verilmiştir. Bu XSLT hata ayıklamayı nasıl etkinleştireceğinizi gösterir.

```csharp
using System;
using System.IO;
using System.Xml;
using System.Xml.Xsl;

namespace ConsoleApplication
{
  class Program
  {
    private const string sourceFile = @"c:\data\xsl_files\books.xml";
    private const string stylesheet = @"c:\data\xsl_files\belowAvg.xsl";
    private const string outputFile = @"c:\data\xsl_files\output.xml";

    static void Main(string[] args)
    {
      // Enable XSLT debugging.
      XslCompiledTransform xslt = new XslCompiledTransform(true);

      // Compile the style sheet.
      xslt.Load(stylesheet)

      // Execute the XSLT transform.
      FileStream outputStream = new FileStream(outputFile, FileMode.Append);
      xslt.Transform(sourceFile, null, outputStream);
    }
  }
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)   