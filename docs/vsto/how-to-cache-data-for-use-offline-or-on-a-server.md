---
title: 'Nasıl yapılır: Çevrimdışı veya sunucuda kullanmak için verileri önbelleğe'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data caching [Office development in Visual Studio], server use
- Office applications [Office development in Visual Studio], data
- datasets [Office development in Visual Studio], caching
- offline data [Office development in Visual Studio]
- data [Office development in Visual Studio], caching
- data caching [Office development in Visual Studio], offline use
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7c53d7bd1264ff21866746796d598b27cfac5984
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094547"
---
# <a name="how-to-cache-data-for-use-offline-or-on-a-server"></a>Nasıl yapılır: Çevrimdışı veya sunucuda kullanmak için verileri önbelleğe
  Böylece kullanılabilir bir veri öğesi belgede önbelleğe alınacak çevrimdışı olarak işaretleyebilirsiniz. Bu ayrıca, belgeyi bir sunucuda depolandığında başka kod tarafından değiştirilmesine belgedeki verileri mümkün kılar.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Veri öğesi kodunuzda bildirildiği veya kullanıyorsanız önbelleğe alınacak bir veri öğesi işaretleyebilirsiniz bir <xref:System.Data.DataSet>, bir özelliği ayarlayarak **özellikleri** penceresi. Olmayan bir veri öğesi önbellek, bir <xref:System.Data.DataSet> veya <xref:System.Data.DataTable>, belgede önbelleğe alınmasını ölçütleri karşıladığından emin olun. Daha fazla bilgi için [veriyi önbelleğe alma](../vsto/caching-data.md).

> [!NOTE]
>  Olarak işaretlenmiş bir Visual Basic kullanılarak oluşturulan veri kümelerini **önbelleğe alınan** ve **WithEvents** (gelen sürüklediğiniz veri kümeleri dahil olmak üzere **veri kaynakları** penceresi veya **Araç kutusu** sahip **CacheInDocument** özelliğini **True**) önbelleğinde adları alt çizgi öneklerine sahiptir. Örneğin, bir veri kümesi oluşturun ve adlandırın **müşteriler**, <xref:Microsoft.VisualStudio.Tools.Applications.CachedDataItem> ad **_Customers** önbelleğinde. Kullanırken <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> önbelleğe alınan bu öğeye erişmek için belirtmelisiniz **_Customers** yerine **müşteriler**.

### <a name="to-cache-data-in-the-document-using-code"></a>Kod kullanarak belgede veriyi önbelleğe almak için

1. Bir ortak alan veya özellik veri öğesi için projenizdeki ana bilgisayar öğesi sınıfının bir üyesi olarak gibi bildirin `ThisDocumen`Word projesindeki t sınıfı veya `ThisWorkbook` Excel projesinde sınıfı.

2. Uygulama <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute> veri öğesinin belgenin verilerini önbelleğinde depolanan işaretlemek için üye özniteliği. Aşağıdaki örnekte bu öznitelik için bir alan bildirimi için geçerlidir. bir <xref:System.Data.DataSet>.

     [!code-csharp[Trin_VstcoreDataExcel#11](../vsto/codesnippet/CSharp/Trin_VstcoreDataExcelCS/Sheet1.cs#11)]
     [!code-vb[Trin_VstcoreDataExcel#11](../vsto/codesnippet/VisualBasic/Trin_VstcoreDataExcelVB/Sheet1.vb#11)]

3. Veri öğesinin bir örneğini oluşturmak için kod ekleyin ve, varsa, veritabanından yükleyin.

     Veri öğesi, yalnızca ilk oluşturulduğunda yüklenir; Bundan sonra önbellek belgeyle kalır ve güncelleştirmek için diğer kod yazmanız gerekir.

### <a name="to-cache-a-dataset-in-the-document-by-using-the-properties-window"></a>Özellikler penceresini kullanarak bir veri kümesi belgedeki önbelleğe almak için

1. Örneğin, Visual Studio tasarımcısı araçları kullanarak projenize bir veri kaynağı ekleyerek kullanarak veri kümesini projeye ekleyin **veri kaynakları** penceresi.

2. Henüz yoksa ve örnek Tasarımcısı'nda seçerseniz veri kümesi örneği oluşturun.

3. İçinde **özellikleri** penceresinde **CacheInDocument** özelliğini **True**.

     Daha fazla bilgi için [Office projelerinde Özellikler](../vsto/properties-in-office-projects.md).

4. İçinde **özellikleri** penceresinde **değiştiriciler** özelliğini **genel** (Bu varsayılan **dahili**).

## <a name="see-also"></a>Ayrıca bkz.
- [Verileri önbelleğe](../vsto/caching-data.md)
- [Nasıl yapılır: Bir Office belgesi bir veri kaynağını programlamayla önbelleğe alma](../vsto/how-to-programmatically-cache-a-data-source-in-an-office-document.md)
- [Nasıl yapılır: Bir parola korumalı belgede veriyi önbelleğe alma](../vsto/how-to-cache-data-in-a-password-protected-document.md)
- [Sunucudaki belgelerde verilere](../vsto/accessing-data-in-documents-on-the-server.md)
- [Verileri kaydetme](../data-tools/saving-data.md)
