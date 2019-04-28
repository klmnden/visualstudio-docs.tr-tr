---
title: 'Nasıl yapılır: Bir SharePoint Proje öğe uzantısına özellik ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- project items [SharePoint development in Visual Studio], extending
- SharePoint project items, extending
- SharePoint development in Visual Studio, extending project items
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 20a7abaa8c132b3cd1679ab95ed8154b8ca86502
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967246"
---
# <a name="how-to-add-a-property-to-a-sharepoint-project-item-extension"></a>Nasıl yapılır: Bir SharePoint Proje öğe uzantısına özellik ekleme
  Visual Studio'da yüklü herhangi bir SharePoint proje öğesi için bir özellik eklemek için bir proje öğesi uzantısı'nı kullanabilirsiniz. Özellik görünür **özellikleri** proje öğesi seçildiğinde penceresi **Çözüm Gezgini**.

 Aşağıdaki adımlar, bir proje öğesi uzantısı zaten oluşturduğunuzu varsayalım. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md).

### <a name="to-add-a-property-to-a-project-item-extension"></a>Bir proje öğe uzantısına özellik eklemek için

1. Eklediğiniz bir proje öğe türüne özellik temsil eden genel özelliğine sahip bir sınıfı tanımlar. Bir proje öğesi türü için birden çok özellik eklemek istiyorsanız, tüm özelliklerin aynı sınıftaki veya farklı sınıflardaki tanımlayabilirsiniz.

2. İçinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension.Initialize%2A> yöntemi, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension> uygulama, tanıtıcısını <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemPropertiesRequested> olayı *Projectıtemtype* parametresi.

3. İçin olay işleyicisinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemPropertiesRequested> olay özellikleri sınıfı bir örneğini ekleme <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemPropertiesRequestedEventArgs.PropertySources%2A> olay bağımsız değişkenleri parametre koleksiyonu.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde adlı bir özellik eklemek gösterilmiştir **örnek özellik** olay alıcısı proje öğesi için.

 [!code-csharp[SPExtensibility.ProjectItemExtension.MenuAndProperty#8](../sharepoint/codesnippet/CSharp/projectitemmenuandproperty/extension/projectitemextensionproperty.cs#8)]
 [!code-vb[SPExtensibility.ProjectItemExtension.MenuAndProperty#8](../sharepoint/codesnippet/VisualBasic/projectitemmenuandproperty/extension/projectitemextensionproperty.vb#8)]

### <a name="understand-the-code"></a>Kodu anlama
 ' In aynı örneğine emin olmak için `CustomProperties` sınıfı, her zaman kullanılır <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemPropertiesRequested> bir olay oluşursa, kod örneği için özellikleri nesnesi ekler <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> özelliği proje öğesi ilk zaman bu olayı oluşur. Bu olay tekrar oluştuğunda bu nesne kodu alır. Kullanma hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> veri proje öğeleriyle ilişkilendirmek için özelliğine bakın [SharePoint ile özel verileri ilişkilendirme araçları uzantıları](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md).

 Özellik değeri değişiklikleri kalıcı hale getirmek için **ayarlamak** için erişimci `ExampleProperty` yeni değere kaydeder <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> özelliği <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem> özelliğin ilişkili olduğu nesne. Kullanma hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> proje öğeleri ile verileri kalıcı hale getirmek için özelliğine bakın [SharePoint Proje sisteminin uzantılarında veri kaydetme](../sharepoint/saving-data-in-extensions-of-the-sharepoint-project-system.md).

### <a name="specify-the-behavior-of-custom-properties"></a>Özel özellikler davranışını belirtin
 Özel bir özellik görünür ve davranır nasıl tanımlayabileceğiniz **özellikleri** öznitelikleri uygulayarak penceresi <xref:System.ComponentModel> özellik tanımı için ad alanı. Aşağıdaki öznitelikler pek çok senaryoda kullanışlıdır:

- <xref:System.ComponentModel.DisplayNameAttribute>: Görüntülenen özellik adını belirtir **özellikleri** penceresi.

- <xref:System.ComponentModel.DescriptionAttribute>: Görüntülenen açıklama dizesi tabanında belirtir **özellikleri** özelliği seçildiğinde penceresi.

- <xref:System.ComponentModel.DefaultValueAttribute>: Özelliğin varsayılan değerini belirtir.

- <xref:System.ComponentModel.TypeConverterAttribute>: Görüntülenen dizeyi arasında özel bir dönüştürme belirtir **özellikleri** penceresi ve dize olmayan özellik değeri.

- <xref:System.ComponentModel.EditorAttribute>: Özelliği değiştirmek için özel bir düzenleyici belirtir.

## <a name="compile-the-code"></a>Kod derleme
 Bu örnekler, aşağıdaki derlemelere başvurular içeren bir sınıf kitaplığı projesi gerektirir:

- Microsoft.VisualStudio.SharePoint

- System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)
- [Nasıl yapılır: Bir SharePoint Proje öğe uzantısına bir kısayol menü öğesi ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-a-sharepoint-project-item-extension.md)
- [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)
- [İzlenecek yol: Bir SharePoint proje öğesi türünü genişletme](../sharepoint/walkthrough-extending-a-sharepoint-project-item-type.md)
