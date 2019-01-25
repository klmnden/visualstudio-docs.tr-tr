---
title: 'Nasıl yapılır: Özel SharePoint Proje öğe türüne özellik ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint project items, defining your own types
- project items [SharePoint development in Visual Studio], defining your own types
- SharePoint development in Visual Studio, defining new project item types
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ca3bfbf6ecd773f0a7c3147a44eb02a5c260764b
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54872800"
---
# <a name="how-to-add-a-property-to-a-custom-sharepoint-project-item-type"></a>Nasıl yapılır: Özel bir SharePoint Proje öğe türüne özellik ekleme
  Özel bir SharePoint proje öğesi türü tanımladığınızda, proje öğesi için bir özelliği ekleyebilirsiniz. Özellik görünür **özellikleri** proje öğesi seçildiğinde penceresi **Çözüm Gezgini**.  
  
 Aşağıdaki adımlarda kendi SharePoint proje öğesi türü zaten tanımlamış olduğunuz varsayılır. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi türü tanımlayacağınızı](../sharepoint/how-to-define-a-sharepoint-project-item-type.md).  
  
### <a name="to-add-a-property-to-a-definition-of-a-project-item-type"></a>Bir özellik bir proje öğesi türü tanımına eklemek için  
  
1.  Özel proje öğe türüne eklemekte olduğunuz özelliğini temsil eden genel özelliğine sahip bir sınıfı tanımlar. Bir özel proje öğesi türü için birden çok özellik eklemek istiyorsanız, tüm özelliklerin aynı sınıftaki veya farklı sınıflardaki tanımlayabilirsiniz.  
  
2.  İçinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider.InitializeType%2A> yöntemi, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider> uygulama, tanıtıcısını <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemPropertiesRequested> olayı *projectItemTypeDefinition* parametresi.  
  
3.  İçin olay işleyicisinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemPropertiesRequested> olay, özel özellikler sınıfı bir örneğini ekleme <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemPropertiesRequestedEventArgs.PropertySources%2A> olay bağımsız değişkenleri parametre koleksiyonu.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde adlı bir özellik eklemek gösterilmiştir **örnek özellik** özel bir proje öğesi türü.  
  
 [!code-vb[SPExtensibility.ProjectItemExtension.MenuAndProperty#11](../sharepoint/codesnippet/VisualBasic/projectitemmenuandproperty/extension/projectitemtypeproperty.vb#11)]
 [!code-csharp[SPExtensibility.ProjectItemExtension.MenuAndProperty#11](../sharepoint/codesnippet/CSharp/projectitemmenuandproperty/extension/projectitemtypeproperty.cs#11)]  
  
### <a name="understand-the-code"></a>Kodu anlama  
 ' In aynı örneğine emin olmak için `CustomProperties` sınıfı, her zaman kullanılır <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemPropertiesRequested> bir olay oluşursa, kod örneği için özellikleri nesnesi kaydeder <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> özelliği proje öğesi ilk zaman bu olayı oluşur. Bu olay tekrar oluştuğunda bu nesne kodu alır. Kullanma hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> proje öğeleri ile verileri kaydetmek için özelliğine bakın [SharePoint ile özel verileri ilişkilendirme araçları uzantıları](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md).  
  
 Özellik değeri değişiklikleri kalıcı hale getirmek için **ayarlamak** için erişimci `ExampleProperty` yeni değere kaydeder <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> özelliği <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem> özelliğin ilişkili olduğu nesne. Kullanma hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> proje öğeleri ile verileri kalıcı hale getirmek için özelliğine bakın [SharePoint Proje sisteminin uzantılarında veri kaydetme](../sharepoint/saving-data-in-extensions-of-the-sharepoint-project-system.md).  
  
### <a name="specify-the-behavior-of-custom-properties"></a>Özel özellikler davranışını belirtin  
 Özel bir özellik görünür ve davranır nasıl tanımlayabileceğiniz **özellikleri** öznitelikleri uygulayarak penceresi <xref:System.ComponentModel> özellik tanımı için ad alanı. Aşağıdaki öznitelikler pek çok senaryoda kullanışlıdır:  
  
-   <xref:System.ComponentModel.DisplayNameAttribute>: Görüntülenen özellik adını belirtir **özellikleri** penceresi.  
  
-   <xref:System.ComponentModel.DescriptionAttribute>: Görüntülenen açıklama dizesi tabanında belirtir **özellikleri** özelliği seçildiğinde penceresi.  
  
-   <xref:System.ComponentModel.DefaultValueAttribute>: Özelliğin varsayılan değerini belirtir.  
  
-   <xref:System.ComponentModel.TypeConverterAttribute>: Görüntülenen dizeyi arasında özel bir dönüştürme belirtir **özellikleri** penceresi ve dize olmayan özellik değeri.  
  
-   <xref:System.ComponentModel.EditorAttribute>: Özelliği değiştirmek için özel bir düzenleyici belirtir.  
  
## <a name="compile-the-code"></a>Kod derleme  
 Bu kod örneği, aşağıdaki derlemelere başvurular içeren bir sınıf kitaplığı projesi gerektirir:  
  
-   Microsoft.VisualStudio.SharePoint  
  
-   System.ComponentModel.Composition  
  
## <a name="deploy-the-project-item"></a>Proje öğesi dağıtma  
 Diğer geliştiricilerin, proje öğesini kullanmak için bir proje şablonu veya bir proje öğesi şablon oluşturun. Daha fazla bilgi için [öğe şablonları ve proje şablonları SharePoint Proje öğeleri için oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md).  
  
 Proje öğesini dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme, şablon ve proje öğesi ile dağıtmak istediğiniz diğer tüm dosyalar. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)   
 [Nasıl yapılır: Özel bir SharePoint Proje öğe türüne bir kısayol menü öğesi ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-a-custom-sharepoint-project-item-type.md)   
 [Özel SharePoint proje öğesi türleri tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md)  
