---
title: 'Nasıl yapılır: Çalışma sayfasındaki veritabanı kayıtları arasında kaydırma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- databases [Office development in Visual Studio], scrolling records
- records [Office development in Visual Studio], scrolling
- data [Office development in Visual Studio], scrolling database records
- worksheets [Office development in Visual Studio], scrolling records
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 0b3ee44c6666a887552f1babfcbbf028e9215e95
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094716"
---
# <a name="how-to-scroll-through-database-records-in-a-worksheet"></a>Nasıl yapılır: Çalışma sayfasındaki veritabanı kayıtları arasında kaydırma
  Aşağıdaki yordam bir Microsoft Office Excel çalışma sayfasındaki tüm kayıtlarda gezinin son kullanıcının etkinleştirme denetimleri ile bir veritabanı tablosundan tek bir alan görüntülemek için tasarımcı kullanmayı gösterir.

 Tasarımcı yalnızca belge düzeyinde projelerde kullanabilirsiniz. Ancak, ayrıca denetimler ekleme ve bunları programlı olarak çalışma zamanında verilere bağlayın. Daha fazla bilgi için [izlenecek yol: VSTO eklenti projesinde basit veri bağlama](../vsto/walkthrough-simple-data-binding-in-vsto-add-in-project.md).

 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]

## <a name="to-scroll-through-database-records-in-a-worksheet"></a>Çalışma sayfasındaki veritabanı kayıtları arasında kaydırma

1. Bir Excel uygulaması projesini Visual Studio'da açın.

2. Açık **veri kaynakları** penceresi ve veritabanından bir veri kaynağı oluşturun. Daha fazla bilgi için [yeni bağlantı ekleme](../data-tools/add-new-connections.md).

3. Göstermek istediğiniz verileri içeren tabloyu genişletmek ve belirli sütunu seçin.

4. Denetimleri ve seçin listeyi açın **NamedRange**.

5. Sürükleme <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi hücrenin verilerin görünmesi istediğiniz yere sürükleyin.

6. Gelen **Windows Forms** sekmesinde **araç kutusu**, ekleme bir <xref:System.Windows.Forms.BindingNavigator> denetlemek için çalışma ve kullanmak istediğiniz denetimlerini ayarlayın. Daha fazla bilgi için [BindingNavigator denetimine genel bakış &#40;Windows Forms&#41;](/dotnet/framework/winforms/controls/bindingnavigator-control-overview-windows-forms).

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
