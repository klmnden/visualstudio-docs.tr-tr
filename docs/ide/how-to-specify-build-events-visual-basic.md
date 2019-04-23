---
title: 'Nasıl yapılır: Derleme olayları belirtme (Visual Basic)'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- pre-build events
- events [Visual Studio], builds
- post-build events
- build events [Visual Studio]
- builds [Visual Studio], events
ms.assetid: 40dc83bf-a7c5-4a14-816a-fa0980b6e4c3
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e9dc571576346aa246452cdebf0a147468d6dfea
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60100930"
---
# <a name="how-to-specify-build-events-visual-basic"></a>Nasıl yapılır: Derleme olayları belirtme (Visual Basic)

Visual Basic'te derleme olayları, betikleri, makroları veya başka eylemler derleme işleminin bir parçası olarak çalıştırmak için kullanılabilir. Derleme öncesi olayları önce derleme oluşur; derleme sonrası olayları derleme sonra oluşur.

Derleme olayları belirtilir **Build Events** iletişim kutusu, kullanılabilir **derleme** sayfasının **Proje Tasarımcısı**.

> [!NOTE]
> Visual Basic Express derleme olayları girişi desteklemez. Bu, yalnızca Visual Studio ürününün tam desteklenir.

## <a name="how-to-specify-pre-build-and-post-build-events"></a>Derleme öncesi ve sonrası derleme olayları belirtme

### <a name="to-specify-a-build-event"></a>Derleme olayı belirtmek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **derleme** sekmesi.

3. Tıklayın **Build Events** açmak için düğmeyi **Build Events** iletişim kutusu.

4. Derleme öncesi veya derleme sonrası eylemleriniz için komut satırı bağımsız değişkenleri girin ve ardından **Tamam**.

    > [!NOTE]
    > Ekleme bir `call` deyiminden önce çalışan tüm derleme sonrası komutlar *.bat* dosyaları. Örneğin, `call C:\MyFile.bat` veya `call C:\MyFile.bat call C:\MyFile2.bat`.

    > [!NOTE]
    > Derleme öncesi veya derleme sonrası olay başarıyla tamamlanmazsa, başarılı bir eylem gösteren bir ile dışında sıfır (0), çıkış kodu olay eyleminizi sağlayarak derleme sonlandırabilirsiniz.

## <a name="example-how-to-change-manifest-information-using-a-post-build-event"></a>Örnek: Derleme sonrası olay kullanarak bildirim bilgilerini değiştirme

Aşağıdaki yordamda, uygulamanın en düşük işletim sistemi sürümünü ayarlama işlemi gösterilmektedir kullanarak bildirim bir *.exe* adlı bir derleme sonrası olay komut ( *. exe.manifest* proje dosyasında Dizin). En düşük işletim sistemi sürümünü 4.10.0.0 gibi dört kısımlı bir sayıdır. Bunu yapmak için komut değişir `<dependentOS>` bildiriminin:

```xml
<dependentOS>
   <osVersionInfo>
      <os majorVersion="4" minorVersion="10" buildNumber="0" servicePackMajor="0" />
   </osVersionInfo>
</dependentOS>
```

### <a name="to-create-an-exe-command-to-change-the-application-manifest"></a>Uygulama bildirimini değiştirmek için bir .exe komutu oluşturmak için

1. Komut için bir konsol uygulaması oluşturun. **Dosya** menüsünde **Yeni**'ye ve ardından **Proje**'ye tıklayın.

2. İçinde **yeni proje** iletişim kutusundaki **Visual Basic** düğümünü **Windows** ardından **konsol uygulaması** şablonu. Projeyi adlandırın `ChangeOSVersionVB`.

3. İçinde *Module1.vb*, diğer aşağıdaki satırı ekleyin `Imports` deyimini dosyanın üst:

   ```vb
   Imports System.Xml
   ```

