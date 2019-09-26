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
ms.openlocfilehash: f0b3c6a8a9292ceda03c9d0020b78d9518ca49d9
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252040"
---
# <a name="how-to-scroll-through-database-records-in-a-worksheet"></a>Nasıl yapılır: Çalışma sayfasındaki veritabanı kayıtları arasında kaydırma
  Aşağıdaki yordamda, Microsoft Office bir Excel çalışma sayfasındaki veritabanı tablosundan, son kullanıcının tüm kayıtlarda gezindiğini etkinleştiren denetimlerle tek bir alan göstermek için tasarımcının nasıl kullanılacağı gösterilmektedir.

 Tasarımcıyı yalnızca belge düzeyinde projeler içinde kullanabilirsiniz. Bununla birlikte, denetimleri de ekleyebilir ve çalışma zamanında programlı olarak verilere bağlayabilirsiniz. Daha fazla bilgi için bkz [. İzlenecek yol: VSTO eklenti projesinde](../vsto/walkthrough-simple-data-binding-in-vsto-add-in-project.md)basit veri bağlama.

 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]

## <a name="to-scroll-through-database-records-in-a-worksheet"></a>Çalışma sayfasındaki veritabanı kayıtlarını kaydırmak için

1. Visual Studio 'da bir Excel uygulama projesi açın.

2. **Veri kaynakları** penceresini açın ve veritabanından bir veri kaynağı oluşturun. Daha fazla bilgi için bkz. [yeni bağlantılar ekleme](../data-tools/add-new-connections.md).

3. Göstermek istediğiniz verileri içeren tabloyu genişletin ve belirli sütunu seçin.

4. Denetim listesini açın ve **NamedRange**' i seçin.

5. <xref:Microsoft.Office.Tools.Excel.NamedRange> Denetimi, verilerin görünmesini istediğiniz hücreye sürükleyin.

6. Araç kutusu **Windows Forms** sekmesinden, çalışmasayfanıza bir <xref:System.Windows.Forms.BindingNavigator> denetim ekleyin ve kullanmak istediğiniz denetimleri ayarlayın. Daha fazla bilgi için bkz. [BindingNavigator denetimine &#40;genel&#41;bakış Windows Forms](/dotnet/framework/winforms/controls/bindingnavigator-control-overview-windows-forms).

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
