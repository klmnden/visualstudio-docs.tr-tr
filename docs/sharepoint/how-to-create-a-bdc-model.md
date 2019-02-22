---
title: 'Nasıl yapılır: BDC modeli oluşturma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- BDC [SharePoint development in Visual Studio], creating a model
- Business Data Connectivity service [SharePoint development in Visual Studio], creating a model
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d82678df0da5932dd33c08a6e3066462df204f6e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596509"
---
# <a name="how-to-create-a-bdc-model"></a>Nasıl yapılır: BDC modeli oluşturma
  Bir iş verileri bağlantısı (BDC) modeli, o tür öğeye şablonu kullanarak ve ardından modeli herhangi bir SharePoint projesine ekleme oluşturabilirsiniz. Daha fazla bilgi için [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md). Modelin nasıl tasarlanabileceğiyle ilgili daha fazla bilgi için bkz. [iş verileri bağlantı modeli tasarlama](../sharepoint/designing-a-business-data-connectivity-model.md).

### <a name="to-create-a-bdc-project"></a>Bir BDC projesi oluşturmak için

1.  Menü çubuğunda, **dosya** > **yeni** > **proje**.

    > [!NOTE]
    >  IDE'nizi Visual Basic geliştirme ayarlarını kullanmaya ayarlanmışsa seçin **dosya** > **yeni proje**.

     **Yeni proje** iletişim kutusu açılır.

2.  Ya da altında **Visual Basic** veya **Visual C#** , seçin **Office/SharePoint**, **SharePoint çözümleri**.

3.  İçinde **şablonları** bölmesinde seçin **SharePoint 2013 - boş proje** öğesi ekleyin ve ardından **Tamam** düğmesi.

     **SharePoint Özelleştirme Sihirbazı** açılır.

4.  Üzerinde **hata ayıklama için site ve güvenlik düzeyini belirtin** sayfasında yerel bilgisayarda bir SharePoint sitesi URL'sini belirtin, **Grup çözümü olarak Dağıt** seçenek düğmesini ve ardından **Son** düğmesi.

     Belirttiğiniz SharePoint sitesindeki modeli test eder.

    > [!IMPORTANT]
    >  İVB modelleri sadece grup çözümlerini desteklediğinden projeyi bir Grup çözümü olarak dağıtmanız gerekir.

     Boş bir SharePoint projesi oluşturulur.

5.  Menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

6.  İçinde **Yeni Öğe Ekle** iletişim kutusunda **Office/SharePoint** düğümü.

7.  SharePoint şablonları listesinde seçin **iş verileri bağlantı modeli (yalnızca Grup çözümü)**.

8.  İçinde **adı** kutusuna BDC modeli için bir ad belirtin ve ardından **Ekle** düğmesi.

     A **iş verileri bağlantı modeli** öğesi projeye eklenir. Varsayılan olarak, model BDC tasarımcısında görüntülenir. Daha fazla bilgi için [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).

## <a name="see-also"></a>Ayrıca bkz.
- [İş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md)
- [Nasıl yapılır: Bir SharePoint projesine mevcut bir BDC modeli dosyası ekleme](../sharepoint/how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project.md)
- [Nasıl yapılır: Yerelleştirilmiş adlar, özellikler ve izinleri belirtmek için bir kaynak dosyası kullanma](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)
- [Nasıl yapılır: İçinde bir BDC özelliğine özel bir derlemeyi etme](../sharepoint/how-to-include-a-custom-assembly-in-a-bdc-feature.md)
- [İş verilerini SharePoint ile tümleştirme](../sharepoint/integrating-business-data-into-sharepoint.md)
