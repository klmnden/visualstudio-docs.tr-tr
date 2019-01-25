---
title: 'Nasıl yapılır: ASPX işaretlemesini yerelleştirme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- localizing XML [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, localizing
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: df6e4be288e957708ba7339383d8e80e82f27e40
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54870275"
---
# <a name="how-to-localize-aspx-markup"></a>Nasıl yapılır: ASPX işaretlemesini yerelleştirme
  [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] (.aspx) sayfası genellikle sabit kodlanmış dize değerleri kullanır. Bu dizelerini yerelleştirmek için yerelleştirilmiş kaynaklara başvuran deyimleri ile değiştirin.  
  
## <a name="localize-aspx-markup"></a>ASPX işaretlemesini yerelleştirme  
  
#### <a name="to-localize-aspx-markup"></a>ASPX biçimlendirmesini yerelleştirmek için  
  
1.  Ayrı kaynak dosyaları ekleyin: biri varsayılan dili ve her bir yerelleştirme dili.  
  
     Yalnızca işaretleme ve kod değil yerelleştiriyorsanız, Genel kaynaklar dosyası proje öğesi ekleyin. Kodu ve biçimlendirmeyi yerelleştirme, bir kaynak dosyası proje öğesi ekleyin.  
  
    1.  Genel bir kaynak dosyası eklemek için **Çözüm Gezgini**, bir SharePoint proje öğesi için kısayol menüsünü açın ve ardından **Ekle** > **yeni öğe**. SharePoint altında **2010** düğümünü seçin **Genel kaynaklar dosyası** şablonu.  
  
    2.  Bir .resources dosyası eklemek için **Çözüm Gezgini**, bir SharePoint proje öğesi için kısayol menüsünü açın ve ardından **Ekle** > **yeni öğe**. Ya da altında **Visual Basic** veya **Visual C#**  düğümünü seçin **kaynak dosyası** şablonu.  
  
    > [!NOTE]  
    >  Dağıtım türü özelliğini etkinleştirmek için bir SharePoint proje öğesi için kaynak dosyaları eklediğinizden emin olun. Bu yordamda daha sonra bu özellik gereklidir. Çözümünüze bir SharePoint proje öğesi yoksa, boş bir SharePoint projesine ekleyin ve varsayılan kaldırmak *Elements.xml* dosya.  
  
2.  Varsayılan kaynak dosyasına protokolün kendi tercih ettiğiniz bir ad verin bir *.resx* MyAppResources.resx gibi bir uzantı. Her bir yerelleştirilmiş kaynak dosyası için aynı temel adı kullanın, ancak kültür ekleme [!INCLUDE[TLA2#tla_id](../sharepoint/includes/tla2sharptla-id-md.md)]. Örneğin, kaynak adı Almanca yerelleştirilmiş *MyAppResources.de-DE.resx*.  
  
3.  Değiştirin **dağıtım türü** özelliği için her kaynak dosyasının **AppGlobalResource** bunları sunucunun App_GlobalResources klasörüne dağıtılacak neden olacak.  
  
4.  ASPX biçimlendirmeye ek olarak kodu yerelleştirmek için kaynakları kullanıyorsanız bırakın **derleme eylemi** özelliği her bir dosyanın **gömülü kaynak**. İsteğe bağlı olarak kaynak dosyalarını yalnızca biçimlendirmeyi yerelleştirmek için kullanıyorsanız, özellik değeri dosyaları değiştirebilirsiniz **içerik**. Daha fazla bilgi için [yerelleştirmek SharePoint çözümleri](../sharepoint/localizing-sharepoint-solutions.md).  
  
5.  Her kaynak dosyasını açın ve her dosyada aynı dize kimliklerini kullanarak yerelleştirilmiş dizeleri ekleyin.  
  
6.  İçinde [!INCLUDE[TLA2#tla_xml](../sharepoint/includes/tla2sharptla-xml-md.md)] ASPX sayfa veya denetimi için biçimlendirme sabit kodlanmış dizeleri aşağıdaki biçimi kullanın değerleriyle değiştirin:  
  
    ```aspx-csharp  
    <%$Resources:Resource File Name, String ID%>  
    ```  
  
     Örneğin, bir uygulama sayfası üzerinde bir etiket denetimi için metni yerelleştirmek için değiştirirsiniz:  
  
    ```aspx-csharp  
    <asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">  
    <asp:Label ID="lbl" runat="server" Text="Label text"></asp:Label>  
    </asp:Content>  
    ```  
  
     to  
  
    ```aspx-csharp  
    <asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">  
    <asp:Label ID="lbl" runat="server" Text="<%$Resources:MyAppResources,String1%>"></asp:Label>  
    </asp:Content>  
    ```  
  
7.  Seçin **F5** anahtarı oluşturun ve uygulamayı çalıştırın.  
  
8.  SharePoint'te, varsayılan görüntüleme dilini değiştirin.  
  
     Yerelleştirilmiş dizeleri uygulamada görüntülenir. Yerelleştirilmiş kaynakları görüntülemek için SharePoint server kaynak dosyanın kültürüyle eşleşen bir dil paketi yüklü olmalıdır.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint Çözümlerini Yerelleştirme](../sharepoint/localizing-sharepoint-solutions.md)   
 [Nasıl yapılır: Bir özelliği yerelleştirme](../sharepoint/how-to-localize-a-feature.md)   
 [Nasıl yapılır: Kaynak dosyası ekleme](../sharepoint/how-to-add-a-resource-file.md)   
 [Nasıl yapılır: Kod yerelleştirme](../sharepoint/how-to-localize-code.md)  
