---
title: 'Nasıl yapılır: XSLT hata ayıklamayı Başlat | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 8358335a-fcb0-45e0-a37e-45b43e49ec0a
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 9811963b6130c3b0c144feee928de915a4bd9ba9
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697017"
---
# <a name="how-to-start-debugging-xslt"></a>Nasıl yapılır: XSLT hata ayıklamayı Başlat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XSLT hata ayıklayıcı bir XSLT stil sayfası veya XSLT uygulamanın hatalarını ayıklamak için kullanılabilir. Hata ayıklama sırasında içine Adımlama, üzerinden Adımlama veya kodların dışına Adımlama aynı anda bir satır kod yürütebilir. XSLT hata ayıklayıcının bir Visual Studio olduğu gibi aynı hata ayıklayıcıları kodu Adımlama işlevselliği kullanmak için komutlar bulunmaktadır. XSLT hata ayıklayıcı, hata ayıklamayı başlattıktan sonra giriş belge ve XSLT çıkış göstermek için windows açılır.  
  
## <a name="xml-editor"></a>XML Düzenleyicisi  
 XML Düzenleyicisi'nden hata ayıklayıcıyı başlatabilirsiniz. Bu, stil sayfası tasarladığınız gibi hatalarını ayıklamanızı sağlar.  
  
#### <a name="to-start-debugging-from-a-style-sheet"></a>Bir stil sayfası hata ayıklamayı başlatmak için  
  
1. Stil sayfası XML düzenleyicisinde açın.  
  
2. Seçin **hata ayıklama XSL** gelen **XML** menüsü.  
  
#### <a name="to-start-debugging-from-an-xml-input-document"></a>Giriş XML belgesinden hata ayıklamayı başlatmak için  
  
1. XML belgesi bir XML düzenleyicisinde açın.  
  
2. Seçin **hata ayıklama XSL** gelen **XML** menüsü.  
  
## <a name="xslt-from-other-languages"></a>Diğer dillerdeki XSLT  
 Ayrıca, bir uygulamanın hatalarını ayıklama sırasında XSLT geçebilirsiniz. F11 bastığınızda bir <xref:System.Xml.Xsl.XslCompiledTransform.Transform%2A?displayProperty=fullName> çağrı, hata ayıklayıcı adım XSLT kodu.  
  
> [!NOTE]
> XSLT içine Adımlama <xref:System.Xml.Xsl.XslTransform> sınıfı desteklenmiyor. <xref:System.Xml.Xsl.XslCompiledTransform> Hata ayıklama sırasında XSLT Adımlama destekleyen XSLT işlemci bir sınıftır.  
  
#### <a name="to-start-debugging-an-xslt-application"></a>XSLT uygulama hata ayıklama başlatılamıyor  
  
1. Örneği oluşturulurken <xref:System.Xml.Xsl.XslCompiledTransform> nesne, ayarlama `enableDebug` parametresi `true` kodunuzda.  
  
     Bu, hata ayıklama bilgilerini derlenen kod oluşturma için XSLT işlemci bildirir.  
  
2. XSLT kodda ilerleyebilmeniz için F11 tuşuna basın.  
  
     XSLT stil sayfası, yeni bir belge penceresi yüklenir ve XSLT hata ayıklayıcı başlatılır.  
  
     Alternatif olarak, stil sayfası için bir kesme noktası ekleyin ve uygulamanızı çalıştırın.  
  
### <a name="example"></a>Örnek  
 Bir C# XSLT programının bir örnek verilmiştir. Bu XSLT hata ayıklamayı nasıl etkinleştireceğinizi gösterir.  
  
```  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md)   
 [Kod Adımlamaya genel bakış](https://msdn.microsoft.com/8791dac9-64d1-4bb9-b59e-8d59af1833f9)
