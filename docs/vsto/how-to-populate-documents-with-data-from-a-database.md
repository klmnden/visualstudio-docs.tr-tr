---
title: 'Nasıl Yapılır: Belgeleri veritabanı verileriyle doldurma'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents, populating with data
- data, adding to documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 71c2494a4c1b70e6bcf40b23062f70e91587f2e3
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53647397"
---
# <a name="how-to-populate-documents-with-data-from-a-database"></a>Nasıl Yapılır: Belgeleri veritabanı verileriyle doldurma

Aynı şekilde, Windows Forms projeleri verilere erişmek için Microsoft Office belge düzeyi projelere verilerine erişebilir. Çözümünüze bir veritabanından verileri getirmek için aynı araçları ve kodu kullanın ve verileri görüntülemek için Windows Forms denetimleri kullanabilirsiniz.

Ayrıca, konak denetimleri kullanarak verileri görüntüleyebilirsiniz. Konak denetimleri, olayları ve veri bağlama özelliğiyle ile zenginleştirilmiştir yerel Microsoft Office Word nesnelerdir. Daha fazla bilgi için [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).

[!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]

Aşağıdaki örnek, bir tasarımcı kullanarak belge düzeyinde projelerde verilere bağlı denetimler eklemek gösterilmektedir. Çalışma zamanında VSTO eklenti projesinde verilere bağlı denetimler eklemek nasıl bir örnek için bkz [izlenecek yol: VSTO eklenti projesinde basit veri bağlama](../vsto/walkthrough-simple-data-binding-in-vsto-add-in-project.md).

![video bağlantısı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [Word 2007 içerik veri bağlama denetimleri kullanarak Visual Studio Araçları Office sistemi (3.0) için](http://go.microsoft.com/fwlink/?LinkId=136785).

## <a name="add-a-control-to-a-document-at-design-time"></a>Denetim belgeye çalışma zamanında ekleme

### <a name="to-populate-a-document-with-data-from-a-database"></a>Bir belge bir veritabanındaki verilerle doldurmak için

1.  Word belge düzeyi projede açın [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], belge tasarımcıda açık.

2.  Açık **veri kaynakları** penceresi ve bir veritabanından bir veri kaynağı oluşturun. Daha fazla bilgi için [yeni bağlantı ekleme](../data-tools/add-new-connections.md).

3.  İstediğiniz alanı sürükleyin **veri kaynakları** belgenize penceresi.

Bir içerik denetimi, belgeye eklenir. İçerik denetimi türü, seçtiğiniz alan, veri türüne göre değişir. Daha fazla bilgi için [içerik denetimleri](../vsto/content-controls.md).

Veri alanını seçerek farklı bir denetim ekleyebilirsiniz **veri kaynakları** penceresini açın ve ardından açılır listeden farklı bir denetim seçme.

## <a name="objects-in-the-project"></a>Projesindeki nesneleri

Denetimin yanı sıra aşağıdaki verilerle ilgili nesneleri otomatik olarak projenize eklenir:

-   Veritabanına bağlı veri tablolarının kapsülleyen bir türü belirtilmiş veri kümesi. Daha fazla bilgi için [Visual Studio'daki veri kümesi Araçları](../data-tools/dataset-tools-in-visual-studio.md).

-   A <xref:System.Windows.Forms.BindingSource> , Denetim türü belirtilmiş veri kümesine bağlanır. Daha fazla bilgi için [BindingSource bileşenine genel bakış](/dotnet/framework/winforms/controls/bindingsource-component-overview).

-   Bir TableAdapter veritabanına yazılan veri kümesi bağlar. Daha fazla bilgi için [oluştur ve TableAdapter yapılandırma](../data-tools/create-and-configure-tableadapters.md).

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
- [Nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)
- [Office çözümlerine genel bakış yerel veritabanı dosyaları kullanma](../vsto/using-local-database-files-in-office-solutions-overview.md)
- [BindingSource bileşenine genel bakış](/dotnet/framework/winforms/controls/bindingsource-component-overview)