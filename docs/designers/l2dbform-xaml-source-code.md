---
title: L2DBForm.XAML kaynak kodu
ms.date: 11/04/2016
ms.topic: sample
ms.assetid: 624e96d4-6d27-4195-8ac2-2f3835f6c57e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b650c65eb81fb087b7783b41065445e1bbea20a0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62844261"
---
# <a name="l2dbformxaml-source-code"></a>L2DBForm.xaml kaynak kodu

Bu konu, içerir ve XAML kaynak dosyasını açıklar [LINQ, XML örneği kullanarak WPF verilerini bağlama](../designers/wpf-data-binding-using-linq-to-xml-example.md), *L2DBForm.xaml*.

## <a name="overall-ui-structure"></a>Genel kullanıcı Arabirimi yapısı

Bir WPF projesi için tipik olan bir üst öğesi, bu dosyayı içeren bir <xref:System.Windows.Window> türetilmiş sınıfla ilişkili XML öğesi `L2XDBFrom` içinde `LinqToXmlDataBinding` ad alanı.

İstemci alanı içinde yer alan bir <xref:System.Windows.Controls.StackPanel> açık mavi bir arka plan verilir. Bu panelde dört içeren <xref:System.Windows.Controls.DockPanel> UI bölümlere ayırarak <xref:System.Windows.Controls.Separator> çubukları. Bu bölümler amacı açıklanan **açıklamalar** içinde [önceki konu](../designers/walkthrough-linqtoxmldatabinding-example.md).

Her bölüm onu tanımlayan bir etiket içerir. İlk iki bölümde, bu etiketi 90 derece kullanımının döndürülür. bir <xref:System.Windows.FrameworkElement.LayoutTransform%2A>. Bölümün geri kalanında bu bölümün amacı için uygun kullanıcı Arabirimi öğeleri içerir: metin bloklarını, metin kutularını, düğmeleri ve benzeri. Bazen bir alt <xref:System.Windows.Controls.StackPanel> bu alt denetimler hizalamak için kullanılır.

## <a name="window-resource-section"></a>Pencere kaynak bölümü

Açılış `<Window.Resources>` 9 etiket penceresi kaynak bölümü başlangıcını gösterir. Kapanış etiketinin satırında 35 ile sona erer.

`<ObjectDataProvider>` Satırları 11 25 üzerinden yayılan, etiket bildirir bir <xref:System.Windows.Data.ObjectDataProvider>, adlandırılmış `LoadedBooks`, kullanan bir <xref:System.Xml.Linq.XElement> kaynağı olarak. <xref:System.Xml.Linq.XElement> Gömülü bir XML belgesi ayrıştırma tarafından başlatılır (bir `CDATA` öğesi). Gömülü bir XML belgesi bildirirken bu boşluk korunur dikkat edin ve ayrıca, bu ayrıştırılır. Boşluk, çünkü korunur <xref:System.Windows.Controls.TextBlock> ham XML görüntülemek için kullanılan denetime sahip hiçbir özel XML özellikleri biçimlendirme.

Son olarak, bir <xref:System.Windows.DataTemplate> adlı `BookTemplate` satırlarında 28 34 aracılığıyla tanımlanır. Bu şablon girişleri görüntülemek için kullanılan **kitap listesi** UI bölümü. Veri bağlama ve LINQ için XML dinamik özellikleri aracılığıyla aşağıdaki kitap adı ve kitap Kimliği almak için kullanır:

```xaml
Text="{Binding Path=Attribute[id].Value}"Text="{Binding Path=Value}"
```

## <a name="data-binding-code"></a>Veri bağlama kodu

Ek olarak <xref:System.Windows.DataTemplate> öğesi, veri bağlama, bu dosyadaki diğer yerler, çeşitli kullanılır.

Açılışında `<StackPanel>` satıra 38, etiket <xref:System.Windows.FrameworkElement.DataContext%2A> özelliği bu panelin `LoadedBooks` veri sağlayıcısı.

```xaml
DataContext="{Binding Source={StaticResource LoadedBooks}}
```

Veri bağlamını ayarlayarak mümkün kılar (satırında, 46) için <xref:System.Windows.Controls.TextBlock> adlı `tbRawXml` bağlayarak bu veri sağlayıcısının ham XML görüntülenecek `Xml` özelliği:

```xaml
Text="{Binding Path=Xml}"
```

<xref:System.Windows.Controls.ListBox> İçinde **kitap listesi** UI bölümünde, 58 62 aracılığıyla satırlarındaki ayarlar görünen öğelerinden şablonu `BookTemplate` penceresi kaynak bölümünde tanımlanan:

