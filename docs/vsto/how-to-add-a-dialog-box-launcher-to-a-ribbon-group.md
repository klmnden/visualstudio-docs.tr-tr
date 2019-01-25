---
title: 'Nasıl yapılır: Bir Şerit grubuna iletişim kutusu başlatıcısı ekleme'
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
ms.openlocfilehash: ac39cd45c566d837d34cf8e7be0cf94ded8de419
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54862544"
---
# <a name="how-to-add-a-dialog-box-launcher-to-a-ribbon-group"></a>Nasıl yapılır: Bir Şerit grubuna iletişim kutusu başlatıcısı ekleme
  Herhangi bir Şerit grubuna iletişim kutusu başlatıcısı ekleyebilirsiniz. İletişim kutusu başlatıcısı içinde bir grup görünür küçük bir simgedir. Kullanıcılar, ilgili iletişim kutusu veya Grup ile ilgili daha fazla seçenek sağlayan görev bölmeleri açmak için bu simgeye tıklayın.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
### <a name="to-add-a-dialog-box-launcher-to-a-ribbon-group"></a>Şerit grubuna iletişim kutusu başlatıcısı ekleme  
  
1.  Şerit kod dosyasını seçin (*.vb* veya *.cs* dosya) içinde **Çözüm Gezgini**.  
  
2.  Üzerinde **görünümü** menüsünde tıklatın **Tasarımcısı**.  
  
3.  Şerit Tasarımcısı'nda tüm grubuna sağ tıklayın ve ardından **DialogBoxLauncher Ekle**.  
  
     Kodu <xref:Microsoft.Office.Tools.Ribbon.RibbonGroup.DialogLauncherClick> olay grubu yerleşik veya özel iletişim kutusunu açın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Şerite Genel Bakış](../vsto/ribbon-overview.md)   
 [Şerit, çalışma zamanında erişme](../vsto/accessing-the-ribbon-at-run-time.md)   
 [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)   
 [Şerit Tasarımcısı](../vsto/ribbon-designer.md)   
 [Şerit nesne modeline genel bakış](../vsto/ribbon-object-model-overview.md)   
 [Şerit XML](../vsto/ribbon-xml.md)   
 [Nasıl yapılır: Bir Şerit Şerit Tasarımcısından Şerit dışarı aktarma](../vsto/how-to-export-a-ribbon-from-the-ribbon-designer-to-ribbon-xml.md)   
 [Nasıl yapılır: Şeritteki sekmenin konumunu değiştirme](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)   
 [Nasıl yapılır: Yerleşik bir sekmeyi özelleştirme](../vsto/how-to-customize-a-built-in-tab.md)   
 [Nasıl yapılır: Backstage görünümüne denetimler ekleme](../vsto/how-to-add-controls-to-the-backstage-view.md)   
 [Outlook için Şerit özelleştirme](../vsto/customizing-a-ribbon-for-outlook.md)   
 [Nasıl yapılır: Şerit özelleştirmeye başlama](../vsto/how-to-get-started-customizing-the-ribbon.md)   
 [Nasıl yapılır: Eklenti kullanıcı arayüzü hatalarını gösterme](../vsto/how-to-show-add-in-user-interface-errors.md)   
 [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [İzlenecek yol: Çalışma zamanında Şerit denetimlerini güncelleştirme](../vsto/walkthrough-updating-the-controls-on-a-ribbon-at-run-time.md)   
 [İzlenecek yol: Şerit XML kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)  
