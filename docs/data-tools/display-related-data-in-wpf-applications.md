---
title: WPF uygulamalarında ilgili verileri görüntüleme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- data [WPF], displaying
- WPF, data binding in Visual Studio
- WPF data binding [Visual Studio]
- displaying data, WPF
- WPF [WPF], data
- WPF Designer, data binding
- data binding, WPF
ms.assetid: 3aa80194-0191-474d-9d28-5ec05654b426
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 2fe1a41792aa6712f61b2d034cac75528108a722
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940901"
---
# <a name="display-related-data-in-wpf-applications"></a>WPF uygulamalarında ilgili verileri görüntüleme

Bazı uygulamalarda, birden fazla tablodan ya da birbirlerine bir üst-alt ilişkisinde ilgili varlıkları gelen verilerle çalışmak isteyebilirsiniz. Örneğin, müşterileri gösteren bir kılavuz görüntülemek isteyebilirsiniz bir `Customers` tablo. Kullanıcı belirli bir müşteri seçtiğinde, o müşterinin ilgili siparişlerini başka bir kılavuz görüntüler `Orders` tablo.

Öğeleri sürükleyerek ilgili verileri görüntüleyen verilere bağlı denetimler oluşturabilirsiniz **veri kaynakları** penceresinden WPF tasarımcısına.

## <a name="to-create-controls-that-display-related-records"></a>İlişkili kayıtları görüntüleyecek denetimler oluşturmak için

1. Üzerinde **veri** menüsünde tıklatın **veri kaynaklarını Göster** açmak için **veri kaynakları** penceresi.

2. Tıklayın **yeni veri kaynağı Ekle**ve tamamlayın **veri kaynağı yapılandırması** Sihirbazı.

3. WPF Tasarımcısı'nı açın ve tasarımcı geçerli bırakma hedefi öğeleri için bir kapsayıcı içerdiğinden emin olun **veri kaynakları** penceresi.

     Geçerli bırakma hedefleri hakkında daha fazla bilgi için bkz. [Visual Studio'da veri bağlama WPF denetimleri](../data-tools/bind-wpf-controls-to-data-in-visual-studio.md).

4. İçinde **veri kaynakları** penceresi, üst tablo temsil eden düğümü genişletin veya ilişkide nesne. Üst tablo veya nesne "bir" bir-çok ilişkisi tarafında ' dir.

5. Üst düğümün (veya üst düğümündeki tek tek öğeleri) sürükleyin **veri kaynakları** penceresinden Tasarımcısı'nda bir geçerli bırakma hedefi.

     Visual Studio sürüklediğiniz her öğe için yeni verilere bağlı denetimler oluşturan XAML oluşturur. XAML ayrıca yeni bir ekler <xref:System.Windows.Data.CollectionViewSource> üst tablo veya bırakma hedefi kaynaklarına nesnesi. Bazı veri kaynakları için Visual Studio ayrıca üst tablo veya nesne verileri yüklemek için kod oluşturur. Daha fazla bilgi için [Visual Studio'da veri bağlama WPF denetimleri](../data-tools/bind-wpf-controls-to-data-in-visual-studio.md).

6. İçinde **veri kaynakları** penceresinde ilgili alt tablo veya nesne bulun. İlgili alt tablolar ve nesneler verileri üst düğümün listesinin altındaki Genişletilebilir düğümleri olarak görünür.

7. Alt düğüm (ya da alt düğümünde tek tek öğeleri) sürükleyin **veri kaynakları** penceresinden Tasarımcısı'nda bir geçerli bırakma hedefi.

     Visual Studio her sürüklediğiniz öğeleri için yeni verilere bağlı denetimler oluşturan XAML oluşturur. XAML ayrıca yeni bir ekler <xref:System.Windows.Data.CollectionViewSource> alt tablo veya bırakma hedefi kaynaklarına nesnesi. Bu yeni <xref:System.Windows.Data.CollectionViewSource> üst tablo ya da yalnızca tasarımcıya sürüklediğiniz nesnesinin bir özelliğine bağlıdır. Bazı veri kaynakları için Visual Studio ayrıca alt tablo veya nesne verileri yüklemek için kod oluşturur.

     Aşağıdaki şekilde ilgili gösterir **siparişler** tablosu **müşteriler** bir veri tablosunda **veri kaynakları** penceresi.

     ![Veri kaynakları penceresi gösteren ilişki](../data-tools/media/datasources2.gif)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da verilere WPF denetimleri bağlama](../data-tools/bind-wpf-controls-to-data-in-visual-studio.md)
- [WPF uygulamalarında arama tabloları oluşturma](../data-tools/create-lookup-tables-in-wpf-applications.md)