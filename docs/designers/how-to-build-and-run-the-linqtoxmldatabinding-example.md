---
title: 'Nasıl yapılır: LinqToXmlDataBinding Örneğini Derleme ve Çalıştırma'
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d53f8d08222eb35660f7a4454164d6b821a976d9
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66714840"
---
# <a name="how-to-build-and-run-the-linqtoxmldatabinding-example"></a>Nasıl yapılır: LinqToXmlDataBinding oluşturma ve çalıştırma örneği

Bu konu nasıl oluşturulup LinqToXmlDataBinding Visual Studio projeyi oluşturun ve elde edilen LinqToXmlDataBinding Windows Presentation Foundation (WPF) örnek program çalıştırma gösterir.

Visual Studio hakkında daha fazla bilgi için bkz. [Visual Studio IDE'ye genel bakış](../get-started/visual-studio-ide.md).

## <a name="create-the-project"></a>Projeyi oluşturma

1. Visual Studio'yu açın ve oluşturma bir C# **WPF uygulaması** adlı **LinqToXmlDataBinding**.

   Projenin .NET Framework 3.5 (veya sonraki sürümler) hedeflemesi.

1. Aksi halde aşağıdaki .NET derlemeleri için zaten mevcut proje başvurularını ekleyin:

    - System.Data

    - System.Data.DataSetExtensions

    - System.Xml

    - System.Xml.Linq

1. Basarak çözümü oluşturun **Ctrl**+**Shift**+**B**, çalıştırın tuşlarına basarak **F5**. Projenin hatasız derleyip genel WPF uygulaması çalıştırın.

## <a name="add-code-to-the-project"></a>Proje için kod ekleyin

1. İçinde **Çözüm Gezgini**, kaynak dosyayı yeniden adlandır **gt;Window1.XAML** için **L2XDBForm.xaml**. Bağımlı kaynak dosyası **Window1.xaml.cs** için otomatik olarak adlandırılmamalıdır **L2XDBForm.xaml.cs**.

1. Kaynak kodu dosyasında bulunan Değiştir **L2XDBForm.xaml** konusunun kod ile [L2DBForm.xaml kaynak kodu](../designers/l2dbform-xaml-source-code.md). Bu dosyayla çalışmak için XAML kaynak görünümünü kullanın.

1. Benzer şekilde, kaynak değiştirin **L2XDBForm.xaml.cs** bulunan kodla [L2DBForm.xaml.cs kaynak kodu](../designers/l2dbform-xaml-cs-source-code.md).

1. Dosyasındaki **App.xaml**, dizenin tüm oluşumları değiştirmek `Window1.xaml` ile `L2XDBForm.xaml`.

1. **Ctrl**+**Shift**+**B** tuşlarına basarak çözümü oluşturun.

## <a name="run-the-program"></a>Programı çalıştırma

LinqToXmlDataBinding program görüntülemek ve gömülü bir XML öğesi olarak depolanan kitap listesi işlemek kullanıcının sağlar.

### <a name="to-run-the-program-and-view-the-book-list"></a>Programı çalıştırın ve kitap listesi görüntülemek için

LinqToXmlDataBinding basarak çalıştırın **F5** (**hata ayıklamayı Başlat**) veya **Ctrl**+**F5** (**Başlat Hata ayıklama olmadan**). Başlık program penceresiyle **LINQ to XML kullanarak WPF verilerini bağlama** görünür.

- Dosyanın üst kısmında ham görüntüler UI fark **XML** temsil eden kitap listesi. WPF kullanarak görüntülenir <xref:System.Windows.Controls.TextBlock> denetimi, klavye ve fare aracılığıyla etkileşim etkinleştirmez.

- Etiketli ikinci dikey bölümde **kitap listesi**, görüntüler books düz metin olarak sıralı listesi. Bunu kullanan bir <xref:System.Windows.Controls.ListBox> klavye ve fare seçimi ancak etkinleştiren denetimi.

### <a name="to-add-and-delete-books-from-the-list"></a>Ekleme ve Kitaplar listeden silme

- Yeni bir kitap listeye eklemek için değerlerini girin. **kimliği** ve **değeri** <xref:System.Windows.Controls.TextBox> son bölümüne denetimler **yeni kitabı ekleme**,'a tıklayın **Ekle Kitap** düğmesi. Not Defteri kitap ve XML listelerini listesine eklenir. Bu program, giriş değerleri doğrulamaz.

- Mevcut bir kitap listeden silmek için onu seçip **kitap listesi** bölümünde'a tıklayın **seçili kitap kaldırmak** düğmesi. Kitap hem ham XML kaynak listelerini defteri girdisi kaldırıldı dikkat edin.

### <a name="to-edit-an-existing-book-entry"></a>Bir kitap girişi düzenlemek için

1. İkinci defteri girdisini seçin **kitap listesi** bölümü. Geçerli değerleri üçüncü bölümünde görüntülenip **seçili kitap Düzenle**.

1. Klavyeyi kullanarak değerleri düzenleyin. Kapanmaz <xref:System.Windows.Controls.TextBox> denetim odağı kaybettiğinde, değişiklikleri otomatik olarak XML kaynak ve kitap listelerini yayılır.

## <a name="see-also"></a>Ayrıca bkz.

- [LINQ, XML örneği kullanarak WPF verilerini bağlama](../designers/wpf-data-binding-using-linq-to-xml-example.md)
- [İzlenecek yol: LinqToXmlDataBinding örneği](../designers/walkthrough-linqtoxmldatabinding-example.md)
- [Visual Studio IDE'ye genel bakış](../get-started/visual-studio-ide.md)