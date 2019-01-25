---
title: 'Nasıl yapılır: Backstage görünümüne denetimler ekleme '
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- customizing the Ribbon, menus
- controls, Ribbon
- menus, customizing
- Microsoft Office Button
- custom Ribbon, menus
- Ribbon, customizing
- Office button
- Ribbon, menus
- Microsoft Office Menu
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5334a931709f4ddfb0206c86f84f49f535a540fa
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54871695"
---
# <a name="how-to-add-controls-to-the-backstage-view"></a>Nasıl yapılır: Backstage görünümüne denetimler ekleme
  Şerit Tasarımcısı tıkladığınızda açılan menüye denetimler eklemek için kullanabileceğiniz **dosya** sekmesi. Eklediğiniz denetimler uygulama çalıştırıldığında **dosya** sekmesinde görünen adlı bir grubu **eklentileri**.  
  
 Visual Studio'da Şerit Tasarımcısını kullanarak, önce veya sonra yerleşik denetimlerin denetimler yerleştiremezsiniz. Yerleşik denetim, Backstage görünümünde önceden görüntülenen bir denetimdir. Önce veya sonra yerleşik denetimlerin yerleştirmenize istiyorsanız Şerit XML kullanmalısınız. Hakkında daha fazla bilgi için **Ribbon (XML)**, bkz: [Ribbon XML](../vsto/ribbon-xml.md). Backstage görünümünü özelleştirme hakkında daha fazla bilgi için bkz. [geliştiriciler için Office 2010 Backstage görünümüne giriş](http://go.microsoft.com/fwlink/?LinkId=182189) ve [geliştiriciler için Office 2010 Backstage görünümünü özelleştirme](http://go.microsoft.com/fwlink/?LinkId=182188).  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
### <a name="to-add-controls-to-backstage-view"></a>Backstage görünümüne denetimler ekleme  
  
1.  Şerit öğesi Tasarım Görünümü'nde açın.  
  
     Ekleme hakkında daha fazla bilgi için bir **Şerit (Görsel Tasarımcı)** öğesi projeniz için bkz: [nasıl yapılır: Şerit özelleştirmeye başlama](../vsto/how-to-get-started-customizing-the-ribbon.md).  
  
2.  Şerit Tasarımcısı'nda tıklatın **dosya** sekmesi.  
  
     Menü Tasarımcısı görüntülenir. Bu tasarım yüzeyine denetimler içermiyor.  
  
3.  Gelen **Office Şerit denetimleri** sekmesinde **araç kutusu**, aşağıdaki denetimleri menü tasarımcının üzerine sürükleyin:  
  
    -   Düğme  
  
    -   CheckBox  
  
    -   Galeri  
  
    -   Menü  
  
    -   Ayırıcı  
  
    -   SplitButton  
  
    -   ToggleButton  
  
4.  Bunları yeni konumlarına menüsünde taşımak için denetimleri sürükleyin.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Şerite Genel Bakış](../vsto/ribbon-overview.md)   
 [Şerit Tasarımcısı](../vsto/ribbon-designer.md)   
 [Şerit XML](../vsto/ribbon-xml.md)   
 [Nasıl yapılır: Başlama Şerit özelleştirme](../vsto/how-to-get-started-customizing-the-ribbon.md)   
 [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)  