```xaml
ItemTemplate ="{StaticResource BookTemplate}"
```

Ardından, satırlara 62 59 books gerçek değerleri bu liste kutusuna bağlıdır:

```xaml
<ListBox.ItemsSource>
    <Binding Path="Elements[{http://www.mybooks.com}book]"/>
</ListBox.ItemsSource>
```

Üçüncü UI bölüm **Düzenle seçili kitap**, ilk bağlar <xref:System.Windows.FrameworkElement.DataContext%2A> üst <xref:System.Windows.Controls.StackPanel> için şu anda seçili öğesinde **kitap listesi** UI bölümü (satır 82):

```xaml
DataContext="{Binding ElementName=lbBooks, Path=SelectedItem}"
```

Kitap öğelerinin geçerli değerlerini görüntülenir ve, iki metin kutusuna bu bölmedeki güncelleştirildi çift yönlü veri bağlama, ardından kullanır. Kullanılan veri bağlama için veri bağlama dinamik özellikleri benzer `BookTemplate` veri şablonu:

```xaml
Text="{Binding Path=Attribute[id].Value}"...Text="{Binding Path=Value}"
```

Son kullanıcı Arabirimi bölümüne **ekleme yeni kitabı**, veri bağlama, XAML kodu kullanmaz. Bunun yerine, veri bağlama, olay kodu dosyasında işleme bulunduğu *L2DBForm.xaml.cs*.

## <a name="example"></a>Örnek

### <a name="description"></a>Açıklama

> [!NOTE]
> Satır numaralarını izlemek daha kolay olacaktır, böylece C# kaynak kod Düzenleyicisi'nde Visual Studio gibi bir kod düzenleyicisi altına aşağıdaki kodu kopyalayın öneririz.

### <a name="code"></a>Kod

