---
title: 'İzlenecek yol: Başlangıç sayfasına özel XAML ekleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- custom start page
- xaml start page
ms.assetid: 9af4d5f9-1cfc-4221-aea7-c8cd3f7571a6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a828fe6f7944e2bb0d9527d781c66630ed1f3879
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54947289"
---
# <a name="walkthrough-add-custom-xaml-to-the-start-page"></a>İzlenecek yol: Başlangıç sayfasına özel XAML ekleme
Bu kılavuzda, özel bir Visual Studio Başlangıç içeren bir Web tarayıcısı sayfası oluşturma işlemi gösterilmektedir.  
  
## <a name="adding-custom-xaml"></a>Özel XAML ekleme  
  
1.  Bir başlangıç sayfası'ndaki yönergeleri takip ederek oluşturma [özel başlangıç sayfası oluşturma](../extensibility/creating-a-custom-start-page.md).  
  
2.  İçinde *MainWindow.xaml* dosya, bulma \<kılavuz > bölümü.  
  
3.  Ekleme bir \<TabControl > öğesi ve bir \<TabItem > içinde \< kılavuz > öğesi, aşağıdaki örnekte gösterildiği gibi.  
  
    ```xml  
    <Grid>  
        <TabControl>  
            <TabItem Header="Bing" Height="Auto">  
                <Frame Source="http://www.bing.com" />  
            </TabItem>  
        </TabControl>  
    </Grid>  
    ```  
  
4.  İkinci bir ekleme \<TabItem >, ile bir \<düğmesi > Yeni bir proje açılır öğe:  
  
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
  
## <a name="testing-the-custom-start-page"></a>Özel başlangıç sayfasını test etme  
  
1.  Tuşuna **F5**.  
  
     Visual Studio'nun deneysel örneğinde, özel başlangıç yüklendi, ancak seçili sayfası ile açılır.  
  
2.  Visual Studio'nun deneysel örneğinde açın **araçları/Options / ortam** sayfası.  
  
3.  Seçin **başlangıç**. Üzerinde **başlangıç sayfasını Özelleştir** listesinden, *.xaml* dosya ve tıklayın **Tamam**.  
  
4.  Üzerinde **görünümü** menüsünü tıklatın **başlangıç sayfası**.  
  
5.  Tıklayın **Bing** sekmesi.  
  
     Bing web sayfası görmeniz gerekir.  
  
6.  Tıklayın **MyButton** sekmesi.  
  
     Görmelisiniz bir **MyProject** düğmesini açan **yeni proje** iletişim.  
  
7.  Deneysel örneği kapatın.  
  
## <a name="apply-the-custom-start-page"></a>Özel başlangıç sayfası uygula  
  
### <a name="to-test-the-custom-start-page"></a>Özel başlangıç sayfası test etmek için  
  
1.  İçinde **Araçlar / Seçenekler / ortam**seçin **başlangıç**. Üzerinde **başlangıç sayfasını Özelleştir** listesinden, *.xaml* dosya ve tıklayın **Tamam**.  
  
## <a name="next-steps"></a>Sonraki adımlar  
 Visual Studio Başlangıç sayfası artık bir Web tarayıcısı sekmesi ve MyButton sekme görüntüleyen bir sekme içerir. Özel başlangıç diğer işlevleri kullanarak olan sayfaları oluşturabilirsiniz *arka plan kod* gösterildiği gibi özel bir .dll dosyasını eklemek için model [başlangıç sayfasına kullanıcı denetimi ekleme](../extensibility/adding-user-control-to-the-start-page.md). Özel başlangıç sayfaları için elde edilen .vsix dosyasını yayımlayarak diğer kullanıcılarla paylaşabilir miyim [Visual Studio Galerisi](http://go.microsoft.com/fwlink/?LinkID=123847) Web sitesini veya başka bir Web sitesinin veya ağ paylaşımı. Daha fazla bilgi için [özel başlangıç sayfaları dağıtma](../extensibility/deploying-custom-start-pages.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Başlangıç sayfasını özelleştirme](../ide/customizing-the-start-page-for-visual-studio.md)   
 [WPF kapsayıcı denetimleri](https://msdn.microsoft.com/library/a0177167-d7db-4205-9607-8ae316952566)