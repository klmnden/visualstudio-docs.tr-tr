---
title: 'Nasıl yapılır: Yerelleştirilmiş adlar, özellikler ve izinleri belirtmek için bir kaynak dosyası kullanma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], localize strings
- BDC [SharePoint development in Visual Studio], localize strings
- BDC [SharePoint development in Visual Studio], resource file
- Business Data Connectivity service [SharePoint development in Visual Studio], resource strings
- BDC [SharePoint development in Visual Studio], properties
- Business Data Connectivity service [SharePoint development in Visual Studio], properties
- Business Data Connectivity service [SharePoint development in Visual Studio], resource file
- BDC [SharePoint development in Visual Studio], resource strings
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 2be88a29d3e9e3da9d1963aa1226ffca0a0a2bbd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62813055"
---
# <a name="how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions"></a>Nasıl yapılır: Yerelleştirilmiş adlar, özellikler ve izinleri belirtmek için bir kaynak dosyası kullanma
  Bir kaynak dosyası kullanarak, yerelleştirilmiş adlar sağlamak, özelliklerini tanımlayın ve bir iş verileri bağlantısı (BDC) modelde tanımlı izinleri tor nesneleri geçerli. Bu bilgileri belirtmek için eklediğiniz bir **iş verileri bağlantısı kaynak** içeren bir proje öğesine bir **iş verileri bağlantı modeli** öğesi. Ardından, adları, özellikler ve izinleri XML kaynak dosyası için düzenleyerek belirtin.

### <a name="to-add-a-bdc-resource-file-to-a-sharepoint-project"></a>Bir BDC kaynak dosyasını bir SharePoint projesine eklemek için

1. İçinde **Çözüm Gezgini**SharePoint proje klasörünü genişletin ve ardından İVB Modeli içeren klasörü seçin.

2. Menü çubuğunda, **proje** > **Yeni Öğe Ekle**.

3. Genişletin **SharePoint** düğümünü seçip **2010** düğümü.

4. İçinde **Yeni Öğe Ekle** iletişim kutusunda **iş verileri bağlantısı kaynak öğesi**.

5. İçinde **adı** kutusuna kaynak dosyasının adını belirtin ve ardından **Ekle** düğmesi.

     .Bdcr uzantısına sahip bir kaynak dosyası projeye eklenir ve düzenleme için açılmış.

6. Yerelleştirilmiş adlar, özellikler ve BDC modelini uygulamak istediğiniz izinleri tanımlamak için XML ekleyin.

     Bu öğeleri tanımlama hakkında daha fazla bilgi için bkz: [modeli ve kaynak dosyalarını](http://go.microsoft.com/fwlink/?LinkID=169283).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir SharePoint projesine mevcut bir BDC modeli dosyası ekleme](../sharepoint/how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project.md)
- [İş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md)
- [Nasıl yapılır: BDC modeli oluşturma](../sharepoint/how-to-create-a-bdc-model.md)
- [Nasıl yapılır: İçinde bir BDC özelliğine özel bir derlemeyi etme](../sharepoint/how-to-include-a-custom-assembly-in-a-bdc-feature.md)
- [İş verilerini SharePoint ile tümleştirme](../sharepoint/integrating-business-data-into-sharepoint.md)
