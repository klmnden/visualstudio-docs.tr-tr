---
title: Program kodundaki UML modelini okuma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- UML API, reading models
ms.assetid: 0f63105e-6079-498a-94f1-318c0f5f9621
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 37539ee6c031d88b9db279cc61214ac5e3077e76
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63387675"
---
# <a name="read-a-uml-model-in-program-code"></a>Program kodundaki UML modelini okuma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir UML model ve diyagramlarını UML API kullanarak yükleyebilirsiniz.  
  
## <a name="Reading"></a> Program kodundaki modeli okuma  
 Göstermeden modelin içeriğine erişmek için bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] penceresinde kullanım `ModelingProject.LoadReadOnly()`.  
  
 Örneğin:  
  
```  
using Microsoft.VisualStudio.Uml.Classes;   
               // for IElement  
using Microsoft.VisualStudio.ArchitectureTools.Extensibility;   
               // for ModelingProject  
using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml;  
               // for IModelStore  
...   
string projectPath = @"C:\MyProjectFolder\MyProject.modelproj";  
using (IModelingProjectReader projectReader =  
           ModelingProject.LoadReadOnly(projectPath))  
{  
   IModelStore store = projectReader.Store;  
   foreach (IClass umlClass in store.AllInstances<IClass>())  
   {   
       ...  
   }  
}  
```  
  
 Bir diyagramdaki şekilleri okumak istiyorsanız, proje ve sonra da diyagramı okumalısınız.  
  
 Örneğin:  
  
```  
using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Presentation;   
                             // for IDiagram  
...  
foreach (string diagramFile in projectReader. DiagramFileNames)  
{   
  IDiagram diagram = projectReader.LoadDiagram(diagramFile);  
  foreach (IShape<IElement> shape   
         in diagram.GetChildShapes<IElement>())  
  { ... }  
}  
```  
  
## <a name="alternative-methods"></a>Alternatif yöntemler  
 Birçok uygulama için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Modelbus modellere ve daha yüksek sağlamlık ve esneklik bu konuda açıklanan yöntemlerle içerdiği öğeler, sağlar. Bu da aynı ya da farklı modellerde rastgele öğeler arasında bağlantı yapmak için standart bir yöntemini sağlar. Daha fazla bilgi için [tümleştirme UML modellerini diğer modeller ve araçlarla birlikte](../modeling/integrate-uml-models-with-other-models-and-tools.md).  
  
 Kullanıcı arabirimi kullanarak modelleri ve diyagramları da açabilirsiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] API. Daha fazla bilgi için [Visual Studio API kullanarak bir UML modeli açma](../modeling/open-a-uml-model-by-using-the-visual-studio-api.md).  
  
## <a name="Standalone"></a> Tek başına uygulamalar  
 Önceki bölümdeki örnek Visual Studio uzantılarında çalışır. Tek başına bir uygulamadaki modeli okumak mümkündür, ancak bazı başvurular eklemeniz gerekir, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] proje.  
  
> [!NOTE]
> Tek başına bir uygulamadaki modeli okumak nasıl ayrıntılarını ürün sürümleri gelecekte değiştirme olasılığı düşüktür. Geçerli sürümünde erişilebilir olan bazı özellikler gelecek sürümlerde kullanılabilir olmayabilir.  
  
#### <a name="to-add-references-to-read-a-model-in-a-stand-alone-application"></a>Tek başına bir uygulamadaki modeli okumak için başvurular eklemek için.  
  
1. Çözüm Gezgini'nde, uygulama oluşturma ve ardından projeyi sağ **özellikleri**. Özellik Düzenleyicisi'ndeki içinde **uygulama** sekmesinde, belirleyin **hedef Framework'ü** gerekli .NET Framework sürümü için.  
  
2. Ekleme [!INCLUDE[TLA2#tla_net](../includes/tla2sharptla-net-md.md)] UML modelleri, genellikle erişmek için gereksinim duyduğunuz başvuruları:  
  
   - Microsoft.VisualStudio.Uml.Interfaces.dll  
  
   - Microsoft.VisualStudio.ArchitectureTools.Extensibility.dll  
  
3. Önceki bölümlerde listelenmiş başvurulara ek olarak, aşağıdaki proje başvurularından ekleme **\Program Visual Studio [sürüm] \Common7\IDE\PrivateAssemblies**:  
  
   - Microsoft.VisualStudio.Uml.dll  
  
   - Microsoft.VisualStudio.TeamArchitect.ModelStore.Dsl.dll  
  
     Uygulamanızdaki diyagramları okumak istiyorsanız, bu başvurular da gerekebilir:  
  
   - Microsoft.VisualStudio.TeamArchitect.ActivityDesigner.Dsl.dll  
  
   - Microsoft.VisualStudio.TeamArchitect.ComponentDesigner.Dsl.dll  
  
   - Microsoft.VisualStudio.TeamArchitect.LogicalClassDesigner.Dsl.dll  
  
   - Microsoft.VisualStudio.TeamArchitect.SequenceDesigner.Dsl.dll  
  
   - Microsoft.VisualStudio.TeamArchitect.UseCase.Dsl.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UML API ile programlama](../modeling/programming-with-the-uml-api.md)   
 [UML modellerini ve diyagramları genişletme](../modeling/extend-uml-models-and-diagrams.md)
