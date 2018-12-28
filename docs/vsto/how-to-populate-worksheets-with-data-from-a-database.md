---
title: 'Nasıl Yapılır: Çalışma sayfalarını veritabanı verileriyle doldurma'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets [Office development in Visual Studio], populating
- databases [Office development in Visual Studio], populating worksheets
- data [Office development in Visual Studio], adding to worksheets
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 53267cdd429b9a4d8848026e460776359b55c023
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53802880"
---
# <a name="how-to-populate-worksheets-with-data-from-a-database"></a>Nasıl Yapılır: Çalışma sayfalarını veritabanı verileriyle doldurma

Windows Forms projeleri verilere erişmek, aynı şekilde, belge düzeyinde Office projelerinde veri erişebilirsiniz. Çözümünüze verileri getirmek için aynı araçları ve kodu kullanın ve verileri görüntülemek için Windows Forms denetimleri bile kullanabilirsiniz. Ayrıca, Microsoft Office Excel olayları ve veri bağlama özelliğiyle Gelişmiş yerel nesneler olan konak kontrollerinden yararlanabilir. Daha fazla bilgi için [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).

[!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]

Aşağıdaki örnek, bir tasarımcı kullanarak belge düzeyinde projelerde verilere bağlı denetimler eklemek gösterilmektedir. Verilere bağlı denetimler, çalışma zamanında uygulama düzeyi projelerine ekleme örneği için bkz: [izlenecek yol: VSTO eklenti projesinde karmaşık veri bağlama](../vsto/walkthrough-complex-data-binding-in-vsto-add-in-project.md).

![video bağlantı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [nasıl yaparım? Verileri bir Excel çalışma sayfasına aktarabilir? ](http://go.microsoft.com/fwlink/?LinkID=130277), ve [nasıl yaparım? Veritabanı verileri Excel'de mı tüketiliyor? ](http://go.microsoft.com/fwlink/?LinkID=130287).

## <a name="add-a-data-bound-control-to-a-worksheet-at-design-time"></a>Veriye bağlı denetim tasarım zamanında çalışma sayfasına ekleme

### <a name="to-populate-a-worksheet-with-data-from-a-database"></a>Bir çalışma sayfasına bir veritabanındaki verilerle doldurmak için

1.  Excel belge düzeyi projesi çalışma açıkken tasarımcıda Visual Studio'da açın.

2.  Açık **veri kaynakları** penceresi ve projeniz için bir veri kaynağı oluşturun. Daha fazla bilgi için [yeni bağlantı ekleme](../data-tools/add-new-connections.md).

3.  İstediğiniz tablo ve alan sürükleyin **veri kaynakları** çalışma penceresine.

Aşağıdaki denetimlerden birini çalışma sayfasında oluşturulur:

-   Bir alanı sürüklediğinizde bir <xref:Microsoft.Office.Tools.Excel.NamedRange> denetimi, çalışma sayfasında oluşturulur. Daha fazla bilgi için [NamedRange denetimi](../vsto/namedrange-control.md).

-   Bir tablo sürüklerseniz bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetimi, çalışma sayfasında oluşturulur. Daha fazla bilgi için [ListObject denetimine](../vsto/listobject-control.md).

Tabloyu seçerek farklı denetim ekleme ya da, alan **veri kaynakları** penceresini açın ve ardından açılır listeden farklı bir denetim seçme.

## <a name="objects-in-the-project"></a>Projesindeki nesneleri

Denetimin yanı sıra aşağıdaki verilerle ilgili nesneleri otomatik olarak projenize eklenir:

-   Veritabanına bağlı veri tablolarının kapsülleyen bir türü belirtilmiş veri kümesi. Daha fazla bilgi için [Visual Studio'daki veri kümesi Araçları](../data-tools/dataset-tools-in-visual-studio.md).

-   A <xref:System.Windows.Forms.BindingSource> , Denetim türü belirtilmiş veri kümesine bağlanır. Daha fazla bilgi için [BindingSource bileşenine genel bakış](/dotnet/framework/winforms/controls/bindingsource-component-overview).

-   Bir TableAdapter veritabanına yazılan veri kümesi bağlar. Daha fazla bilgi için [TableAdapter genel bakışı](../data-tools/fill-datasets-by-using-tableadapters.md#tableadapter-overview).

-   Hiyerarşik güncelleştirmeleri etkinleştirmek için veri kümesinde tablo bağdaştırıcıları koordine etmek için kullanılan bir TableAdapterManager. Daha fazla bilgi için [hiyerarşik güncelleştirme](../data-tools/hierarchical-update.md) ve [TableAdapterManager başvuru](../data-tools/fill-datasets-by-using-tableadapters.md#tableadaptermanager-reference).

Projeyi çalıştırdığınızda, denetim veri kaynağındaki ilk kaydı görüntüler. Kullanabileceğiniz <xref:System.Windows.Forms.BindingSource> kayıtlarda gezinin olanağı.

### <a name="to-scroll-through-the-records"></a>Kayıtlarda gezinmek için

-   Kullanım <xref:System.Windows.Forms.BindingSource> gibi yöntemler <xref:System.Windows.Forms.BindingSource.MoveNext%2A> ve <xref:System.Windows.Forms.BindingSource.MovePrevious%2A>.

Güncelleştirmeleri yazılmış veri kümesi ve veritabanına gönderme hakkında daha fazla bilgi için bkz: [nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md)
- [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Nasıl yapılır: Belgeleri nesne verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-objects.md)
- [Nasıl yapılır: Belgeleri veritabanı verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md)
- [Nasıl yapılır: Belgeleri hizmet verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-services.md)
- [Nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)
- [Nasıl Yaparım Bir Excel çalışma sayfasına veri aktarımı](http://go.microsoft.com/fwlink/?LinkID=130277)
- [Nasıl Yaparım Veritabanı verileri Excel'de mı tüketiliyor?](http://go.microsoft.com/fwlink/?LinkID=130287)