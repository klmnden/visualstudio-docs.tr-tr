---
title: XAML Tasarımcısı’nda verilere bağlama
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- VS.XamlDesigner.DataBinding
dev_langs:
- CSharp
- VB
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 58f83616985556d762ae05a0a97c6263e2e6d7a4
ms.sourcegitcommit: 90c3187d804ad7544367829d07ed4b47d3f8a72d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68821549"
---
# <a name="walkthrough-bind-to-data-in-xaml-designer"></a>İzlenecek yol: XAML Tasarımcısı’nda verilere bağlama

XAML Tasarımcısı, çalışma yüzeyini ve Özellikler penceresi kullanarak veri bağlama özelliklerini ayarlayabilirsiniz. Bu yönergedeki örnek, verileri bir denetime bağlamayı gösterir. Özellikle, izlenecek yol, `ItemCount`adlı bir [DependencyProperty](xref:Windows.UI.Xaml.DependencyProperty) 'yi içeren basit bir alışveriş sepeti sınıfının nasıl oluşturulacağını gösterir `ItemCount` ve sonra özelliği bir [TextBlock](xref:Windows.UI.Xaml.Controls.TextBlock) denetiminin **Text** özelliğine bağlar.

## <a name="to-create-a-class-to-use-as-a-data-source"></a>Veri kaynağı olarak kullanılacak bir sınıf oluşturmak için

1. Üzerinde **dosya** menüsünde seçin **yeni** > **proje**.

1. **Yeni proje** iletişim kutusunda, **Visual C#**  veya **Visual Basic** düğümünü seçin, **Windows Masaüstü** düğümünü genişletin ve ardından **WPF uygulama** şablonunu seçin.

1. Projeyi **BindingTest**olarak adlandırın ve **Tamam** düğmesini seçin.

1. **MainWindow.xaml.cs** (veya **MainWindow. xaml. vb**) dosyasını açın ve aşağıdaki kodu ekleyin. İçinde C#, kodu `BindingTest` ad alanına ekleyin (dosyadaki son kapanış parantezinden önce). Visual Basic ' de, yeni sınıfı eklemeniz yeterlidir.

   ```csharp
   public class ShoppingCart : DependencyObject
   {
       public int ItemCount
       {
           get { return (int)GetValue(ItemCountProperty); }
           set { SetValue(ItemCountProperty, value); }
       }

       public static readonly DependencyProperty ItemCountProperty =
            DependencyProperty.Register("ItemCount", typeof(int),
            typeof(ShoppingCart), new PropertyMetadata(0));
   }
   ```

   ```vb
   Public Class ShoppingCart
       Inherits DependencyObject

       Public Shared ReadOnly ItemCountProperty As DependencyProperty = DependencyProperty.Register(
            "ItemCount", GetType(Integer), GetType(ShoppingCart), New PropertyMetadata(0))
       Public Property ItemCount As Integer
           Get
               ItemCount = CType(GetValue(ItemCountProperty), Integer)
           End Get
           Set(value As Integer)
               SetValue(ItemCountProperty, value)
           End Set
       End Property
   End Class
   ```

   Bu kod, [PropertyMetadata](xref:Windows.UI.Xaml.PropertyMetadata) nesnesini kullanarak varsayılan öğe sayısı olarak 0 değerini ayarlar.

1. **Dosya** menüsünde Build**Build Solution**öğesini > seçin.

## <a name="to-bind-the-itemcount-property-to-a-textblock-control"></a>ItemCount özelliğini bir TextBlock denetimine bağlamak için

1. Çözüm Gezgini, **MainWindow. xaml** için kısayol menüsünü açın ve **Görünüm Tasarımcısı**' nı seçin.

1. Araç kutusunda bir [kılavuz](xref:Windows.UI.Xaml.Controls.Grid) denetimi seçin ve forma ekleyin.

1. Seçili olan Özellikler penceresi, **DataContext** özelliğinin yanındaki yeni düğmesini seçin. `Grid`

1. **Nesne Seç** iletişim kutusunda, **tüm derlemeleri göster** onay kutusunun temizlenmiş olduğundan emin olun, **BindingTest** ad alanı altında **ShoppingCart** ' i seçin ve **Tamam** düğmesini seçin.

     Aşağıdaki çizimde, **ShoppingCart** seçiliyken **nesne Seç** iletişim kutusu gösterilmektedir.

     ![Nesne Seç iletişim kutusu](../designers/media/blendselectobject.png)

1. **Araç kutusunda**, forma eklemek için `TextBlock` bir denetim seçin.

1. Denetim seçiliyken, Özellikler penceresi metin özelliğinin sağ tarafındaki özellik işaretini seçin ve sonra **veri bağlama oluştur**' u seçin. `TextBlock` (Özellik işaretçisi küçük bir kutu gibi görünür.)

1. Veri bağlamayı oluştur iletişim kutusunda, **yol** kutusunda, **ItemCount: (Int32)** özelliğini seçin ve sonra **Tamam** düğmesini seçin.

     Aşağıdaki çizimde, **ItemCount** özelliği seçili olan **veri bağlamayı oluştur** iletişim kutusu gösterilmektedir.

     ![Veri bağlama oluştur iletişim kutusu](../designers/media/xaml_create_data_binding.png)

1. Uygulamayı çalıştırmak için **F5** tuşuna basın.

     `TextBlock` Denetim, varsayılan değer olan 0 değerini metin olarak göstermelidir.

## <a name="see-also"></a>Ayrıca bkz.

- [XAML Tasarımcısı’nı kullanarak bir kullanıcı arabirimi oluşturma](../designers/creating-a-ui-by-using-xaml-designer-in-visual-studio.md)
- [Değer Dönüştürücüsü Ekle iletişim kutusu](https://msdn.microsoft.com/library/c5f3d110-a541-4b55-8bca-928f77778af8)