---
title: 'Nasıl Yapılır: Modele bir varlık ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- EntityTool
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], entity
- Business Data Connectivity service [SharePoint development in Visual Studio], adding an entity
- Business Data Connectivity service [SharePoint development in Visual Studio], entity
- BDC [SharePoint development in Visual Studio], adding an entity
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 347728ac4f096359f06ca7823adfcd1b25ff527a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53964040"
---
# <a name="how-to-add-an-entity-to-a-model"></a>Nasıl Yapılır: Modele bir varlık ekleme
  Bir varlık oluşturmak için Visual Studio'dan bir varlık denetimi ekleme **araç kutusu** İş Verileri Bağlantısı (BDC) tasarımcıya.  
  
### <a name="to-add-an-entity-to-the-model"></a>Modele bir varlık eklemek için  
  
1.  Bir BDC projesi oluşturmak veya mevcut bir BDC projesi açın. Daha fazla bilgi için [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).  
  
2.  İçinde **araç kutusu**, gelen **BusinessDataCatalog** grubunda, ekleme bir **varlık** tasarımcıya denetim.  
  
     Yeni varlık tasarımcısında görüntülenir. Visual Studio ekler bir `<Entity>` projenizdeki bir BDC modeli dosyası XML öğesi. Bir varlık öğe öznitelikleri hakkında daha fazla bilgi için bkz. [varlık](http://go.microsoft.com/fwlink/?LinkId=169296).  
  
3.  Tasarımcıda varlık için kısayol menüsünü açın, **Ekle**ve ardından **tanımlayıcı**.  
  
     Yeni bir tanımlayıcı varlık üzerinde görünür.  
  
    > [!NOTE]  
    >  Varlık ve tanımlayıcı adını değiştirebilirsiniz **özellikleri** penceresi.  
  
4.  Varlık alanlarını bir sınıfta tanımlayın. Projeye yeni bir sınıf ekleyin veya Object Relational Designer (O/R Tasarımcısı) gibi diğer araçları kullanarak oluşturduğunuz var olan bir sınıfı kullanın. Aşağıdaki örnek, kişi adlı bir varlık sınıfı gösterir.  
  
     [!code-csharp[SP_BDC_Entity_Data_Class#1](../sharepoint/codesnippet/CSharp/sp_bdc_entity_data_class/bdcmodel1/contact.cs#1)]
     [!code-vb[SP_BDC_Entity_Data_Class#1](../sharepoint/codesnippet/VisualBasic/sp_bdc_entity_data_class/bdcmodel1/contact.vb#1)]  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir yaratıcı metodu ekleme](../sharepoint/how-to-add-a-creator-method.md)   
 [Nasıl yapılır: Silici metodu ekleme](../sharepoint/how-to-add-a-deleter-method.md)   
 [Nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md)   
 [Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)   
 [Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-specific-finder-method.md)  
