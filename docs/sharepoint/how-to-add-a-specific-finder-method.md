---
title: 'Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], Specific Finder
- BDC [SharePoint development in Visual Studio], return an entity
- BDC [SharePoint development in Visual Studio], get an entity
- Business Data Connectivity service [SharePoint development in Visual Studio], return an entity
- BDC [SharePoint development in Visual Studio], Specific Finder
- Business Data Connectivity service [SharePoint development in Visual Studio], get an entity
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 93819bea0db3011ed8241389f59e0550d8a3ff84
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54868920"
---
# <a name="how-to-add-a-specific-finder-method"></a>Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme
  Tek varlık örneğini oluşturarak döndürebilir bir *belirli Bulucu* yöntemi. Bir kullanıcı, bir iş verileri web bölümü veya dış listedeki bir varlık seçtiğinde belirli Bulucu metodunu İş Verileri Bağlantısı (BDC) hizmeti yürütür. Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
### <a name="to-create-a-specific-finder-method"></a>Belirli bir Bulucu yöntemi oluşturmak için
  
1. Üzerinde **İVB Tasarımcısı**, varlık seçin.  
  
    Bir varlık ekleme hakkında daha fazla bilgi için **İVB Tasarımcısı** Visual Studio'da görmek [nasıl yapılır: Modele bir varlık ekleme](../sharepoint/how-to-add-an-entity-to-a-model.md).  
  
2. Menü çubuğunda, **görünümü** > **diğer Windows**, **BDC yöntem ayrıntıları**.  
  
    **BDC yöntem ayrıntıları** penceresi açılır. Bu pencere hakkında daha fazla bilgi için bkz. [BDC modeli Tasarım araçları genel bakış](../sharepoint/bdc-model-design-tools-overview.md).  
  
3. İçinde **bir yöntem ekleyin** listesinde **belirli Bulucu metodu Oluştur**.  
  
    Visual Studio modele aşağıdaki öğeleri ekler. Bu öğelerin görünür **BDC yöntem ayrıntıları** penceresi.  
  
   - Bir yöntem.  
  
   - Yöntemi giriş parametresi.  
  
   - Yöntemin bir dönüş parametresi.  
  
   - Her parametre için bir tür tanımlayıcı.  
  
   - Yöntemi için yöntem örneği.  
  
     Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).  
  
4. Visual Studio'yu açın **özellikleri** penceresi.  
  
5. Dönüş parametrenin tür tanımlayıcısını bir varlık türü tanımlayıcısı yapılandırın. Bir varlık türü tanımlayıcısı oluşturma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md).  
  
   > [!NOTE]  
   >  Varlığa bir Bulucu yöntemi eklediyseniz, bu adımı gerçekleştirmeniz gerekmez. Visual Studio Bulucu yönteminde tanımlanan tür tanımlayıcısını kullanır.  
  
   > [!NOTE]  
   >  Varlık türünün tanımlayıcı alanı otomatik olarak oluşturulan bir veritabanı tablosundaki bir alanı temsil ediyorsa, ayarlama **salt okunur** özelliği tanımlayıcı alanı **True**.  
  
6. İçinde **metot ayrıntıları** penceresinde yöntemi yöntemi örneğini seçin.  
  
7. İçinde **Özellikler penceresi**ayarlayın **dönüş parametresi adı** özelliğini yönteminin dönüş parametresinin adı. Yöntem örneği özellikleri hakkında daha fazla bilgi için bkz. [MethodInstance](http://go.microsoft.com/fwlink/?LinkID=169282).  
  
8. İçinde **Çözüm Gezgini**, oluşturulan hizmet kodu dosyası varlık için kısayol menüsünü açın ve ardından **kodu görüntüle**.  
  
    Varlık hizmeti kod dosyasını Kod düzenleyicisinde açılır. Varlık hizmeti kodu dosyası hakkında daha fazla bilgi için bkz. [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).  
  
9. Belirli Bulucu yöntemine kod ekleyin. Bu kod aşağıdaki görevleri gerçekleştirir:  
  
   - Bir veri kaynağındaki bir kaydı alır.  
  
   - BDC hizmeti için bir varlık döndürür.  
  
     Aşağıdaki örnekte, AdventureWorks örnek veritabanındaki SQL Server için bir kişi döndürür.  
  
     > [!NOTE]  
     >  Değiştirin `ServerName` alanını sunucunuzun adıyla.  
  
     [!code-csharp[SP_BDC#3](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/contactservice.cs#3)]
     [!code-vb[SP_BDC#3](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/contactservice.vb#3)]  
  
## <a name="see-also"></a>Ayrıca bkz.
 [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)   
 [Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)   
 [Nasıl yapılır: Bir yaratıcı metodu ekleme](../sharepoint/how-to-add-a-creator-method.md)   
 [Nasıl yapılır: Silici metodu ekleme](../sharepoint/how-to-add-a-deleter-method.md)   
 [Nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md)   
 [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)   
 [Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)   
 [Nasıl yapılır: Metot örneği tanımlama](../sharepoint/how-to-define-a-method-instance.md)  
