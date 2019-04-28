---
title: 'Nasıl yapılır: Bir Bulucu metoduna filtre tanımlayıcısı ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], filter descriptors
- Business Data Connectivity service [SharePoint development in Visual Studio], add a filter
- BDC [SharePoint development in Visual Studio], add a filter
- BDC [SharePoint development in Visual Studio], filter descriptors
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: fceb6270aea9da5af1a53adf7560df7dd3702349
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63418300"
---
# <a name="how-to-add-a-filter-descriptor-to-a-finder-method"></a>Nasıl yapılır: Bir Bulucu metoduna filtre tanımlayıcısı ekleme
  Filtre tanımlayıcıları, yürütmeden önce değerleri yöntemlere geçirmek model tüketicilerinin etkinleştirin. Daha fazla bilgi için [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).

 Sık karşılaşılan senaryolardan biri, kullanıcıların SharePoint dış içerik türü'nın bazı ölçütlerle eşleşen örneğini almak istediğiniz ' dir. Bu senaryo bir Bulucu yöntemine filtre tanımlayıcısı ekleyerek destekler.

### <a name="to-add-a-filter-descriptor-to-a-finder-method"></a>Bir Bulucu metoduna filtre tanımlayıcısı ekleme

1. İçinde **BDC yöntem ayrıntıları** penceresinde bir Bulucu yöntemi düğümünü genişletin, **parametreleri** düğümünü ve ardından giriş parametresi ekleyin. Daha fazla bilgi için [nasıl yapılır: Bir yönteme parametre eklemek](../sharepoint/how-to-add-a-parameter-to-a-method.md).

2. İçinde **metot ayrıntıları** penceresinde, parametrenin tür tanımlayıcısını seçin.

3. Menü çubuğunda, **görünümü** > **Özellikler penceresi**.

4. İçinde **özellikleri** penceresinde **tür adı** özellik filtresi için uygun bir veri türü.

     Örneğin, bir filtre, sipariş tarihi yöntem tarafından döndürülen satış siparişleri sayısını sınırlamak için kullanabilirsiniz. Bu filtre desteklemek için **tür adı** tür tanımlayıcısı özelliği ayarlanmalıdır **System.DateTime**.

5. İçinde **metot ayrıntıları** penceresini genişletin **filtre tanımlayıcıları** düğümü.

6. İçinde **filtre tanımlayıcısı ekleme** listesinde **filtre tanımlayıcısı oluştur**.

     Yeni filtre tanımlayıcısı düğmesinin altında görünür **filtre tanımlayıcıları** düğümü.

7. Menü çubuğunda, **görünümü** > **Özellikler penceresi**.

8. İçinde **özellikleri** penceresinde seçin **türü** özelliği.

9. İçin görüntülenen listedeki **türü** özelliğini istediğiniz filtre deseni seçin.

     Örneğin, sipariş tarihi bir Bulucu yöntemi döndürülen satış siparişleri sayısını sınırlamak için kullandığı bir filtre oluşturmak için tercih **karşılaştırma**. Bir Bulucu yöntemi belirli bir koşulu karşılayan örneklerini döndüren bir karşılaştırma filtresi sağlar. Her filtre desen hakkında daha fazla bilgi için bkz: [, filtre tarafından desteklenen türleri İVB](http://go.microsoft.com/fwlink/?LinkId=169287).

10. İçinde **özellikleri** penceresinde seçin **ilişkili tür tanımlayıcısı** özelliği.

11. İçin görüntülenen listedeki **ilişkili tür tanımlayıcısı** özelliği, bu yordamda daha önce oluşturduğunuz tür tanımlayıcısını seçin. Bu Bulucu metodunu giriş parametresi için filtre ilişkilendirir.

12. Veri döndüren Bulucu yöntemine kod ekleyin. Select sorgusunda koşulu olarak giriş parametresini kullanabilirsiniz.

     Aşağıdaki örnek belirtilen bir sipariş tarihi olan satış siparişlerini döndürür.

    > [!NOTE]
    > Değiştirin `ServerName` alanını sunucunuzun adıyla.

     [!code-csharp[SP_BDC#11](../sharepoint/codesnippet/CSharp/SP_BDC/bdcmodel1/salesorderservice.cs#11)]
     [!code-vb[SP_BDC#11](../sharepoint/codesnippet/VisualBasic/sp_bdc/bdcmodel1/salesorderservice.vb#11)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-finder-method.md)
- [Nasıl yapılır: Belirli bir Bulucu yöntemi ekleme](../sharepoint/how-to-add-a-specific-finder-method.md)
- [Nasıl yapılır: Bir yönteme bir parametre ekleyin](../sharepoint/how-to-add-a-parameter-to-a-method.md)
- [Nasıl yapılır: Bir parametrenin tür tanımlayıcısını tanımlama](../sharepoint/how-to-define-the-type-descriptor-of-a-parameter.md)
- [İş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md)
- [İş verilerini SharePoint ile tümleştirme](../sharepoint/integrating-business-data-into-sharepoint.md)
