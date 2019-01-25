---
title: SharePoint özellikleri oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, features
- features [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 58db8ea5affd295ec21ed9e398053c57345dee79
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54862137"
---
# <a name="create-sharepoint-features"></a>SharePoint özellikleri oluşturma
  Kolay dağıtım için ilgili SharePoint Proje öğeleri gruplandırmak için bir SharePoint özelliğini kullanabilirsiniz. Özellikler oluşturmak, kapsamı ayarla ve diğer özellikleri, SharePoint özellik Tasarımcısı kullanarak bağımlılıkları olarak işaretleyin. Tasarımcı, aynı zamanda her bir özellik açıklayan bir XML dosyası olan bir bildirim oluşturur.  
  
## <a name="add-features-to-the-sharepoint-solution"></a>SharePoint çözümü özellikleri ekleyin
 SharePoint çözümü, Çözüm Gezgini veya paketleme Gezgini'ni kullanarak bir özelliği ekleyebilirsiniz. Bir özellik eklemek için aşağıdaki yöntemlerden birini kullanabilirsiniz.  
  
-   İçinde **Çözüm Gezgini**, kısayol menüsünü açın **özellikleri**ve ardından **Özellik Ekle**.  
  
-   İçinde **paketleme Gezgini**, paket için kısayol menüsünü açın ve ardından **Özellik Ekle**.  
  
## <a name="using-the-feature-designer"></a>Özellik Tasarımcısı'nı kullanarak
 SharePoint çözüm bir veya daha fazla SharePoint Çözüm Gezgini'nde özellik düğümünün altında gruplanmış özellikleri içerebilir. Her özelliğin kendi bölümüne sahiptir **özellik Tasarımcısı** özellik özellikleri özelleştirmek için kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint özelliğini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-feature.md). Özellikleri birbirinden ayırt etmek için başlık, açıklama, sürüm ve kapsamı gibi özellik özellikleri yapılandırabilirsiniz.  
  
### <a name="feature-designer-options"></a>Özellik Tasarımcısı seçenekleri
 Bir özellik oluşturduktan sonra özellik Tasarımcısı özelleştirmek için kullanabilirsiniz.  
  
 Aşağıdaki tabloda, özellik Tasarımcısı'nda görüntülenen özellik özellikleri açıklanmaktadır.  
  
|Özellik|Açıklama|  
|--------------|-----------------|  
|Başlık|İsteğe bağlı. Varsayılan başlığı özelliğinin ayarlandığından *SolutionName* *FeatureName*.|  
|Açıklama|İsteğe bağlı. SharePoint özelliğinin açıklaması.|  
|Kapsam|Gerekli. Bir özellik kullanarak oluşturduysanız **Çözüm Gezgini**, kapsamı, Web için varsayılan olarak ayarlanır.<br /><br /> -Grup: Tüm sunucu grubu için bir özelliği etkinleştirir.<br /><br /> -Site: Bir site koleksiyonundaki tüm web siteleri için bir özelliği etkinleştirir.<br /><br /> -Web: Belirli bir web sitesi için bir özelliği etkinleştirir.<br /><br /> -WebApplication: Bir web uygulamasındaki tüm web siteleri için bir özelliği etkinleştirir.|  
|Çözümdeki öğeler|Özellikle eklenebilir tüm SharePoint öğeleri.|  
|Özellik öğeleri|Özellikle eklenmiş olan SharePoint Proje öğeleri.|  
  
## <a name="add-and-remove-sharepoint-project-items"></a>Ekleme ve SharePoint Proje öğeleri kaldırma
 Dağıtım için bir SharePoint özelliği eklemek istediğiniz hangi SharePoint Proje öğeleri seçebilirsiniz. Kullanım **özellik Tasarımcısı** ekleyin ve özelliklerine öğe kaldırıp özellik bildiriminde görüntüleyin. Daha fazla bilgi için [nasıl yapılır: SharePoint özelliklerine öğe ekleyip](../sharepoint/how-to-add-and-remove-items-to-sharepoint-features.md).  
  
## <a name="add-feature-dependencies"></a>Özellik bağımlılıkları ekleme
 Böylece, özellik etkinleştirilmeden önce SharePoint sunucusu bazı özellikleri etkinleştirir. özellik bildiriminde yapılandırabilirsiniz. SharePoint özelliğinizi işlevi veya verileri diğer özellikleri bağlıdır, örneğin, SharePoint sunucusunun ilk özelliğinizi bağımlı özelliklerinden herhangi birini etkinleştirmek deneyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Özellik bağımlılıkları ekleyip](../sharepoint/how-to-add-and-remove-feature-dependencies.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir SharePoint özelliğini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-feature.md)   
 [Nasıl yapılır: SharePoint özelliklerine öğe ekleyip](../sharepoint/how-to-add-and-remove-items-to-sharepoint-features.md)   
 [Nasıl yapılır: Ekleme ve kaldırma özellik bağımlılıkları](../sharepoint/how-to-add-and-remove-feature-dependencies.md)  