```xml
<Window x:Class="LinqToXmlDataBinding.L2XDBForm"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:system="clr-namespace:System;assembly=mscorlib"
    xmlns:xlinq="clr-namespace:System.Xml.Linq;assembly=System.Xml.Linq"
    xmlns:local="clr-namespace:LinqToXmlDataBinding"
    Title="WPF Data Binding using LINQ-to-XML" Height="665" Width="500" ResizeMode="NoResize">

    <Window.Resources>
        <!-- Books provider and inline data -->
        <ObjectDataProvider x:Key="LoadedBooks" ObjectType="{x:Type xlinq:XElement}" MethodName="Parse">
            <ObjectDataProvider.MethodParameters>
                <system:String xml:space="preserve">
<![CDATA[
<books xmlns="http://www.mybooks.com">
  <book id="0">book zero</book>
  <book id="1">book one</book>
  <book id="2">book two</book>
  <book id="3">book three</book>
</books>
]]>
                </system:String>
                <xlinq:LoadOptions>PreserveWhitespace</xlinq:LoadOptions>
            </ObjectDataProvider.MethodParameters>
        </ObjectDataProvider>

        <!-- Template for use in Books List listbox. -->
        <DataTemplate x:Key="BookTemplate">
            <StackPanel Orientation="Horizontal">
                <TextBlock Margin="3" Text="{Binding Path=Attribute[id].Value}"/>
                <TextBlock Margin="3" Text="-"/>
                <TextBlock Margin="3" Text="{Binding Path=Value}"/>
            </StackPanel>
        </DataTemplate>
    </Window.Resources>

    <!-- Main visual content container -->
    <StackPanel Background="lightblue" DataContext="{Binding Source={StaticResource LoadedBooks}}">
        <!-- Raw XML display section -->
        <DockPanel Margin="5">
            <Label  Background="Gray" FontSize="12" BorderBrush="Black" BorderThickness="1" FontWeight="Bold">XML
            <Label.LayoutTransform>
                <RotateTransform Angle="90"/>
            </Label.LayoutTransform>
            </Label>
            <TextBlock Name="tbRawXml" Height="200" Background="LightGray" Text="{Binding Path=Xml}" TextTrimming="CharacterEllipsis" />
        </DockPanel>

        <Separator Height="4" Margin="5" />

        <!-- List box to display all books section -->
        <DockPanel Margin="5">
            <Label  Background="Gray" FontSize="12" BorderBrush="Black" BorderThickness="1" FontWeight="Bold">Book List
                <Label.LayoutTransform>
                    <RotateTransform Angle="90"/>
                </Label.LayoutTransform>
            </Label>
            <ListBox Name="lbBooks" Height="200" Width="415" ItemTemplate ="{StaticResource BookTemplate}">
                <ListBox.ItemsSource>
                    <Binding Path="Elements[{http://www.mybooks.com}book]"/>
                </ListBox.ItemsSource>
            </ListBox>
            <Button Margin="5" DockPanel.Dock="Right" Height="30" Width ="130" Content="Remove Selected Book" Click="OnRemoveBook">
            <Button.LayoutTransform>
                <RotateTransform Angle="90"/>
            </Button.LayoutTransform>
            </Button>
        </DockPanel>

        <Separator Height="4" Margin="5" />

        <!-- Edit current selection section -->
        <DockPanel Margin="5">
            <TextBlock Margin="5" Height="30" Width="65" DockPanel.Dock="Right" Background="LightGray" TextWrapping="Wrap" TextAlignment="Center">
                    Changes are live!
                <TextBlock.LayoutTransform>
                    <RotateTransform Angle="90"/>
                </TextBlock.LayoutTransform>
            </TextBlock>
            <StackPanel>
                <Label Width="450" Background="Gray" FontSize="12" BorderBrush="Black" BorderThickness="1" HorizontalAlignment="Left" FontWeight="Bold">Edit Selected Book</Label>
                <StackPanel Margin="1" DataContext="{Binding ElementName=lbBooks, Path=SelectedItem}">
                    <StackPanel Orientation="Horizontal">
                        <Label Width="40">ID:</Label>
                        <TextBox Name="editAttributeTextBox" Width="410" Text="{Binding Path=Attribute[id].Value}">
                            <TextBox.ToolTip>
                                <TextBlock FontWeight="Bold" TextAlignment="Center">
                                    <Label>Edit the selected book ID and see it changed.</Label>
                                </TextBlock>
                            </TextBox.ToolTip>
                        </TextBox>
                    </StackPanel>
                    <StackPanel Orientation="Horizontal">
                        <Label Width="40">Value:</Label>
                        <TextBox Name="editValueTextBox" Width="410" Text="{Binding Path=Value}" Height="25">
                            <TextBox.ToolTip>
                                <TextBlock FontWeight="Bold" TextAlignment="Center">
                                    <Label>Edit the selected book Value and see it changed.</Label>
                                </TextBlock>
                            </TextBox.ToolTip>
                        </TextBox>
                    </StackPanel>
                </StackPanel>
            </StackPanel>
        </DockPanel>

        <Separator Height="4" Margin="5" />

        <!-- Add new book section -->
        <DockPanel Margin="5">
            <Button Margin="5" Height="30" DockPanel.Dock="Right" Click ="OnAddBook">Add Book
                <Button.LayoutTransform>
                    <RotateTransform Angle="90"/>
                </Button.LayoutTransform>
            </Button>
            <StackPanel>
                <Label Width="450" Background="Gray" FontSize="12" BorderBrush="Black" BorderThickness="1" HorizontalAlignment="Left" FontWeight="Bold">Add New Book</Label>
                <StackPanel Margin="1">
                    <StackPanel Orientation="Horizontal">
                        <Label Width="40">ID:</Label>
                        <TextBox Name="tbAddID" Width="410">
                            <TextBox.ToolTip>
                                <TextBlock FontWeight="Bold" TextAlignment="Center">
                                    <Label>Enter a book ID and Value pair, then click Add Book.</Label>
                                </TextBlock>
                            </TextBox.ToolTip>
                        </TextBox>
                    </StackPanel>
                    <StackPanel Orientation="Horizontal">
                        <Label Width="40">Value:</Label>
                        <TextBox Name="tbAddValue" Width="410" Height="25">
                            <TextBox.ToolTip>
                                <TextBlock FontWeight="UltraBold" TextAlignment="Center">
                                    <Label>Enter a book ID and Value pair, then click Add Book.</Label>
                                </TextBlock>
                            </TextBox.ToolTip>
                        </TextBox>
                    </StackPanel>
                </StackPanel>
            </StackPanel>
        </DockPanel>
    </StackPanel>
</Window>
```

### <a name="comments"></a>Açıklamalar

C# kaynak kodu için bir WPF UI öğeleriyle ilişkili olay işleyicileri için bkz: [L2DBForm.xaml.cs kaynak kodu](../designers/l2dbform-xaml-cs-source-code.md).

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: LinqToXmlDataBinding örneği](../designers/walkthrough-linqtoxmldatabinding-example.md)
- [L2DBForm.xaml.cs kaynak kodu](../designers/l2dbform-xaml-cs-source-code.md)