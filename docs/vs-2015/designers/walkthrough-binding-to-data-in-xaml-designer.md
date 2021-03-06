---
title: "İzlenecek yol: XAML Tasarımcısı'nda verilere bağlama | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-designers
ms.topic: conceptual
f1_keywords:
- VS.XamlDesigner.DataBinding
ms.assetid: 1a99aeae-c3ef-407d-ba79-b8055489a43d
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c839350dd37f71d4f3368e077f4d9afe1b2bb2f4
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65701955"
---
# <a name="walkthrough-binding-to-data-in-xaml-designer"></a>İzlenecek yol: XAML Tasarımcısı'nda verilere bağlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XAML Tasarımcısı'nda, çalışma yüzeyine ve Özellikler penceresini kullanarak veri bağlama özellikleri ayarlayabilirsiniz. Bu kılavuzda örnek veriyi denetime bağlama gösterilmektedir. Özellikle, gözden geçirme sahip basit bir alışveriş sepeti sınıfı oluşturma işlemini gösterir ve bir [DependencyProperty](https://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.dependencyproperty.aspx) adlı `ItemCount`ve ardından `ItemCount` özelliğini **metin** özelliği bir [TextBlock](https://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.controls.textblock.aspx) denetimi.  
  
### <a name="to-create-a-class-to-use-as-a-data-source"></a>Veri kaynağı olarak kullanılacak bir sınıf oluşturmak için  
  
1. Üzerinde **dosya** menüsünde seçin **yeni**, **proje**.  
  
2. İçinde **yeni proje** iletişim kutusunda, ya da **Visual C#** veya **Visual Basic** düğümünü genişletin **Windows Masaüstü** düğümünü ve ardından seçin **WPF uygulaması** şablonu.  
  
3. Projeyi adlandırın **BindingTest**ve ardından **Tamam** düğmesi.  
  
4. MainWindow.xaml.cs (veya MainWindow.xaml.vb) dosyasını açın ve aşağıdaki kodu ekleyin. C# kodu ekleyin `BindingTest` ad alanı (önce dosyanın son kapatma parantezi). Visual Basic'te, yalnızca yeni bir sınıf ekleyin.  
  
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
  
     Bu kod, kullanarak varsayılan öğe sayısı 0 değerini ayarlar [PropertyMetadata](https://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.propertymetadata.aspx) nesne.  
  
5. Üzerinde **dosya** menüsünde seçin **derleme**, **Çözümü Derle**.  
  
### <a name="to-bind-the-itemcount-property-to-a-textblock-control"></a>Bir TextBlock denetimi ItemCount özelliği bağlamak için  
  
1. Çözüm Gezgini içinde MainWindow.xaml için kısayol menüsünü açın ve seçin **Görünüm Tasarımcısı**.  
  
2. Araç kutusunda seçin bir [kılavuz](https://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.controls.grid.aspx) denetlemek ve forma ekleyin.  
  
3. İle `Grid` seçiliyken, Özellikler penceresinde **yeni** düğmesinin yanındaki **DataContext** özelliği.  
  
4. İçinde **Nesne Seç** iletişim kutusunda, emin **tüm derlemeleri Göster** onay kutusu işaretli değilse, seçin **ShoppingCart** altında **BindingTest** ad alanını seçip **Tamam** düğmesi.  
  
     Aşağıdaki çizimde gösterildiği **Nesne Seç** iletişim kutusuyla **ShoppingCart** seçili.  
  
     ![Nesne Seç iletişim kutusu](../designers/media/blendselectobject.PNG "BlendSelectObject")  
  
5. İçinde **araç kutusu**, seçin bir `TextBlock` eklemek için form denetimi.  
  
6. İle `TextBlock` denetimi, Özellikler penceresinde, seçili özellik işaretçisi sağındaki seçin **metin** özelliği ve ardından **veri bağlama oluşturun**. (Özellik işaretçisi küçük bir kutu gibi görünüyor.)  
  
7. İletişim kutusu, bağlama Oluştur Veri **yolu** kutusunda **ItemCount: (int32)** özelliği seçip **Tamam** düğmesi.  
  
     Aşağıdaki çizimde gösterildiği **veri bağlama oluşturun** iletişim kutusuyla **ItemCount** seçili özellik.  
  
     ![Oluştur iletişim kutusu veri bağlama](../designers/media/xaml-create-data-binding.png "xaml_create_data_binding")  
  
8. Uygulamayı çalıştırmak için F5'e basın.  
  
     `TextBlock` Denetim 0 varsayılan değerini metin olarak göstermelidir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XAML Tasarımcısı'nı kullanarak kullanıcı Arabirimi oluşturma](../designers/creating-a-ui-by-using-xaml-designer-in-visual-studio.md)   
 [NIB: Değer dönüştürücüsü iletişim kutusu Ekle](https://msdn.microsoft.com/c5f3d110-a541-4b55-8bca-928f77778af8)
