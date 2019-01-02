---
title: 'İzlenecek yol: Veri kümesi Tasarımcısı ile veri kümesi oluşturma'
ms.date: 09/11/2017
ms.topic: conceptual
helpviewer_keywords:
- datasets [Visual Basic], walkthroughs
- XML schemas, creating datasets
- data [Visual Studio], Dataset Designer
- Dataset Designer, walkthroughs
- datasets [Visual Basic], creating
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: e79646609bf592b7a8d71d3e0ba8660c65520715
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53868527"
---
# <a name="walkthrough-create-a-dataset-with-the-dataset-designer"></a>İzlenecek yol: Veri kümesi Tasarımcısı ile veri kümesi oluşturma

Bu kılavuzda kullanarak bir veri kümesi oluşturursunuz **veri kümesi Tasarımcısı**. Makaleyi yeni proje oluşturma ve yeni bir ekleme işleminde gereken **veri kümesi** ona öğesi. Sihirbaz kullanmadan bir veritabanındaki tabloları temel tablo oluşturulacağını öğreneceksiniz.

## <a name="prerequisites"></a>Önkoşullar

Bu izlenecek yol, SQL Server Express LocalDB ve Northwind örnek veritabanını kullanır.

1.  SQL Server Express LocalDB yoksa,'nden ya da yükleme [SQL Server Express indirme sayfası](https://www.microsoft.com/sql-server/sql-server-editions-express), aracılığıyla veya **Visual Studio yükleyicisi**. Visual Studio yükleyicisi, SQL Server Express LocalDB parçası olarak yüklenebilir **veri depolama ve işleme** iş yükü veya tek bir bileşen olarak.

2.  Northwind örnek veritabanı, şu adımları izleyerek yükleyin:

    1. Visual Studio'da açın **SQL Server Nesne Gezgini** penceresi. (Bir parçası olarak SQL Server Nesne Gezgini yüklü **veri depolama ve işleme** iş yükünü Visual Studio Yükleyicisi'nde.) Genişletin **SQL Server** düğümü. LocalDB Örneğinizde sağ tıklayıp **yeni sorgu**.

       Sorgu Düzenleyicisi penceresi açılır.

    2. Kopyalama [Northwind Transact-SQL betiği](https://github.com/MicrosoftDocs/visualstudio-docs/blob/master/docs/data-tools/samples/northwind.sql?raw=true) panonuza. Bu T-SQL betiği, sıfırdan Northwind veritabanı oluşturur ve verilerle doldurur.

    3. T-SQL betiği sorgu düzenleyiciye yapıştırın ve ardından **yürütme** düğmesi.

       Kısa bir süre sonra sorgu yürütülürken tamamlanır ve Northwind veritabanı oluşturulur.

## <a name="create-a-new-windows-forms-application-project"></a>Yeni bir Windows Forms uygulaması projesi oluşturma

1. Visual Studio'da üzerinde **dosya** menüsünde **yeni** > **proje**.

2. Ya da genişletin **Visual C#** veya **Visual Basic** seçip sol bölmedeki **Windows Masaüstü**.

3. Orta bölmede seçin **Windows Forms uygulaması** proje türü.

4. Projeyi adlandırın **DatasetDesignerWalkthrough**ve ardından **Tamam**.

     Visual Studio projeyi ekler **Çözüm Gezgini** ve yeni bir form Tasarımcısı'nda görüntüleyin.

## <a name="add-a-new-dataset-to-the-application"></a>Uygulamaya yeni bir veri kümesi ekleyin

1.  Üzerinde **proje** menüsünde **Yeni Öğe Ekle**.

     **Yeni Öğe Ekle** iletişim kutusu görünür.

2.  Sol bölmede seçin **veri**, ardından **veri kümesi** orta bölmesinde.

3.  Veri kümesi adı **NorthwindDataset**ve ardından **Ekle**.

     Visual Studio adlı bir dosya ekler **NorthwindDataset.xsd** projeye ve onu açar **veri kümesi Tasarımcısı**.

## <a name="create-a-data-connection-in-server-explorer"></a>Sunucu Gezgini'nde bir veri bağlantısı oluşturma

1.  Üzerinde **görünümü** menüsünü tıklatın **Sunucu Gezgini**.

2.  İçinde **Sunucu Gezgini**, tıklayın **veritabanına bağlan** düğmesi.

3.  Northwind örnek veritabanına bağlantı oluşturun.

## <a name="create-the-tables-in-the-dataset"></a>Dataset içinde tablolar oluşturmak

Bu bölümde, veri kümesi için tablo ekleme açıklanmaktadır.

### <a name="to-create-the-customers-table"></a>Müşteriler tablosu oluşturmak için

1.  Oluşturduğunuz veri bağlantısı genişletin **Sunucu Gezgini**ve ardından **tabloları** düğümü.

2.  Sürükleme **müşteriler** tablosunda **Sunucu Gezgini** üzerine **veri kümesi Tasarımcısı**.

     A **müşteriler** veri tablosu ve **CustomersTableAdapter** veri kümesine eklenir.

### <a name="to-create-the-orders-table"></a>Siparişler tablosu oluşturmak için

-   Sürükleme **siparişler** tablosunda **Sunucu Gezgini** üzerine **veri kümesi Tasarımcısı**.

     Bir **siparişler** veri tablosu **orderstableadapter bağdaştırıcısına**ve arasında veri ilişkisi **müşteriler** ve **siparişler** tabloları eklenir veri kümesi.

### <a name="to-create-the-orderdetails-table"></a>OrderDetails tablo oluşturmak için

-   Sürükleme **sipariş ayrıntıları** tablosunda **Sunucu Gezgini** üzerine **veri kümesi Tasarımcısı**.

     Bir **sipariş ayrıntıları** veri tablosu **OrderDetailsTableAdapter**ve arasında veri ilişkisi **siparişler** ve **OrderDetails** tabloları veri kümesine eklenir.

## <a name="next-steps"></a>Sonraki Adımlar

-   Veri kümesini kaydetme.

-   Öğe seçin **veri kaynakları** penceresi ve bunları formunuza sürükleyin. Daha fazla bilgi için [Visual Studio'da verilere Windows Forms bağlama denetimleri](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md).

-   Daha fazla sorgular için TableAdapter'ları ekleyin.

-   Doğrulama mantığı eklemenize <xref:System.Data.DataTable.ColumnChanging> veya <xref:System.Data.DataTable.RowChanging> veri kümesindeki veri tablolarının olayları. Daha fazla bilgi için [veri kümelerindeki verileri doğrulama](../data-tools/validate-data-in-datasets.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio’da veri kümeleri oluşturma ve yapılandırma](../data-tools/create-and-configure-datasets-in-visual-studio.md)
- [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Visual Studio'da verilere denetimler bağlama](../data-tools/bind-controls-to-data-in-visual-studio.md)
- [Verileri doğrulama](../data-tools/validate-data-in-datasets.md)