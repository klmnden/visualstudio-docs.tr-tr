---
title: 'Nasıl yapılır: Varlıklar arasında ilişkilendirme oluşturma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- AssociationGroupTool
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], create an assocation
- Business Data Connectivity service [SharePoint development in Visual Studio], associations between entities
- BDC [SharePoint development in Visual Studio], associations between entities
- Business Data Connectivity service [SharePoint development in Visual Studio], create an assocation
- Business Data Connectivity service [SharePoint development in Visual Studio], associate external content types
- Business Data Connectivity service [SharePoint development in Visual Studio], relate entities
- BDC [SharePoint development in Visual Studio], relate entities
- BDC [SharePoint development in Visual Studio], associate external content types
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1870d8965947c1ee8adce5b7839c732d2d590daa
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867981"
---
# <a name="how-to-create-an-association-between-entities"></a>Nasıl yapılır: Varlıklar arasında ilişkilendirme oluşturma
  İlişkilendirmeleri oluşturarak iş verileri bağlantısı (BDC) modelinizdeki varlıklar arasında ilişkiler tanımlayabilirsiniz. Visual Studio model tüketicilerinin her ilişkilendirmesi hakkında bilgi sağlayan yöntemler oluşturur. Bu yöntemler, SharePoint web bölümleri, liste veya bir kullanıcı arabirimi (UI) veri ilişkileri görüntülemek için özel uygulamaları tarafından kullanılabilecek.  
  
 İki tür ilişkilerini BDC tasarımcısında oluşturabilirsiniz: yabancı anahtar tabanlı ilişkilendirmeleri ve yabancı anahtarsız ilişkileri. Daha fazla bilgi için [varlıklar arasında ilişkilendirme oluşturma](../sharepoint/creating-an-association-between-entities.md).  
  
### <a name="to-create-an-association-between-entities"></a>Varlıklar arasında ilişkilendirme oluşturma  
  
1.  Üzerinde **BusinessDataConnectivity** sekmesinde **araç kutusu**, seçin **ilişkilendirme** öğesi.  
  
2.  İVB Tasarımcısı kaynak varlık seçin ve ardından hedef varlık seçin.  
  
     **İlişkilendirme Düzenleyicisi** görünür.  
  
3.  Bir yabancı anahtar tabanlı ilişki oluşturmak isteyip istemediğinizi seçin **yabancı anahtar ilişkilendirmesi olduğundan** onay kutusu.  
  
    1.  İçinde **kaynak kimliği** sütununun **tanımlayıcı eşlemesi** tablo, tanımlayıcı yanında görünen eşleşen her tür tanımlayıcısını seçin **alan** sütun.  
  
         Örneğin, **kaynak kimliği** sütunundaki `ContactID` yanındaki `ReadList.salesOrderList.SalesOrderList.SalesOrder.ContactID` tür tanımlayıcısı ve `ReadItem.salesOrder.SalesOrder.ContactID` tür tanımlayıcısı.  
  
4.  Bir yabancı anahtarsız ilişkilendirmesini oluşturmak istiyorsanız, Temizle **yabancı anahtar ilişkilendirmesi olduğundan** onay kutusu.  
  
5.  Seçin **Tamam** düğmesi.  
  
6.  İVB Tasarımcısı üzerinde kaynak varlık ve hedef varlık ilişkiyi temsil eden bir çizgi görünür.  
  
     Visual Studio bir hizmet sınıfı, hedef varlık ve hizmet sınıfı, kaynak varlık ilişkisi Gezgin yöntemi ekler. İlişkilendirme Gezinti yöntemleri hakkında daha fazla bilgi için bkz. [desteklenen işlemler](http://go.microsoft.com/fwlink/?LinkId=169286).  
  
7.  Kaynak varlık ilişkisi Gezgin yönteminde bir hedef varlık koleksiyonunu döndüren kod ekleyin.  
  
8.  Hedef varlık ilişkisi Gezgin yönteminde, ilişkili kaynak varlık döndüren kod ekleyin.  
  
     İlişkilendirme Gezgin yöntemleri örnekleri için bkz. [varlıklar arasında ilişkilendirme oluşturma](../sharepoint/creating-an-association-between-entities.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Varlıklar arasında ilişkilendirme oluşturma](../sharepoint/creating-an-association-between-entities.md)   
 [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)   
 [Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)   
 [Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-specific-finder-method.md)   
 [Nasıl yapılır: Bir yaratıcı metodu ekleme](../sharepoint/how-to-add-a-creator-method.md)   
 [Nasıl yapılır: Silici metodu ekleme](../sharepoint/how-to-add-a-deleter-method.md)   
 [Nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md)   
 [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)   
 [Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)   
 [Nasıl yapılır: Metot örneği tanımlama](../sharepoint/how-to-define-a-method-instance.md)   
 [Nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)   
 [İzlenecek yol: İş verileri kullanarak SharePoint'te dış liste oluşturma](../sharepoint/walkthrough-creating-an-external-list-in-sharepoint-by-using-business-data.md)  
