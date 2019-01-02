---
title: 'Nasıl Yapılır: Yerleşik bir sekmeyi özelleştirme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Ribbon [Office development in Visual Studio], tabs
- built-in tabs [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: c9f2506ae22b3d33870c4e636a27f100b70358c8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53859418"
---
# <a name="how-to-customize-a-built-in-tab"></a>Nasıl Yapılır: Yerleşik bir sekmeyi özelleştirme
  Yerleşik bir sekmeye grup ve denetim ekleyebilirsiniz. Yerleşik bir sekmeyi bir Microsoft Office uygulamasının Şerit üzerinde zaten var olan bir sekmedir. Örneğin, **veri** Excel yerleşik bir sekmede sekmesidir. Özel bir grup oluşturduğunuzda, son sekmede görünür, ancak grubunuzun sekmesinde istediğiniz yere taşıyabilirsiniz.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
> [!NOTE]  
>  Yerleşik bir sekmeye gruplar ekleyebilirsiniz, ancak yerleşik bir sekmeden varsayılan grupları silemezsiniz.  
  
### <a name="to-add-groups-to-a-built-in-tab"></a>Yerleşik bir sekmeye gruplar eklemek için  
  
1.  Şerit kod dosyasını sağ tıklatın **Çözüm Gezgini**ve ardından **Görünüm Tasarımcısı**.  
  
    > [!NOTE]  
    >  Şerit kod dosyasını görünmüyorsa **Çözüm Gezgini**, eklemelisiniz bir **Şerit öğesi** projenize. Bkz: [nasıl yapılır: Şerit özelleştirmeye başlama](../vsto/how-to-get-started-customizing-the-ribbon.md).  
  
2.  Şerit Tasarımcısı'nda herhangi bir sekmesini sağ tıklatın ve ardından **özellikleri**.  
  
3.  İçinde **özellikleri** penceresini genişletin **ControlId** özelliği ve ardından **ControlIdType** özelliğini **Office**.  
  
4.  Ayarlama **OfficeId** özelliğini *kimliği kontrol* özelleştirmek istediğiniz yerleşik bir sekmenin.  
  
     Denetim Kimliği sekmeler, gruplar ve Microsoft Office uygulamalarında yerleşik denetimler benzersiz olarak tanımlayan addır.  
  
     Denetim kimliklerinin bir listesi için bkz. [Office 2010 Yardım dosyaları: Office fluent kullanıcı arabirimi denetimi tanımlayıcıları](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
5.  Gelen **Office Şerit denetimleri** sekmesinde **araç kutusu**, grupları sekmenin sürükleyin.  
  
    > [!NOTE]  
    >  Yerleşik gruplar Tasarımcısı'nda görünmez. Bu nedenle, yerleşik bir sekmeyi ile çalışma belirlemek için tek yolu incelemektir **ControlId** sekmesinin özelliği.  
  
### <a name="to-position-groups-on-a-built-in-tab"></a>Grupları yerleşik bir sekmede konuma  
  
1.  Şerit Tasarımcısı'nda, özel bir grubu seçin.  
  
2.  İçinde **özellikleri** penceresini genişletin **konumu** özelliği.  
  
3.  Ayarlama **PositionType** uygun değere özelliği:  
  
    -   **BeforeOfficeId** grubun belirli bir yerleşik grubun önce yerleştirir.  
  
    -   **AfterOfficeId** grubun belirtilen yerleşik bir gruptan sonra yerleştirir.  
  
4.  Ayarlama **OfficeId** yerleşik grup denetim kimliği özelliği.  
  
     Denetim kimliklerinin bir listesi için bkz. [Office 2010 Yardım dosyaları: Office fluent kullanıcı arabirimi denetimi tanımlayıcıları](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Şerite Genel Bakış](../vsto/ribbon-overview.md)   
 [Şerit Tasarımcısı](../vsto/ribbon-designer.md)   
 [Şerit XML](../vsto/ribbon-xml.md)   
 [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [İzlenecek yol: Şerit XML kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)   
 [Nasıl yapılır: Şerit özelleştirmeye başlama](../vsto/how-to-get-started-customizing-the-ribbon.md)   
 [Nasıl yapılır: Şeritteki sekmenin konumunu değiştirme](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)   
 [Nasıl yapılır: Backstage görünümüne denetimler ekleme](../vsto/how-to-add-controls-to-the-backstage-view.md)   
 [Nasıl yapılır: Eklenti kullanıcı arayüzü hatalarını gösterme](../vsto/how-to-show-add-in-user-interface-errors.md)  
