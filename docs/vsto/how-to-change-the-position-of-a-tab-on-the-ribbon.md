---
title: 'Nasıl Yapılır: Şeritteki sekmenin konumunu değiştirme'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Ribbon [Office development in Visual Studio], tabs
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: c00fa747ee3c74592d491796e1281207d0c5a83f
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53647122"
---
# <a name="how-to-change-the-position-of-a-tab-on-the-ribbon"></a>Nasıl Yapılır: Şeritteki sekmenin konumunu değiştirme
  Kullanarak bir Şeritteki özel sekmelerin sırasını değiştirebilirsiniz **Sekme Derlemi Düzenleyicisi**. Önce veya sonra Şeritteki yerleşik bir sekmeyi özel sekmeler konumlandırabilirsiniz. Yerleşik bir sekmeyi bir Microsoft Office uygulamasının Şerit üzerinde zaten var olan bir sekmedir. Örneğin, **veri** Excel yerleşik bir sekmede sekmesidir.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
### <a name="to-change-the-order-of-tabs-on-the-ribbon"></a>Şeritteki sekmeler sırasını değiştirmek için  
  
1.  Şerit kod dosyasını seçin (*.vb* veya *.cs* dosya) içinde **Çözüm Gezgini**.  
  
2.  Üzerinde **görünümü** menüsünde tıklatın **Tasarımcısı**.  
  
3.  Şerit Tasarımcısını sağ tıklayın ve ardından **özellikleri**.  
  
4.  İçinde **özellikleri** penceresinde **sekmeleri** özelliği ve ardından üç nokta düğmesini (![ASP.NET Mobil Tasarımcısı elips](../sharepoint/media/mwellipsis.gif "ASP.NET Mobil Tasarımcı elips")).  
  
     **Sekme Derlemi Düzenleyicisi** görünür.  
  
5.  İçinde **Sekme Derlemi Düzenleyicisi**, **üyeleri** listesinde, istediğiniz Taşı ve yukarı veya aşağı okları sekme sırasını değiştirmek için sekmesinde seçin.  
  
### <a name="to-position-a-tab-before-or-after-a-built-in-tab-on-the-ribbon"></a>Bir sekme önce veya sonra Şeritteki yerleşik bir sekmeyi konumlandırmak için  
  
1.  Şerit Tasarımcısı'nda bir özel sekmesini seçin.  
  
2.  İçinde **özellikleri** penceresini genişletin **ControlId** özelliği ve ardından emin olun değerini **ControlIdType** özelliği **özel**.  
  
3.  İçinde **özellikleri** penceresini genişletin **konumu** özelliği.  
  
4.  Ayarlama **PositionType** uygun değere özelliği:  
  
    -   **BeforeOfficeId** grubu belirtilen yerleşik bir sekmeyi önce konumlandırır.  
  
    -   **AfterOfficeId** gruptan sonra belirtilen yerleşik bir sekmeyi konumlandırır.  
  
5.  Ayarlama **OfficeId** yerleşik bir sekmeyi denetim kimliği özelliği.  
  
     Denetim kimliklerinin bir listesi için bkz. [Office 2010 Yardım dosyaları: Office fluent kullanıcı arabirimi denetimi tanımlayıcıları](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Şerite Genel Bakış](../vsto/ribbon-overview.md)   
 [Şerit Tasarımcısı](../vsto/ribbon-designer.md)   
 [Şerit XML](../vsto/ribbon-xml.md)   
 [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [İzlenecek yol: Şerit XML kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)  
  
  