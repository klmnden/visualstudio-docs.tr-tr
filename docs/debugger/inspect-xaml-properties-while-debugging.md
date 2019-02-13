---
title: Hata ayıklama sırasında XAML özelliklerini denetleme | Microsoft Docs
ms.date: 03/06/2017
ms.topic: conceptual
ms.assetid: 390edde4-7b8d-4c89-8d69-55106b7e6b11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: d5b04a64ea75458d23e64e83a405a103ae70a100
ms.sourcegitcommit: 22b73c601f88c5c236fe81be7ba4f7f562406d75
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56227702"
---
# <a name="inspect-xaml-properties-while-debugging"></a>Hata ayıklama sırasında XAML özelliklerini denetleme
Çalışan XAML kodunuzu ile gerçek zamanlı bir görünümünü elde edebilirsiniz **Live Visual Tree** ve **Live Property Explorer**. Bu araçlar, çalışan XAML uygulamanızın kullanıcı Arabirimi öğelerini ağaç görünümünü sağlar ve seçtiğiniz herhangi bir kullanıcı Arabirimi öğesi çalışma zamanı özelliklerini göster.

Aşağıdaki yapılandırmaları bu araçları kullanabilirsiniz:

|Uygulama türü|İşletim sistemi ve araçları|
|-----------------|--------------------------------|
|Windows Presentation Foundation (4.0 ve üzeri) uygulamaları|Windows 7 ve üzeri|
|Evrensel Windows uygulamaları|Windows 10 ve üzeri ile [Windows 10 SDK'sı](https://dev.windows.com/en-us/downloads/windows-10-sdk)|

## <a name="looking-at-elements-in-the-live-visual-tree"></a>Öğeleri Canlı görsel ağaç bakarak
Bir liste görünümü ve bir düğme olan çok basit WPF uygulaması başlayalım. Düğmesini her zaman başka bir öğe listesine eklenir. Tek sayılı öğeleri gri renkte görünür ve öğeleri tek sayılı sarı renkte görünür.

Yeni bir C# WPF uygulaması (Dosya > Yeni > Proje, ardından C# ve WPF uygulaması bulabilirsiniz). Adlandırın **TestXAML**.

MainWindow.xaml şu şekilde değiştirin:

```xaml
<Window x:Class="TestXAML.MainWindow"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:local="clr-namespace:TestXAML"
    mc:Ignorable="d"
    Title="MainWindow" Height="350" Width="525">
    <Grid>
        <Button x:Name="button" Background="LightBlue" Content="Add Item" HorizontalAlignment="Left" Margin="216,206,0,0" VerticalAlignment="Top" Width="75" Click="button_Click"/>
        <ListBox x:Name="listBox" HorizontalAlignment="Left" Height="100" VerticalAlignment="Top" Width="100" Margin="205,80,0,0"/>
    </Grid>
</Window>
```

Aşağıdaki komut işleyici MainWindow.xaml.cs dosyasına ekleyin:

```csharp
int count;

private void button_Click(object sender, RoutedEventArgs e)
{
    ListBoxItem item = new ListBoxItem();
    item.Content = "Item" + ++count;
    if (count % 2 == 0)
    {
        item.Background = Brushes.LightGray;
    }
    else
    {
        item.Background = Brushes.LightYellow;
    }
    listBox.Items.Add(item);
}
```

Projeyi oluşturmak ve hata ayıklamaya başlayın. (Derleme yapılandırması hata ayıklama, yayın değil olmalıdır. Derleme yapılandırmaları hakkında daha fazla bilgi için bkz. [derleme yapılandırmalarını anlama](../ide/understanding-build-configurations.md).)

Pencere ortaya çıktığında tıklayın **Öğe Ekle** düğmesine birkaç kez. Bunun gibi bir şey görmeniz gerekir:

![Uygulamanın ana pencere](../debugger/media/livevisualtree-app.png "LiveVIsualTree uygulama")

Şimdi açmak **Live Visual Tree** penceresi (**hata ayıklama > Windows > Live Visual Tree**, veya IDE'nin sol tarafında bulabilirsiniz). Bu pencereyi baktığımızda şekilde yerleştirme konumuna uzağa sürükleyin ve **Canlı özellikleri** yan yana penceresi. İçinde **Live Visual Tree** penceresini genişletin **ContentPresenter** düğümü. Bu düğme ve liste kutusu için düğüm içermelidir. Liste kutusu genişletin (ardından **ScrollContentPresenter** ve **ItemsPresenter**) liste kutusu öğelerini bulmak için. Pencerenin şu şekilde görünmelidir:

![Canlı görsel ağaç ListBoxItems](../debugger/media/livevisualtree-listboxitems.png "LiveVisualTree ListBoxItems")

Uygulama penceresine dönün ve birkaç daha fazla öğe ekleyin. Daha fazla liste kutusu öğeleri görünür görmelisiniz **Live Visual Tree**.

Şimdi bir liste kutusu öğelerini özelliklerine göz atalım. İlk liste kutusu öğesini seçmek **Live Visual Tree** tıklatıp **özellikleri göster** araç çubuğundaki simgeye. **Live Property Explorer** görünmelidir. Unutmayın **içerik** "Item1" bir alandır ve **arka plan** alandır **#FFFFFFE0** (Açık Sarı). Geri Git **Live Visual Tree** ve ikinci liste kutusu öğesini seçin. **Live Property Explorer** göstermesi gerekir **içerik** "Item2" bir alandır ve **arka plan** alandır **#FFD3D3D3** (açık gri ).

Çok ilgi doğrudan büyük olasılıkla öğelerin XAML gerçek yapısını içerir ve kod iyi bilmiyorsanız, aradığınızı bulmak için ağacı gezinme sabit bir zaman olabilir. Bu nedenle **Live Visual Tree** incelemek istediğiniz öğe bulmanıza yardımcı olmak için uygulamanın UI kullandığınız olanak sağlayan birkaç yolu vardır.

**Çalışan uygulamada Seçimi Etkinleştir**. En soldaki düğme seçtiğinizde bu modu etkinleştirebilirsiniz **Live Visual Tree** araç çubuğu. Bu moduyla uygulamada, bir kullanıcı Arabirimi öğesi seçebilirsiniz ve **Live Visual Tree** (ve **Canlı özellik Görüntüleyici**) o öğeye karşılık gelen ağaç düğümü göstermek için otomatik olarak güncelleştirir. ve özellikleri.

**Çalışan uygulamada Düzen donatıcılarını görüntüleyin**. Etkin seçim düğmesi sağda hemen düğmesini seçtiğinizde, bu modu etkinleştirebilirsiniz. Zaman **Düzen donatıcılarını görüntüleyin** açıktır, uygulama penceresinin yatay ve dikey çizgileri seçili nesnenin sınırları boyunca neler bunu, kenar boşlukları gösteren dikdörtgenler yanı sıra hizalar görebilmeniz göstermek neden olur. Örneğin, her ikisini de etkinleştirmek **Seçimi Etkinleştir** ve **görünen Düzen** açık ve select **Öğe Ekle** uygulamada metin bloğu. Metin bloğu düğümü görmelisiniz **Canlı görsel ağaç** ve metin engelleme özellikleri **Canlı özellik Görüntüleyici**, yatay ve dikey metin bloğu sınırlarının satırlarda yanı sıra.

![LivePropertyViewer DisplayLayout içinde](../debugger/media/livevisualtreelivepropertyviewer-displaylayout.png "LiveVisualTreeLivePropertyViewer DisplayLayout")

**Önizleme seçimi**. Live Visual Tree araç soldaki alan üçüncü düğmeye seçerek bu modu etkinleştirebilirsiniz. Bu mod, uygulamanın kaynak koduna erişiminiz varsa öğe nerede bildirildi, XAML gösterir. Seçin **etkinleştirme seçimi** ve **Önizleme seçimi**, ve ardından test uygulamamız düğmesini seçin. MainWindow.xaml dosyasını Visual Studio'da açılır ve imleç düğmenin tanımlandığı satıra yerleştirilir.

## <a name="using-xaml-tools-with-running-applications"></a>Çalışan uygulamalar ile XAML araçlarını kullanma
Kaynak kodu yoksa olsa bile bu XAML araçları kullanabilirsiniz. Çalışan bir XAML uygulamaya ekleme yaptığınızda, kullanabileceğiniz **Live Visual Tree** uygulama UI öğeleri üzerinde çok. Önce kullandığımız WPF test uygulaması kullanarak, bir örnek aşağıda verilmiştir.

1. Başlangıç **TestXaml** sürüm yapılandırmasını uygulama. İçinde çalışan bir işleme iliştirilemiyor bir **hata ayıklama** yapılandırma.

2. Visual Studio ikinci bir örneğini açın ve tıklayın **hata ayıklama > iliştirme**. Bulma **TestXaml.exe** kullanılabilir işlemler seçeneğine tıklayıp listesinde **iliştirme**.

3. Uygulama çalışmaya başlar.

4. Visual Studio'nun ikinci örnekte, Aç **Live Visual Tree** (**hata ayıklama > Windows > Live Visual Tree**). Görmelisiniz **TestXaml** kullanıcı Arabirimi öğeleri ve olmalıdır uygulama doğrudan hata ayıklarken gibi bunları yönetmek kullanabilirsiniz.
