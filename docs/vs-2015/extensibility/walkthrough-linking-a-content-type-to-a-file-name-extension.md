---
title: 'İzlenecek yol: Bir içerik türü için bir dosya adı uzantısına bağlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new - link content type to file name extension
ms.assetid: 21ee64ce-9afe-4b08-94a0-8389cc4dc67c
caps.latest.revision: 25
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: beae9d0526cb9f2f294f2267a8da52d3ce3d8c08
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68202003"
---
# <a name="walkthrough-linking-a-content-type-to-a-file-name-extension"></a>İzlenecek yol: İçerik Türünü Dosya Adı Uzantısına Bağlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kendi içerik türü tanımlayabilir ve düzenleyici Yönetilen Genişletilebilirlik Çerçevesi (MEF) uzantılarını kullanarak bağlamak için bir dosya adı uzantısı. Bazı durumlarda, dosya adı uzantısı zaten bir dil hizmeti tarafından tanımlandı; Bununla birlikte, MEF ile kullanmak için yine de bunu bir içerik türüyle bağlamanız gerekir.  
  
## <a name="prerequisites"></a>Önkoşullar  
 Visual Studio 2015'ten başlayarak, size Visual Studio SDK İndirme Merkezi'nden yüklemeyin. Visual Studio kurulumunda isteğe bağlı bir özellik olarak eklenmiştir. VS SDK'yi daha sonra yükleyebilirsiniz. Daha fazla bilgi için [Visual Studio SDK'sını yükleme](../extensibility/installing-the-visual-studio-sdk.md).  
  
## <a name="creating-a-mef-project"></a>MEF proje oluşturma  
  
1. Bir C# VSIX projesi oluşturun. (İçinde **yeni proje** iletişim kutusunda **Visual C# / genişletilebilirlik**, ardından **VSIX projesi**.) Çözüm adı `ContentTypeTest`.  
  
2. İçinde **source.extension.vsixmanifest** dosya, Git **varlıklar** sekmesini tıklatıp ayarlamak **türü** alanı **Microsoft.VisualStudio.MefComponent**, **kaynak** alanı **mevcut çözümde bir proje**ve **proje** projesinin adı alanı.  
  
## <a name="defining-the-content-type"></a>İçerik türü tanımlama  
  
1. Bir sınıf dosyası ekleyin ve adlandırın `FileAndContentTypes`.  
  
2. Aşağıdaki derlemelere başvurular ekleyin:  
  
    1. System.ComponentModel.Composition  
  
    2. Microsoft.VisualStudio.Text.Logic  
  
    3. Microsoft.VisualStudio.CoreUtility  
  
3. Aşağıdaki `using` yönergeleri.  
  
    ```csharp  
    using System.ComponentModel.Composition;  
    using Microsoft.VisualStudio.Text.Classification;  
    using Microsoft.VisualStudio.Utilities;  
  
    ```  
  
4. Tanımları içeren bir statik sınıf bildirin.  
  
    ```csharp  
    internal static class FileAndContentTypeDefinitions  
    {. . .}  
    ```  
  
5. Bu sınıf, dışarı aktarma bir <xref:Microsoft.VisualStudio.Utilities.ContentTypeDefinition> "gizlenmiş" adlı ve temel tanımına "metin" olarak bildirin.  
  
    ```csharp  
    internal static class FileAndContentTypeDefinitions  
    {  
        [Export]  
        [Name("hid")]  
        [BaseDefinition("text")]  
        internal static ContentTypeDefinition hidingContentTypeDefinition;  
    }  
    ```  
  
## <a name="linking-a-file-name-extension-to-a-content-type"></a>Bir içerik türü için bir dosya adı uzantısına bağlama  
  
- Bu içerik türü için bir dosya adı uzantısı eşlemek için dışarı aktarma bir <xref:Microsoft.VisualStudio.Utilities.FileExtensionToContentTypeDefinition> ".hid" uzantısı olan ve "gizlenmiş" içerik türü.  
  
    ```csharp  
    internal static class FileAndContentTypeDefinitions  
    {  
         [Export]  
         [Name("hid")]  
         [BaseDefinition("text")]  
        internal static ContentTypeDefinition hidingContentTypeDefinition;  
  
         [Export]  
         [FileExtension(".hid")]  
         [ContentType("hid")]  
        internal static FileExtensionToContentTypeDefinition hiddenFileExtensionDefinition;  
    }  
    ```  
  
## <a name="adding-the-content-type-to-an-editor-export"></a>İçerik türü Düzenleyicisi vermeyi ekleme  
  
1. Düzenleyici uzantısı oluşturun. Örneğin, açıklanan kenar boşluğu glif uzantısı kullanabilirsiniz [izlenecek yol: Bir dış boşluk karakteri oluşturma](../extensibility/walkthrough-creating-a-margin-glyph.md).  
  
2. Bu yordamda tanımlanan sınıfı ekleyin.  
  
3. Extension sınıfının dışarı aktardığınızda ekleme bir <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> "kendisine HID" türü.  
  
    ```csharp  
    [Export]  
    [ContentType("hid")]  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Dil Hizmeti ve Düzenleyici Uzantı Noktaları](../extensibility/language-service-and-editor-extension-points.md)
