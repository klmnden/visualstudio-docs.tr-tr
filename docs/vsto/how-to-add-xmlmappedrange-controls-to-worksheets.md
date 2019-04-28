---
title: 'Nasıl yapılır: Çalışma sayfalarına XMLMappedRange denetimleri ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XMLMappedRange control, adding to worksheets
- controls [Office development in Visual Studio], adding to worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 60f1fe8330e3a40676738c4187273ee60215db6d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63427442"
---
# <a name="how-to-add-xmlmappedrange-controls-to-worksheets"></a>Nasıl yapılır: Çalışma sayfalarına XMLMappedRange denetimleri ekleme
  Microsoft Office Excel hücresine bir XML öğesi eşlediğinizde, Visual Studio otomatik olarak ekler bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> çalışma denetimi.

 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]

> [!NOTE]
> <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> Denetim üzerinde kullanılabilir değil **araç kutusu** veya **veri kaynakları** penceresi. Ayrıca, oluşturulamıyor <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> programlı olarak denetler.

## <a name="to-add-an-xmlmappedrange-control-to-a-worksheet"></a>XMLMappedRange denetimi bir çalışma sayfasına eklemek için

1. Visual Studio tasarımcıda Excel çalışma kitabını açın.

2. Denetim eklemek istediğiniz çalışma sayfasını açın.

3. Üzerinde **Geliştirici** sekmesinde **kaynak**.

    > [!NOTE]
    > Varsa **Geliştirici** sekmesi, Şerit üzerinde görünür değilse, onu etkinleştirmeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Şeritte Geliştirici sekmesini gösterme](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md).

     **XML kaynağı** görev bölmesi görünür.

4. İçinde **XML kaynağı** görev bölmesi, tıklayın **XML eşlemeleri**.

5. İçinde **XML eşlemeleri** iletişim kutusu, tıklayın **Ekle**.

     **XML kaynağı** iletişim kutusu görüntülenir.

6. XML şemasından seçin **XML kaynağı** iletişim kutusu ve tıklatın **açık**.

     Şema eklenir **XML eşlemeleri** iletişim kutusu.

7. İçinde **XML eşlemeleri** iletişim kutusu, tıklayın **Tamam**.

8. Bir öğeyi sürükleyin **XML kaynağı** çalışma sayfasındaki bir hücreyi görev bölmesi.

     Bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> oluşturulur ve projeye eklendi.

    > [!NOTE]
    > Bir üst öğeden sürüklerseniz **XML kaynağı** görev bölmesi, bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetim oluşturulur.

## <a name="see-also"></a>Ayrıca bkz.
- [XmlMappedRange denetimi](../vsto/xmlmappedrange-control.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
- [Nasıl yapılır: Şemaları Visual Studio içindeki çalışma sayfalarıyla eşleştirme](../vsto/how-to-map-schemas-to-worksheets-inside-visual-studio.md)
