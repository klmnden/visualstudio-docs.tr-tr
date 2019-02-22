---
title: 'Nasıl yapılır: Silici metodu ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], deleting data
- Business Data Connectivity service [SharePoint development in Visual Studio], Deleter
- BDC [SharePoint development in Visual Studio], Deleter
- BDC [SharePoint development in Visual Studio], removing data
- BDC [SharePoint development in Visual Studio], deleting entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], deleting entity instances
- Business Data Connectivity service [SharePoint development in Visual Studio], deleting data
- Business Data Connectivity service [SharePoint development in Visual Studio], removing data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d7a486ea4a448cb30b64631589f003854e8b1b40
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56644399"
---
# <a name="how-to-add-a-deleter-method"></a>Nasıl yapılır: Silici metodu ekleme
  Modele bir Silici metodu ekleme tarafından bir SharePoint sitesinde dış bir listeden bir veri kaydı silmek bir son kullanıcı etkinleştirebilirsiniz. Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).

### <a name="to-create-a-deleter-method"></a>Silici yöntemi oluşturmak için

1. Üzerinde **İVB Tasarımcısı**, varlık seçin.

2. Menü çubuğunda, **görünümü** > **diğer Windows** > **BDC yöntem ayrıntıları**.

    **BDC yöntem ayrıntıları** penceresi açılır. Bu pencere hakkında daha fazla bilgi için bkz. [BDC modeli Tasarım araçları genel bakış](../sharepoint/bdc-model-design-tools-overview.md).

3. İçinde **bir yöntem ekleyin** listesinde **Silici metodu Oluştur**.

    Visual Studio modele aşağıdaki öğeleri ekler. Bu öğelerin görünür **BDC yöntem ayrıntıları** penceresi.

   - Adlı bir yöntem **Sil**.

   - Yöntemi giriş parametresi.

   - Parametresi için bir tür tanımlayıcı.

   - Yöntemi için yöntem örneği.

     Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).

4. İçinde **Çözüm Gezgini**, oluşturulan hizmet kodu dosyası varlık için kısayol menüsünü açın ve ardından **kodu görüntüle**.

    Varlık hizmeti kod dosyasını Kod düzenleyicisinde açılır. Varlık hizmeti kodu dosyası hakkında daha fazla bilgi için bkz. [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).

5. Bir kaydı silmek için Silici metodu için kod ekleyin. Aşağıdaki örnekte, AdventureWorks örnek veritabanı için SQL Server kullanarak, bir satış siparişi satırı öğesini siler.

   > [!NOTE]
   >  Bu örnekte iki giriş parametresi kullanmaktadır.

   > [!NOTE]
   >  Değiştirin `ServerName` alanını sunucunuzun adıyla.

    [!code-csharp[SP_BDC#6](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/salesorderdetailservice.cs#6)]
    [!code-vb[SP_BDC#6](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/salesorderdetailservice.vb#6)]

## <a name="see-also"></a>Ayrıca bkz.
- [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)
- [Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)
- [Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-specific-finder-method.md)
- [Nasıl yapılır: Bir yaratıcı metodu ekleme](../sharepoint/how-to-add-a-creator-method.md)
- [Nasıl yapılır: Bir güncelleyici metodu ekleme](../sharepoint/how-to-add-an-updater-method.md)
- [BDC modeli tasarım araçlarına genel bakış](../sharepoint/bdc-model-design-tools-overview.md)
- [Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)
- [Nasıl yapılır: Metot örneği tanımlama](../sharepoint/how-to-define-a-method-instance.md)
