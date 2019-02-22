---
title: 'Nasıl yapılır: Bir yaratıcı metodu ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], Creator
- BDC [SharePoint development in Visual Studio], adding entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], adding entities
- Business Data Connectivity service [SharePoint development in Visual Studio], adding entity instances
- BDC [SharePoint development in Visual Studio], adding entities
- Business Data Connectivity service [SharePoint development in Visual Studio], Creator
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1c1596213b618ba67cd4bf1406f63c0754fd9b96
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56619322"
---
# <a name="how-to-add-a-creator-method"></a>Nasıl yapılır: Bir yaratıcı metodu ekleme
  Bir yaratıcı yöntemi, bir varlığın veri kaynağına yeni veri ekler. Kullanıcıların iş verileri bağlantısı (BDC) hizmeti bu yöntemi çağırır **yeni öğe** düğmesini **Şerit** listesini modelini temel alıyor. Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).

### <a name="to-add-a-creator-method"></a>Bir yaratıcı metodu ekleme

1. Üzerinde **İVB Tasarımcısı**, varlık seçin.

2. Menü çubuğunda, **görünümü** > **diğer Windows** >**BDC yöntem ayrıntıları**.

    **BDC yöntem ayrıntıları** penceresi açılır. Bu pencere hakkında daha fazla bilgi için bkz. [BDC modeli Tasarım araçları genel bakış](../sharepoint/bdc-model-design-tools-overview.md).

3. İçinde **bir yöntem ekleyin** listesinde **Oluşturucu metodu Oluştur**.

    Visual Studio, modele aşağıdaki öğeleri ekler ve bu öğelerin görünür **BDC yöntem ayrıntıları** penceresi.

   - Adlı bir yöntem **Oluştur**.

   - Yöntemi giriş parametresi.

   - Yöntemin bir dönüş parametresi.

   - Tür tanımlayıcıları için parametreleri.

   - Yöntemi için yöntem örneği.

     Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).

4. İçinde **Çözüm Gezgini**, oluşturulan hizmet kodu dosyası varlık için kısayol menüsünü açın ve ardından **kodu görüntüle**.

    Varlık hizmeti kod dosyasını Kod düzenleyicisinde açılır. Varlık hizmeti kodu dosyası hakkında daha fazla bilgi için bkz. [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).

5. Veri kaynağına veri ekler Oluşturucu yöntemine kod ekleyin. Aşağıdaki örnek, bir kişi SQL Server için AdventureWorks örnek veritabanına ekler.

   > [!NOTE]
   >  Değiştirin `ServerName` alanını sunucunuzun adıyla.

    [!code-csharp[SP_BDC#4](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/contactservice.cs#4)]
    [!code-vb[SP_BDC#4](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/contactservice.vb#4)]

## <a name="see-also"></a>Ayrıca bkz.
- [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)
- [Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)
- [Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-specific-finder-method.md)
- [Nasıl yapılır: Silici metodu ekleme](../sharepoint/how-to-add-a-deleter-method.md)
- [Nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md)
- [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)
- [Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)
- [Nasıl yapılır: Metot örneği tanımlama](../sharepoint/how-to-define-a-method-instance.md)
