---
title: 'Nasıl yapılır: Bir SharePoint projesine mevcut bir BDC modeli dosyası ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.BDC.ImportDialog
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], import a model
- Business Data Connectivity service [SharePoint development in Visual Studio], reuse a model
- BDC [SharePoint development in Visual Studio], import a model
- BDC [SharePoint development in Visual Studio], remove a model
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 9c10dcf48e5c047778b86c524b35b4e1d5d8cc8a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967059"
---
# <a name="how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project"></a>Nasıl yapılır: Bir SharePoint projesine mevcut bir BDC modeli dosyası ekleme
  Özelleştirme, paket ve model dosyası eklemek için Visual Studio kullanarak bir iş verileri bağlantısı (BDC) modeli yeniden (*.bdcm*) herhangi bir SharePoint grubu projesine. Daha fazla bilgi için [iş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md).

### <a name="to-add-a-bdc-model-file-to-a-sharepoint-project"></a>Bir SharePoint projesine bir BDC modeli dosyası ekleme

1. İçinde **Çözüm Gezgini**, bir SharePoint proje klasörünü seçin.

2. Menü çubuğunda, **proje** > **varolan öğeyi Ekle**.

3. İçinde **varolan öğeyi Ekle** iletişim kutusu, projenize ekleyin, dosyayı seçin ve ardından istediğiniz model tanım dosyasının konumuna göz atın **Ekle** düğmesi.

    Model tanımlamıyorsa bir *türü .NET bütünleştirilmiş kodu satır, iş kolu (LOB) sistemine*, **LobSystem ekleme .NET bütünleştirilmiş kodu** iletişim kutusu açılır.

4. İletişim kutusu görüntülenirse, aşağıdaki adımlardan birini gerçekleştirin:

   - Öğesini alınan model meta verilerini tanımlamak için bir tasarımcı kullanır ve özel kod yazmak istiyorsanız **Evet** düğmesi, sistem adlandırın ve ardından **Tamam** düğmesi.

   - Aksi takdirde seçin **Hayır** düğmesine ve ardından **Tamam** düğmesi.

     **İş verileri bağlantı modeli** öğesi projeye eklenir.

## <a name="see-also"></a>Ayrıca bkz.
- [İş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md)
- [Nasıl yapılır: BDC modeli oluşturma](../sharepoint/how-to-create-a-bdc-model.md)
- [Nasıl yapılır: Yerelleştirilmiş adlar, özellikler ve izinleri belirtmek için bir kaynak dosyası kullanma](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)
- [Nasıl yapılır: İçinde bir BDC özelliğine özel bir derlemeyi etme](../sharepoint/how-to-include-a-custom-assembly-in-a-bdc-feature.md)
- [İş verilerini SharePoint ile tümleştirme](../sharepoint/integrating-business-data-into-sharepoint.md)
