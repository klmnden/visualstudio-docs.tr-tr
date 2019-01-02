---
title: 'İzlenecek yol: Metin görünümünü özelleştirme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], new - customizing the view
ms.assetid: 32d32ac8-22ff-4de7-af69-bd46ec4ad9bf
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8748ccade8e610c66d9c4142312c2c5dfed1ddf9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53917325"
---
# <a name="walkthrough-customize-the-text-view"></a>İzlenecek yol: Metin görünümünü özelleştirme
Bir metin görünümünü kendi Düzenleyicisi biçim eşlemesi şu özelliklerde değiştirerek özelleştirebilirsiniz:  
  
-   Belirteç kenar boşluğu  
  
-   Ekleme düzeltme işareti  
  
-   Giriş işaretini üzerine yaz  
  
-   Seçili metni  
  
-   Etkin olmayan seçili metin (odağını kaybetmiş diğer bir deyişle, seçilen metin)  
  
-   Görünür boşluk  
  
## <a name="prerequisites"></a>Önkoşullar  
 Visual Studio 2015'ten başlayarak, size Visual Studio SDK İndirme Merkezi'nden yüklemeyin. Visual Studio kurulumunda isteğe bağlı bir özellik eklemiştir. VS SDK'yi daha sonra yükleyebilirsiniz. Daha fazla bilgi için [Visual Studio SDK'yı yükleme](../extensibility/installing-the-visual-studio-sdk.md).  
  
## <a name="create-a-mef-project"></a>MEF proje oluşturma  
  
1.  Bir C# VSIX projesi oluşturun. (İçinde **yeni proje** iletişim kutusunda **Visual C# / genişletilebilirlik**, ardından **VSIX projesi**.) Çözüm adı `ViewPropertyTest`.  
  
2.  Bir düzenleyici sınıflandırıcı öğe şablonu, projeye ekleyin. Daha fazla bilgi için [bir düzenleyici öğesi şablonuyla uzantı oluşturma](../extensibility/creating-an-extension-with-an-editor-item-template.md).  
  
3.  Varolan sınıf dosyaları silin.  
  
## <a name="define-the-content-type"></a>İçerik türünü tanımlayın  
  
1. Bir sınıf dosyası ekleyin ve adlandırın `ViewPropertyModifier`.  
  
2. Aşağıdaki `using` yönergeleri:  
  
    [!code-csharp[VSSDKViewPropertyTest#1](../extensibility/codesnippet/CSharp/walkthrough-customizing-the-text-view_1.cs)]
    [!code-vb[VSSDKViewPropertyTest#1](../extensibility/codesnippet/VisualBasic/walkthrough-customizing-the-text-view_1.vb)]  
  
3. Adlı bir sınıf bildirme `TestViewCreationListener` öğesinden devralan <xref:Microsoft.VisualStudio.Text.Editor.IWpfTextViewCreationListener>. Bu sınıf aşağıdaki özniteliklerle dışarı aktarın:  
  
   - <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> Bu dinleyici uygulandığı içerik türünü belirtmek için.  
  
   - <xref:Microsoft.VisualStudio.Text.Editor.TextViewRoleAttribute> Bu dinleyici rolünü belirtmek için.  
  
     [!code-csharp[VSSDKViewPropertyTest#2](../extensibility/codesnippet/CSharp/walkthrough-customizing-the-text-view_2.cs)]
     [!code-vb[VSSDKViewPropertyTest#2](../extensibility/codesnippet/VisualBasic/walkthrough-customizing-the-text-view_2.vb)]  
  
4. Bu sınıf, içeri aktarma <xref:Microsoft.VisualStudio.Text.Classification.IEditorFormatMapService>.  
  
    [!code-csharp[VSSDKViewPropertyTest#3](../extensibility/codesnippet/CSharp/walkthrough-customizing-the-text-view_3.cs)]
    [!code-vb[VSSDKViewPropertyTest#3](../extensibility/codesnippet/VisualBasic/walkthrough-customizing-the-text-view_3.vb)]  
  
## <a name="change-the-view-properties"></a>Görünüm özelliklerini değiştir  
  
1.  Ayarlanan <xref:Microsoft.VisualStudio.Text.Editor.IWpfTextViewCreationListener.TextViewCreated%2A> yöntemi böylece görünüm açıldığında Görünüm Özellikleri değiştirilir. Değişiklik yapmak için öncelikle bulma <xref:System.Windows.ResourceDictionary> bulmak istediğiniz görünümü en/boy karşılık gelir. Ardından, kaynak sözlüğünde uygun özelliğini değiştirin ve özelliklerini ayarlayın. Toplu işlem çağrıları <xref:Microsoft.VisualStudio.Text.Classification.IEditorFormatMap.SetProperties%2A> yöntemi çağırarak <xref:Microsoft.VisualStudio.Text.Classification.IEditorFormatMap.BeginBatchUpdate%2A> özellikleri ayarlanmadan önce yöntemi ve ardından <xref:Microsoft.VisualStudio.Text.Classification.IEditorFormatMap.EndBatchUpdate%2A> özellikleri ayarladıktan sonra.  
  
     [!code-csharp[VSSDKViewPropertyTest#4](../extensibility/codesnippet/CSharp/walkthrough-customizing-the-text-view_4.cs)]
     [!code-vb[VSSDKViewPropertyTest#4](../extensibility/codesnippet/VisualBasic/walkthrough-customizing-the-text-view_4.vb)]  
  
## <a name="build-and-test-the-code"></a>Kod oluşturup test  
  
1.  Çözümü oluşturun.  
  
     Bu projede hata ayıklayıcıda çalıştırdığınızda, Visual Studio'nun ikinci bir örneğini başlatılır.  
  
2.  Bir metin dosyası oluşturun ve bir metin yazın.  
  
    -   Ekleme giriş işaretini Eflatun olmalıdır ve üzerine yazma giriş işaretini Turkuaz olmalıdır.  
  
    -   Belirteç kenar boşluğu ('metin görünümünü sol) açık olması gereken yeşil.  
  
3.  Yazdığınız metni seçin. Seçili metnin rengini açık olmalıdır pembe.  
  
4.  Metin seçili durumdayken metni penceresi dışında herhangi bir yere tıklayın. Seçili metnin rengini koyu pembe olmalıdır.  
  
5.  Üzerinde görünür boşluk bırakın. (Üzerinde **Düzenle** menüsünde **Gelişmiş** ve ardından **beyaz boşluğu görüntüle**). Bazı sekmeler metin girin. Sekmeleri temsil eden kırmızı ok görüntülenmesi gerekir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Dil hizmeti ve düzenleyici uzantı noktaları](../extensibility/language-service-and-editor-extension-points.md)