4. Aşağıdaki kodu ekleyin `Sub Main`:

   ```vb
   Sub Main()
      Dim applicationManifestPath As String
      applicationManifestPath = My.Application.CommandLineArgs(0)
      Console.WriteLine("Application Manifest Path: " & applicationManifestPath.ToString)

      'Get version name
      Dim osVersion As Version
      If My.Application.CommandLineArgs.Count >= 2 Then
         osVersion = New Version(My.Application.CommandLineArgs(1).ToString)
      Else
         Throw New ArgumentException("OS Version not specified.")
      End If
      Console.WriteLine("Desired OS Version: " & osVersion.ToString())

      Dim document As XmlDocument
      Dim namespaceManager As XmlNamespaceManager
      namespaceManager = New XmlNamespaceManager(New NameTable())
      With namespaceManager
         .AddNamespace("asmv1", "urn:schemas-microsoft-com:asm.v1")
         .AddNamespace("asmv2", "urn:schemas-microsoft-com:asm.v2")
      End With

      document = New XmlDocument()
      document.Load(applicationManifestPath)

      Dim baseXPath As String
      baseXPath = "/asmv1:assembly/asmv2:dependency/asmv2:dependentOS/asmv2:osVersionInfo/asmv2:os"

      'Change minimum required OS Version.
      Dim node As XmlNode
      node = document.SelectSingleNode(baseXPath, namespaceManager)
      node.Attributes("majorVersion").Value = osVersion.Major.ToString()
      node.Attributes("minorVersion").Value = osVersion.Minor.ToString()
      node.Attributes("buildNumber").Value = osVersion.Build.ToString()
      node.Attributes("servicePackMajor").Value = osVersion.Revision.ToString()

      document.Save(applicationManifestPath)
   End Sub
   ```

   Komut iki bağımsız değişkeni alır. İlk bağımsız değişkeni uygulama bildirimini yoludur (diğer bir deyişle, hangi yapı işlemi oluşturur, bildirim genellikle klasör  *\<ProjectName > .publish*). İkinci bağımsız değişkeni yeni bir işletim sistemi sürümüdür.

5. Üzerinde **derleme** menüsünde tıklatın **Çözümü Derle**.

6. Kopyalama *.exe* gibi bir dizine dosya *C:\TEMP\ChangeOSVersionVB.exe*.

   Ardından, uygulama bildirimini değiştirmek için bu komutu bir derleme sonrası olay çağırın.

### <a name="to-invoke-a-post-build-event-to-change-the-application-manifest"></a>Uygulama bildirimini değiştirmek için bir derleme sonrası olay çağırmak için

1. Yayımlanacak proje için bir Windows uygulaması oluşturun. **Dosya** menüsünde **Yeni**'ye ve ardından **Proje**'ye tıklayın.

2. İçinde **yeni proje** iletişim kutusundaki **Visual Basic** düğümünü **Windows Masaüstü** ardından **Windows Forms uygulaması** şablonu. Projeyi adlandırın `VBWinApp`.
3. Seçilen proje **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

4. İçinde **Proje Tasarımcısı**Git **Yayımla** sayfasında ve ayarlayın **konumu yayımlama** için *C:\TEMP*.

5. Tıklayarak projeyi yayımlama **Şimdi Yayımla**.

     Bildirim dosyası oluşturulmuş ve koymak *C:\TEMP\VBWinApp_1_0_0_0\VBWinApp.exe.manifest*. Bildirimi görüntülemek için dosyaya sağ tıklayın ve **birlikte Aç**, ardından **program bir listeden seçim**ve ardından **not defteri**.

     Arama için dosyasında `<osVersionInfo>` öğesi. Örneğin, sürüm olabilir:

    ```xml
    <os majorVersion="4" minorVersion="10" buildNumber="0" servicePackMajor="0" />
    ```

6. İçinde **Proje Tasarımcısı**Git **derleme** sekmesine **Build Events** açmak için düğmeyi **Build Events** iletişim kutusu.

7. İçinde **derleme sonrası olay komut satırı** kutusunda, aşağıdaki komutu girin:

     `C:\TEMP\ChangeOSVersionVB.exe "$(TargetPath).manifest" 5.1.2600.0`

     Proje oluşturduğunuzda, bu komut uygulama bildiriminde minimum işletim sistemi sürümü için 5.1.2600.0 değiştirin.

     `$(TargetPath)` Makrosu oluşturulan yürütülebilir dosyanın tam yolunu ifade eder. Bu nedenle, *$(TargetPath) .manifest* belirtin, oluşturulan uygulama bildirimi *bin* dizin. Yayımlama bu bildirimi daha önce belirlediğiniz yayımlama konumuna kopyalar.

8. Projeyi yeniden yayımlayın. Git **Yayımla** sayfasında ve tıklayın **Şimdi Yayımla**.

     Bildirim yeniden görüntüleyin. Bildirimi görüntülemek için dosyayı yayımlama dizinine sağ tıklatıp gidin **birlikte Aç** ardından **program bir listeden seçim**ve ardından **not defteri**.

     Sürüm şöyle olmalıdır:

    ```xml
    <os majorVersion="5" minorVersion="1" buildNumber="2600" servicePackMajor="0" />
    ```

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/compile-page-project-designer-visual-basic.md)
- [Yayımlama Sayfası, Proje Tasarımcısı](../ide/reference/publish-page-project-designer.md)
- [Derleme öncesi olay/derleme sonrası olay komut satırı iletişim kutusu](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)
- [Nasıl yapılır: Derleme olayları belirtme (C#)](../ide/how-to-specify-build-events-csharp.md)