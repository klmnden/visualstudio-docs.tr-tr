---
title: 'Nasıl Yapılır: Belgeleri hizmet verileriyle doldurma'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], populating with data
- Web services [Office development in Visual Studio], populating documents
- data [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: fe69a35fb7f11eb649a45cd2d2238d1fb8e17ad1
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53647042"
---
# <a name="how-to-populate-documents-with-data-from-services"></a>Nasıl Yapılır: Belgeleri hizmet verileriyle doldurma

Windows Forms projelerinde olduğu gibi veri erişimi için Microsoft Office belge düzeyinde projelerde aynı şekilde çalışır. Çözümünüze verileri getirmek için aynı araçları ve kodu kullanın ve verileri görüntülemek için Windows Forms denetimleri bile kullanabilirsiniz. Ayrıca, olayları ve veri bağlama özelliğiyle ile zenginleştirilmiştir yerel nesneler Microsoft Office Excel ve Microsoft Office Word konak kontrollerinden yararlanabilir. Daha fazla bilgi için [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).

[!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

Aşağıdaki örnek, verilere bağlı denetimler, tasarım zamanında belgelere ekleme gösterilmektedir. Verilere bağlı denetimler, çalışma zamanında VSTO eklentiler ekleme örneği için bkz: [izlenecek yol: Bir VSTO eklenti projesinde bir hizmetten verilere bağlama](../vsto/walkthrough-binding-to-data-from-a-service-in-a-vsto-add-in-project.md).

![video bağlantı](../vsto/media/playvideo.gif "video bağlantı") ilgili video gösterimi için bkz. [nasıl yaparım? Microsoft Excel web Hizmetleri ile etkileşim? ](http://go.microsoft.com/fwlink/?LinkID=130284).

## <a name="to-populate-a-document-level-project-with-data-from-a-web-service"></a>Bir belge düzeyi projesi bir web hizmetinden veri ile doldurmak için

1.  Açık **veri kaynakları** penceresi ve projeniz için bir veri kaynağı hizmeti oluşturun. Daha fazla bilgi için [yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md).

2.  Tablo veya istediğiniz alanı sürükleyin **veri kaynakları** belgenize penceresi.

     Bir denetim, belgede oluşturulur bir <xref:System.Windows.Forms.BindingSource> oluşturulan nesne sınıfı, projenizdeki bağlanır ve sınıflar, hizmet için oluşturulur.

3.  Kodunuzda, 1. adımda bağlandığı web hizmeti sınıfının bir örneğini oluşturun.

4.  Web hizmeti ile iletişim için gerekli olan özellikleri varsa, bu özellikleri bir örneğini oluşturun.

5.  Oluşturun ve 4. adımda oluşturduğunuz Web hizmeti ve herhangi bir özellik örnekleri tarafından kullanıma sunulan yöntemleri kullanarak veri isteği gönderin.

     Kullandığınız yöntem, web hizmeti sunduğuna bağlıdır.

6.  Web hizmetine veri yanıtını atamayı <xref:System.Windows.Forms.BindingSource.DataSource%2A> özelliği <xref:System.Windows.Forms.BindingSource>.

Projeyi çalıştırdığınızda, denetimler, veri kaynağındaki ilk kaydı görüntüler. Nesneleri kullanarak para birimi olaylarını işleme göre kayıtlar arasında kaydırma etkinleştirebilirsiniz <xref:System.Windows.Forms.BindingSource>.

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümlerinde denetimlere veri bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md)
- [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Nasıl yapılır: Çalışma sayfalarını veritabanı verileriyle doldurma](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)
- [Nasıl yapılır: Belgeleri nesne verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-objects.md)
- [Nasıl yapılır: Belgeleri veritabanı verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md)
- [Nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)