---
title: SharePoint Proje sistemini genişletme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, extending projects
- SharePoint development in Visual Studio, extending project items
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 51449003457ecd09e7dca7bc579d652c94a592e2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53891118"
---
# <a name="extend-the-sharepoint-project-system"></a>SharePoint Proje sistemini genişletme
  Visual Studio Proje şablonları ve öğe şablonları kullanarak SharePoint çözümleri oluşturabilirsiniz. Bu şablonlar birçok geliştirme senaryosu gereksinimlerini karşılamak, ancak bazı durumlarda, ihtiyaç duyduğunuz işlevsellik burada sağlamayan keşfedebilirsiniz. Bu durumlarda, SharePoint Proje sistemi genişletebilirsiniz.  
  
## <a name="overview-of-the-sharepoint-project-system"></a>SharePoint Proje sistemi genel bakış
 ' In temel bileşeni tabanlı bir SharePoint Proje sistemi *SharePoint Proje öğeleri*. Bir SharePoint proje öğesi bir liste tanımı, Web Bölümü veya içerik türü gibi tek bir SharePoint özelleştirme temsil eder.  
  
 Bir SharePoint projesine bir veya daha fazla SharePoint Proje öğeleri içeren bir Visual Studio projesidir. SharePoint projeleri, proje öğeleri özellikleri ve dağıtım için paketi nasıl gruplandırıldığını tanımlayan ek bileşenler de içerir.  
  
 SharePoint Proje öğeleri ve SharePoint projeleri içeriği hakkında daha fazla bilgi için bkz. [öğe şablonları ve proje şablonları SharePoint Proje öğeleri için oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md).  
  
## <a name="how-to-extend-the-sharepoint-project-system"></a>SharePoint Proje sistemini genişletme
 SharePoint Proje sistemini aşağıdaki yollarla genişletebilirsiniz:  
  
-   Kendi SharePoint proje öğesi türleri tanımlayın ve bunları yeni öğe şablonları veya Visual Studio Proje şablonları ile ilişkilendirin. Örneğin, özel bir eylem veya bir alan oluşturmak için bir SharePoint proje öğesi türü tanımlayabilirsiniz. Daha fazla bilgi için [özel SharePoint proje öğesi türleri tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md).  
  
-   Visual Studio'da yüklü SharePoint proje öğesi türleri genişletir. Örneğin, bir proje öğesine bir kısayol menü öğesi ekleyebilirsiniz **Çözüm Gezgini** ve proje öğesi bir geliştirici menü öğesi seçtiğinde özelleştirin. Daha fazla bilgi için [genişletmek SharePoint Proje öğeleri](../sharepoint/extending-sharepoint-project-items.md).  
  
-   SharePoint projeleri genişletin. Örneğin, öğeleri eklendiğinde veya kaldırıldığında SharePoint projeleri, belirli görevlerin gerçekleştirilmesi için olay işleyicileri ekleyebilirsiniz. Daha fazla bilgi için [genişletmek SharePoint projeleri](../sharepoint/extending-sharepoint-projects.md).  
  
-   SharePoint Proje öğeleri ve SharePoint projeleri paketleme ve dağıtım davranışını genişletin. Örneğin, dağıtmak veya bir proje Ayıkla ya da Visual Studio, belirli dağıtım adımları yürütüldüğünde, ek özel görevleri yerine getirebilirsiniz yürütmek için kendi dağıtım adımları oluşturabilirsiniz. Daha fazla bilgi için [genişletmek SharePoint paketleme ve dağıtım](../sharepoint/extending-sharepoint-packaging-and-deployment.md).  
  
## <a name="common-development-tasks"></a>Genel geliştirme görevleri
 SharePoint Proje sisteminin uzantılarında aşağıdaki yaygın görevleri gerçekleştirebilirsiniz:  
  
-   Özel dize verileri, proje öğeleri ve proje dosyaları birkaç farklı türde Kaydet. Daha fazla bilgi için [SharePoint Proje sisteminin uzantılarında veri kaydetme](../sharepoint/saving-data-in-extensions-of-the-sharepoint-project-system.md).  
  
-   Visual Studio Otomasyon nesne modeli veya tümleştirme nesne modeli, karşılık gelen bir nesne için SharePoint Proje sistemindeki bir nesneyi dönüştürmek veya bunun tersi de geçerlidir. Daha fazla bilgi için [SharePoint Proje sistem türleri ve diğer Visual Studio Proje türleri arasında Dönüştür](../sharepoint/converting-between-sharepoint-project-system-types-and-other-visual-studio-project-types.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Özel SharePoint proje öğesi türlerini tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md)   
 [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)   
 [SharePoint projeleri genişletme](../sharepoint/extending-sharepoint-projects.md)   
 [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)   
 [SharePoint Proje sisteminin uzantılarında veri kaydetme](../sharepoint/saving-data-in-extensions-of-the-sharepoint-project-system.md)   
 [SharePoint Proje sistem türleri ve diğer Visual Studio Proje türleri arasında dönüştürme](../sharepoint/converting-between-sharepoint-project-system-types-and-other-visual-studio-project-types.md)   
 [SharePoint araçlarını Visual Studio'da genişletme](../sharepoint/extending-the-sharepoint-tools-in-visual-studio.md)   
 [SharePoint Araç Uzantıları için Programlama Kavramları ve Özellikler](../sharepoint/programming-concepts-and-features-for-sharepoint-tools-extensions.md)  
