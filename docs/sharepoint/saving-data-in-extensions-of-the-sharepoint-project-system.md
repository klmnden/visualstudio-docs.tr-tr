---
title: SharePoint Proje sisteminin uzantılarında veri kaydetme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
helpviewer_keywords:
- SharePoint project items, saving string data
- project items [SharePoint development in Visual Studio], saving string data
- projects [SharePoint development in Visual Studio], saving string data
- SharePoint projects, saving string data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 373f031795238c599d15eec92f1730289662c3a0
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54866548"
---
# <a name="save-data-in-extensions-of-the-sharepoint-project-system"></a>SharePoint Proje sisteminin uzantılarında veri kaydetme
  SharePoint Proje sistemi genişlettiğinizde, bir SharePoint projesine kapatıldıktan sonra devam eden bir dize verileri kaydedebilirsiniz. Veriler genellikle belirli bir proje öğesi veya proje ile ilişkilidir.  
  
 Kalıcı hale getirmek gerekmez veri varsa uygulayan SharePoint araçları nesne modelinde herhangi bir nesneye veri ekleyebilirsiniz <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject> arabirimi. Daha fazla bilgi için [SharePoint ile özel verileri ilişkilendirme araçları uzantıları](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md).  
  
## <a name="save-data-that-is-associated-with-a-project-item"></a>Proje öğesi ile ilişkili olan verileri kaydedin
 Bir proje öğesine eklediğiniz bir özelliğin değerini gibi belirli bir SharePoint proje öğesi ile ilişkili olan verilere sahip olduğunuz verilere kaydedebilirsiniz *.spdata* proje öğesinin dosya. Bunu yapmak için <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> özelliği bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem> nesne. Bu özelliğe eklemek veri kaydedildiğinde **ExtensionData** öğesinde *.spdata* proje öğesinin dosya. Daha fazla bilgi için [ExtensionData öğesi](../sharepoint/extensiondata-element.md).  
  
 Aşağıdaki kod örneğinde nasıl kullanılacağını gösterir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem.ExtensionData%2A> değeri özel bir SharePoint proje öğesi türünde tanımlanan bir dize özelliğini kaydetmeyi özelliği. Daha büyük bir örneğin bağlamında bu örnek için bkz [nasıl yapılır: Özel bir SharePoint Proje öğe türüne özellik ekleme](../sharepoint/how-to-add-a-property-to-a-custom-sharepoint-project-item-type.md).  
  
 [!code-vb[SPExtensibility.ProjectItemExtension.MenuAndProperty#14](../sharepoint/codesnippet/VisualBasic/projectitemmenuandproperty/extension/projectitemtypeproperty.vb#14)]
 [!code-csharp[SPExtensibility.ProjectItemExtension.MenuAndProperty#14](../sharepoint/codesnippet/CSharp/projectitemmenuandproperty/extension/projectitemtypeproperty.cs#14)]  
  
## <a name="save-data-that-is-associated-with-a-project"></a>Bir proje ile ilişkili olan verileri kaydedin
 SharePoint projelerine ekleme bir özelliğin değerini gibi proje düzeyinde verileri varsa, verileri proje dosyasına kaydedebilirsiniz ( *.csproj* dosya veya *.vbproj* dosyası) veya proje kullanıcı seçenekleri dosya ( *. csproj.user* dosya veya *. vbproj.user* dosyası). Verileri kaydetmek için seçtiğiniz dosya, kullanılacak verilerini nasıl istediğinize bağlıdır:  
  
-   Verileri, verilerin SharePoint projesini tüm geliştiriciler için kullanılabilir olmasını istiyorsanız, proje dosyasına kaydedin. Bu dosyadaki verileri Projeyi kullanıma diğer geliştiriciler için kullanılabilir, bu nedenle bu dosyayı her zaman kaynak denetim veritabanları için iade edildi.  
  
-   Veriler SharePoint Proje Visual Studio'da Aç olan geçerli Geliştirici kullanılabilir olmasını istiyorsanız, veri proje kullanıcı seçeneği dosyasına kaydedin. Bu dosyadaki verileri Projeyi kullanıma diğer geliştiriciler için kullanılabilir olmadığından bu dosya genellikle kaynak denetim veritabanları için iade edildiğinde değil.  
  
### <a name="save-data-to-the-project-file"></a>Proje dosyasına veri kaydetme
 Proje dosyasına veri kaydetmek için dönüştürme bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> nesnesini bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage> nesnesi ve ardından <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetPropertyValue%2A> yöntemi. Aşağıdaki kod örneği, bir proje özelliği değeri proje dosyasına kaydetmek için bu yöntemi kullanmak nasıl gösterir. Bu örnekte bağlamı daha büyük bir örnek görmek için bkz [nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md).  
  
 [!code-vb[SpExt_SPCustomPrjProperty#3](../sharepoint/codesnippet/VisualBasic/customspproperty/customproperty.vb#3)]
 [!code-csharp[SpExt_SPCustomPrjProperty#3](../sharepoint/codesnippet/CSharp/customspproperty/customproperty.cs#3)]  
  
 Dönüştürme hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> nesneler Visual Studio Otomasyon nesne modeli veya tümleştirme nesne modeli, diğer türlere bakın [SharePoint Proje sistem türleri ve diğerVisualStudioProjetürleriarasındadönüştürme](../sharepoint/converting-between-sharepoint-project-system-types-and-other-visual-studio-project-types.md).  
  
### <a name="save-data-to-the-project-user-option-file"></a>Proje kullanıcı seçeneği dosyasına verileri kaydetme
 Proje kullanıcı seçeneği dosyasına verileri kaydetmek için <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject.ProjectUserFileData%2A> özelliği bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> nesne. Aşağıdaki kod örneği bu özellik proje özelliği değeri proje kullanıcı seçeneği dosyayı kaydetmek için nasıl kullanılacağını gösterir. Bu örnekte bağlamı daha büyük bir örnek görmek için bkz [nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md).  
  
 [!code-vb[SpExt_SPCustomPrjProperty#2](../sharepoint/codesnippet/VisualBasic/customspproperty/customproperty.vb#2)]
 [!code-csharp[SpExt_SPCustomPrjProperty#2](../sharepoint/codesnippet/CSharp/customspproperty/customproperty.cs#2)]  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint Proje sistemini genişletme](../sharepoint/extending-the-sharepoint-project-system.md)   
 [SharePoint araç uzantıları ile özel verileri ilişkilendirme](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md)   
 [SharePoint Proje sistem türleri ve diğer Visual Studio Proje türleri arasında dönüştürme](../sharepoint/converting-between-sharepoint-project-system-types-and-other-visual-studio-project-types.md)  
