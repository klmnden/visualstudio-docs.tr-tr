---
title: 'Nasıl yapılır: İçinde bir BDC özelliğine özel bir derlemeyi etme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.BDC.Add_Assemblies_Dialog
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Business Data Connectivity service [SharePoint development in Visual Studio], add reference
- Business Data Connectivity service [SharePoint development in Visual Studio], custom assembly
- BDC [SharePoint development in Visual Studio], custom assembly
- BDC [SharePoint development in Visual Studio], add reference
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6de3313dad06c009244a8b784e81bf7d2a768c3b
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443109"
---
# <a name="how-to-include-a-custom-assembly-in-a-bdc-feature"></a>Nasıl yapılır: İçinde bir BDC özelliğine özel bir derlemeyi etme
  Projenizi derlemeleri aynı çözümdeki diğer projelerden başvuruda bulunabilir. Projenin özellik dosyasına kullanarak bu derlemeleri ancak eklemelisiniz **Ata başvurulan bütünleştirilmiş kodları LobSystem için** iletişim kutusu.

### <a name="to-include-a-custom-assembly-in-a-business-data-connectivity-bdc-feature"></a>Bir iş verileri bağlantısı (BDC) özelliği bir özel bütünleştirilmiş kod eklemek için

1. İçinde **Çözüm Gezgini**, İVB Modeli içeren klasörü seçin.

2. Üzerinde **görünümü** menüsünde tıklatın **Özellikler penceresi**.

3. İçinde **özellikleri** penceresinde seçin **derlemeleri** özelliği ve üç nokta düğmesini (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcı elips")).

     **Ata başvurulan bütünleştirilmiş kodları LobSystem için** iletişim kutusu görüntülenir.

4. İçinde **bir derleme seçin** listesinde, özel bir derlemeyi seçin.

    > [!NOTE]
    > Derlemeleri yalnızca görünür **Ata başvurulan bütünleştirilmiş kodları LobSystem için** derlemeyi içeren projeye başvuru eklediyseniz iletişim kutusu. Daha fazla bilgi için [nasıl yapılır: Başvurular ekleme veya kaldırma Başvuru Ekle iletişim kutusunu kullanarak](https://msdn.microsoft.com/3bd75d61-f00c-47c0-86a2-dd1f20e231c9).

5. İçinde **başvurusu özellikleri** için açılan listeyi açın, grup **LobSystem kapsamı** özelliği, özel bir derlemeyi kullanın ve ardından yöntemleri LOB sistemine seçin **Tamam**  düğmesi.

    > [!NOTE]
    > Özel derleme kodunda hata ayıklamak için derleme çözüm paketine eklemeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Ek derlemeler ekleyip](../sharepoint/how-to-add-and-remove-additional-assemblies.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Yerelleştirilmiş adlar, özellikler ve izinleri belirtmek için bir kaynak dosyası kullanma](../sharepoint/how-to-use-a-resource-file-to-specify-localized-names-properties-and-permissions.md)
- [Nasıl yapılır: Bir SharePoint projesine mevcut bir BDC modeli dosyası ekleme](../sharepoint/how-to-add-an-existing-bdc-model-file-to-a-sharepoint-project.md)
- [İş verileri bağlantı modeli oluşturma](../sharepoint/creating-a-business-data-connectivity-model.md)
- [Nasıl yapılır: BDC modeli oluşturma](../sharepoint/how-to-create-a-bdc-model.md)
- [SharePoint iş verileri Integragte](../sharepoint/integrating-business-data-into-sharepoint.md)
