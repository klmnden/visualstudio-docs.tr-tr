---
title: XSLT kod hatalarını ayıklamanın yolları
ms.date: 03/05/2019
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- multiple
ms.openlocfilehash: 67ea95e3c52daed03acfe451f353edc039e1fecb
ms.sourcegitcommit: 9753c7544cec852ca5efd0834e0956d9e53a5734
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67043540"
---
# <a name="debugging-xslt"></a>XSLT Hatalarını Ayıklama

Visual Studio XSLT kodunda hata ayıklaması yapabilirsiniz. XSLT hata ayıklayıcı, kesme noktaları ayarlama, XSLT yürütme durumlarını görüntüleme destekler ve benzeri. XSLT hata ayıklayıcısı, XSLT stil sayfalarını veya XSLT uygulamalarda hata ayıklamak için kullanılabilir.

İçine Adımlama, üzerinden Adımlama veya kodların dışına Adımlama bir defada bir satır kod yürütebilir. XSLT hata ayıklayıcısı kodu Adımlama işlevselliğini kullanmak için aynı olan bir Visual Studio için hata ayıklayıcıları komutlardır.

XSLT hata ayıklayıcı, hata ayıklamayı başlattıktan sonra giriş belge ve XSLT çıkış göstermek için windows açılır.

> [!NOTE]
> XSLT hata ayıklayıcısı yalnızca Visual Studio Professional ve Enterprise sürümlerinde kullanılabilir.

## <a name="debug-from-the-xml-editor"></a>XML Düzenleyicisi'nden hata ayıklama

Bir stil sayfası veya giriş XML dosyası düzenleyicide açık olduğunda, hata ayıklayıcıyı başlatabilirsiniz. Bu stil sayfası tasarladığınız gibi hatalarını ayıklamanıza olanak tanır.

1. Stil sayfası veya XML dosyasını Visual Studio'da açın.

1. Seçin **XSLT hata ayıklamayı Başlat** gelen **XML** menü veya basın **Alt**+**F5**.

## <a name="debug-from-an-app-that-uses-xslt"></a>XSLT kullanan bir uygulamayı hata ayıklama

XSLT, bir uygulamanın hatalarını ayıklama sırasında geçebilirsiniz. Bastığınızda **F11** üzerinde bir <xref:System.Xml.Xsl.XslCompiledTransform.Transform%2A?displayProperty=fullName> çağrı, hata ayıklayıcı adım XSLT kodu.

> [!NOTE]
> XSLT içine Adımlama <xref:System.Xml.Xsl.XslTransform> sınıfı desteklenmiyor. <xref:System.Xml.Xsl.XslCompiledTransform> Hata ayıklama sırasında XSLT Adımlama destekleyen XSLT işlemci bir sınıftır.

### <a name="to-start-debugging-an-xslt-application"></a>XSLT uygulama hata ayıklama başlatılamıyor

1. Örneği oluşturulurken <xref:System.Xml.Xsl.XslCompiledTransform> nesne, ayarlama `enableDebug` parametresi `true` kodunuzda. Bu, hata ayıklama bilgilerini derlenen kod oluşturma için XSLT işlemci bildirir.

1. Tuşuna **F11** XSLT kod içine Adımlama için.

   XSLT stil sayfası, yeni bir belge penceresi yüklenir ve XSLT hata ayıklayıcıyı başlatır.

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
    private const string stylesheet = @"c:\data\xsl_files\below-average.xsl";
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

## <a name="xslt-profiler"></a>XSLT profil oluşturucusu

[XSLT Profil Oluşturucusu](../xml-tools/xslt-profiler.md) ölçmesine, değerlendirme ve performans ile ilgili sorunları XSLT kodda ayrıntılı XSLT performans raporlar oluşturarak hedef geliştiricilerinin bir araçtır. Daha fazla bilgi için [XSLT Profil Oluşturucusu](../xml-tools/xslt-profiler.md).

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md)
- [Visual Studio hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
- [Hata ayıklama temelleri: Kesme noktaları](../debugger/using-breakpoints.md)
