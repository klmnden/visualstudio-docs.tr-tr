---
title: 'İzlenecek yol: Başlangıç sayfasına özel XAML ekleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- custom start page
- xaml start page
ms.assetid: 9af4d5f9-1cfc-4221-aea7-c8cd3f7571a6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
monikerRange: vs-2017
ms.openlocfilehash: 543faf9cf122e77cce6242f95008b777cd5666b2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322773"
---
# <a name="walkthrough-add-custom-xaml-to-the-start-page"></a>İzlenecek yol: Başlangıç sayfasına özel XAML ekleme

Bu izlenecek yol, bir Web tarayıcısı içeren özel bir Visual Studio Başlangıç sayfası oluşturma işlemi gösterilmektedir.

## <a name="add-custom-xaml"></a>Özel XAML ekleme

1. Başlangıç Sayfası'ndaki yönergeleri takip ederek oluşturma [özel başlangıç sayfası oluşturma](../extensibility/creating-a-custom-start-page.md).

2. İçinde *MainWindow.xaml* dosya, bulma \<kılavuz > bölümü.

3. Ekleme bir \<TabControl > öğesi ve bir \<TabItem > içinde \< kılavuz > öğesi, aşağıdaki örnekte gösterildiği gibi.

    ```xml
    <Grid>
        <TabControl>
            <TabItem Header="Bing" Height="Auto">
                <Frame Source="http://www.bing.com" />
            </TabItem>
        </TabControl>
    </Grid>
    ```

4. İkinci bir ekleme \<TabItem >, ile bir \<düğmesi > Yeni bir proje açılır öğe:

    ```xml
    <Grid>
        <TabControl>
            <TabItem Header="MyButton" Height="Auto">
                <Button Name="btnNewProj" Content="New Project"
                    Command="{x:Static vscom:VSCommands.ExecuteCommand}"
                    CommandParameter="File.NewProject" >
                </Button>
            </TabItem>
            <TabItem Header="Bing" Height="Auto">
                <Frame Source="http://www.bing.com" />
            </TabItem>
        </TabControl>
    </Grid>
    ```

## <a name="test-the-custom-start-page"></a>Özel başlangıç sayfasını test etme

1. Tuşuna **F5**.

     Visual Studio'nun deneysel örneğinde yüklü ancak seçili özel başlangıç sayfası ile açılır.

2. Visual Studio'nun deneysel örneğinde açın **araçları/Options / ortam** sayfası.

3. Seçin **başlangıç**. Üzerinde **başlangıç sayfasını Özelleştir** listesinden, *.xaml* dosya ve tıklayın **Tamam**.

4. Üzerinde **görünümü** menüsünü tıklatın **başlangıç sayfası**.

5. Tıklayın **Bing** sekmesi.

     Bing web sayfası görmeniz gerekir.

6. Tıklayın **MyButton** sekmesi.

     Görmelisiniz bir **MyProject** düğmesini açan **yeni proje** iletişim.

7. Deneysel örneği kapatın.

Özel başlangıç sayfası olarak uygulamak için **Araçları** > **seçenekleri** > **ortam**seçin **başlangıç**. Üzerinde **başlangıç sayfasını Özelleştir** listesinden, *.xaml* dosya ve tıklayın **Tamam**.

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio Başlangıç sayfası artık bir Web tarayıcısı sekmesi ve MyButton sekme görüntüleyen bir sekme içerir. Diğer işlevleri kullanarak sahip özel başlangıç sayfaları oluşturabilirsiniz *arka plan kod* gösterildiği gibi özel bir .dll dosyasını eklemek için model [başlangıç sayfasına kullanıcı denetimi ekleme](../extensibility/adding-user-control-to-the-start-page.md). Özel başlangıç sayfaları için elde edilen .vsix dosyasını yayımlayarak diğer kullanıcılarla paylaşabilir miyim [Visual Studio Market](https://marketplace.visualstudio.com/) Web sitesini veya başka bir Web sitesinin veya ağ paylaşımı. Daha fazla bilgi için [özel başlangıç sayfaları dağıtma](../extensibility/deploying-custom-start-pages.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Başlangıç sayfasını özelleştirme](../ide/customizing-the-start-page-for-visual-studio.md)
- [WPF kapsayıcı denetimleri](https://msdn.microsoft.com/library/a0177167-d7db-4205-9607-8ae316952566)