---
title: 'Nasıl yapılır: Şerit grubuna Iletişim kutusu Başlatıcısı Ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- dialog box launcher [Office development in Visual Studio]
- Ribbon [Office development in Visual Studio], dialog box launcher
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b930348845e04dca089cf153a11cc2a9fd29c880
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255901"
---
# <a name="how-to-add-a-dialog-box-launcher-to-a-ribbon-group"></a>Nasıl yapılır: Şerit grubuna Iletişim kutusu Başlatıcısı Ekleme
  Şeritteki herhangi bir gruba bir iletişim kutusu Başlatıcısı ekleyebilirsiniz. İletişim kutusu Başlatıcısı, bir grupta görüntülenen küçük bir simgedir. Kullanıcılar, grupla ilgili daha fazla seçenek sağlayan ilgili iletişim kutularını veya görev bölmelerini açmak için bu simgeye tıklayın.

 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]

### <a name="to-add-a-dialog-box-launcher-to-a-ribbon-group"></a>Şerit grubuna iletişim kutusu başlatıcısı eklemek için

1. **Çözüm Gezgini**içindeki Şerit kod dosyasını ( *. vb* veya *. cs* dosyası) seçin.

2. **Görünüm** menüsünde **Tasarımcı**' ya tıklayın.

3. Şerit Tasarımcısı ' nda herhangi bir gruba sağ tıklayın ve ardından **DialogBoxLauncher Ekle**' ye tıklayın.

     Özel veya yerleşik bir <xref:Microsoft.Office.Tools.Ribbon.RibbonGroup.DialogLauncherClick> iletişim kutusu açmak için grubun olayına kod ekleyin.

## <a name="see-also"></a>Ayrıca bkz.
- [Şerite Genel Bakış](../vsto/ribbon-overview.md)
- [Çalışma zamanında Şerite erişin](../vsto/accessing-the-ribbon-at-run-time.md)
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Şerit Tasarımcısı](../vsto/ribbon-designer.md)
- [Şerit nesne modeline genel bakış](../vsto/ribbon-object-model-overview.md)
- [Şerit XML](../vsto/ribbon-xml.md)
- [Nasıl yapılır: Şerit Tasarımcısından Şerit XML 'ine şerit aktarma](../vsto/how-to-export-a-ribbon-from-the-ribbon-designer-to-ribbon-xml.md)
- [Nasıl yapılır: Şeritteki sekmenin konumunu değiştirme](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)
- [Nasıl yapılır: Yerleşik bir sekmeyi özelleştirme](../vsto/how-to-customize-a-built-in-tab.md)
- [Nasıl yapılır: Backstage görünümüne denetimler ekleme](../vsto/how-to-add-controls-to-the-backstage-view.md)
- [Outlook için şerit özelleştirme](../vsto/customizing-a-ribbon-for-outlook.md)
- [Nasıl yapılır: Şeriti özelleştirmeye başlama](../vsto/how-to-get-started-customizing-the-ribbon.md)
- [Nasıl yapılır: Eklenti kullanıcı arabirimi hatalarını göster](../vsto/how-to-show-add-in-user-interface-errors.md)
- [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)
- [İzlenecek yol: Çalışma zamanında Şeritteki denetimleri güncelleştirme](../vsto/walkthrough-updating-the-controls-on-a-ribbon-at-run-time.md)
- [İzlenecek yol: Şerit XML kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)
