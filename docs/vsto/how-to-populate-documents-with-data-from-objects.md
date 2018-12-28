---
title: 'Nasıl Yapılır: Belgeleri nesne verileriyle doldurma'
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
- data [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 87e194aa29a44458c23e5057d7813e5e21ffbc42
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53648387"
---
# <a name="how-to-populate-documents-with-data-from-objects"></a>Nasıl Yapılır: Belgeleri nesne verileriyle doldurma

Windows Forms projelerinde olduğu gibi bir veri nesnesi içinde veri belirtilmemelidir Microsoft Office Word için belge düzeyi projelerine aynı şekilde çalışır. Verileri bir nesneden çözümünüze getirmek için aynı araçları ve kodu kullanın ve verileri görüntülemek için Windows Forms denetimleri kullanabilirsiniz. Ayrıca, konak denetimleri kullanarak verileri görüntüleyebilirsiniz. Konak denetimleri, olayları ve veri bağlama özelliğiyle ile zenginleştirilmiştir yerel Microsoft Office Word nesnelerdir. Daha fazla bilgi için [konak öğelerini ve denetimlerine genel bakış için ana bilgisayar](../vsto/host-items-and-host-controls-overview.md).

[!INCLUDE[appliesto_controls](../vsto/includes/appliesto-controls-md.md)]

Belgenin bir nesneyi verilerle doldurmak için üç temel adımlarını tamamlamanız gerekir:

-   Verilere bağlayabilirsiniz belge için bir denetim ekleyin.

-   Bir veri nesnesi belgeye ekleyin.

-   Veri nesnesi için BindingSource bağlanın.

## <a name="to-add-a-data-object"></a>Bir veri nesnesi eklemek için

Bir veri nesnesi eklemek için açık **veri kaynakları** penceresi ve bir nesneden bir veri kaynağı oluşturun. Daha fazla bilgi için [yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md).

## <a name="connect-the-data-object-to-the-bindingsource"></a>Veri nesnesi için BindingSource bağlanma

Belge düzeyi projelere belgeniz için denetimler ekleme ve bunları tasarım zamanında verilere bağlayın.

VSTO eklentisi projeleri, denetimleri oluşturur ve bunları çalışma zamanında bağlayın.

### <a name="document-level-projects"></a>Belge düzeyi projeleri

Veri nesnesi için BindingSource bağlanmak için:

1.  İstediğiniz veri alanına sürükleyin **veri kaynakları** belgenize penceresi. Bu, bir denetimi otomatik olarak oluşturur.

2.  Kodunuzda, veri kaynağı için seçtiğiniz nesnenin türü örneği oluşturun.

3.  Örneğine atadığınız <xref:System.Windows.Forms.BindingSource.DataSource%2A> özelliği <xref:System.Windows.Forms.BindingSource>.

### <a name="application-level-projects"></a>Uygulama düzeyi projeleri

Veri nesnesi için BindingSource bağlanmak için:

1.  Kodunuzda, veri kaynağıyla ilişkili olan nesnenin türü örneği oluşturun.

2.  Bir örneğini oluşturmak bir <xref:System.Windows.Forms.BindingSource>.

3.  Veri kaynağı örneği atayın <xref:System.Windows.Forms.BindingSource.DataSource%2A> özelliği <xref:System.Windows.Forms.BindingSource>.

4.  Veri kaynağı bir veri bağlama denetimine ekleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md)
- [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Nasıl yapılır: Belgeleri veritabanı verileriyle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md)
- [Nasıl yapılır: Bir konak kontrolü verileriyle veri kaynağını güncelleme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)
- [BindingSource bileşenine genel bakış](/dotnet/framework/winforms/controls/bindingsource-component-overview)