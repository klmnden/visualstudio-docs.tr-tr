---
title: Yalıtılmış Kabuğu genişletme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio shell, isolated mode
ms.assetid: 9a641d8f-211e-4486-a1b1-4a89fafe7ee8
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ea55039de769598b26868727a93cfa11726e4838
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443926"
---
# <a name="extending-the-isolated-shell"></a>Yalıtılmış Kabuğu genişletme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio yalıtılmış kabuğu, yalıtılmış Kabuk uygulaması için bir VSPackage'ı, Yönetilen Genişletilebilirlik Çerçevesi (MEF) bileşen parçası veya genel bir VSIX projesi ekleyerek genişletebilirsiniz.  
  
> [!NOTE]
> Aşağıdaki adımlar, bir temel yalıtılmış Kabuk uygulaması Visual Studio Kabuğu yalıtılmış proje şablonunu kullanarak oluşturduğunuz presuppose. Bu proje şablonu hakkında daha fazla bilgi için bkz: [izlenecek yol: Yalıtılmış Kabuk uygulaması temel bir oluşturma](../extensibility/walkthrough-creating-a-basic-isolated-shell-application.md).  
  
## <a name="locations-for-the-visual-studio-package-project-template"></a>Visual Studio Paket projesi şablonu için konumları  
 Visual Studio Paket proje şablonu, üç farklı konumlarda bulunabilir **yeni proje** iletişim:  
  
1. Altında **Visual Basic**, **genişletilebilirlik**. Visual Basic proje varsayılan dildir.  
  
2. Altında **Visual C#**, **genişletilebilirlik**. Varsayılan proje C# dilidir.  
  
3. Altında **diğer proje türleri**, **genişletilebilirlik**. C++ projesinin varsayılan dildir.  
  
## <a name="adding-a-vspackage"></a>VSPackage ekleme  
 VSPackage yalıtılmış kabuk uygulamanıza ekleyebilirsiniz. Aşağıdaki adımlar, menü komutlarını ekleyen oluşturma işlemi gösterilmektedir.  
  
#### <a name="to-add-a-new-vspackage"></a>Yeni bir VSPackage'ı eklemek için  
  
1. Adlı bir Visual Studio Paket projesi Ekle `MenuCommandsPackage`.  
  
2. Üzerinde **Temel VSPackage Bilgileri** sihirbazının ayarlamak **şirket adı** için `Fabrikam` ve **VSPackage'ı adı** için `FabrikamMenuCommands`. Seçin **sonraki** düğmesi.  
  
3. Sonraki sayfada seçin **menü komutu** seçip **sonraki**.  
  
4. Sonraki sayfada ayarlamak **komut adı** için `Fabrikam Command` ve **komut kimliği** için `cmdidFabrikamCommand`ve ardından **sonraki**.  
  
5. Üzerinde **proje seçenekleri Test** sayfasında, test seçenekleri temizleyin ve ardından **son** düğmesi.  
  
6. ShellExtensionsVSIX projesinde olan source.extension.vsixmanifest dosyasını açın.  
  
     **Varlıklar** bölümü VSShellStub.AboutBoxPackage proje için bir girdi içermelidir.  
  
7. Seçin **yeni** düğmesi.  
  
8. İçinde **yeni varlık Ekle** penceresi içinde **türü** listesinden **Microsoft.VisualStudio.VsPackage**.  
  
9. İçinde **kaynak** emin olun, liste **mevcut çözümde bir proje** seçilir. İçinde **proje** liste kutusu, select **MenuCommandsPackage**.  
  
10. Dosyayı kaydedin ve kapatın.  
  
11. Çözümü yeniden oluşturun ve yalıtılmış Kabuk hata ayıklamaya başlayın.  
  
12. Menü çubuğunda, **Araçları** menüsüne ve sonra **Fabrikam komut**.  
  
     Bir ileti kutusu görüntülenmelidir.  
  
13. Uygulama hata ayıklamasını durdurun.  
  
## <a name="adding-a-mef-component-part"></a>Bir MEF Bileşeni bölümü ekleme  
 Aşağıdaki adımlarda, bir MEF Bileşeni parçası yalıtılmış kabuk uygulamanıza eklemek gösterilmektedir.  
  
#### <a name="to-add-a-mef-component"></a>MEF bileşeni eklemek için  
  
1. İçinde **Yeni Proje Ekle** iletişim kutusunun **Visual C#**, **genişletilebilirlik**, kullanın **Düzenleyici kenar** şablonunu bir projeye ekleyin. Adlandırın `ShellEditorMargin`.  
  
2. ShellExtensionsVSIX projesinde tasarım görünümünde, kod görünümü olan Source.extension.vsixmanifest dosyasını açın.  
  
3. İçinde `Asset` bölümünde, seçin **İçerik Ekle**.  
  
4. İçinde **yeni varlık Ekle** penceresi içinde **türü** listesinden **Microsoft.VisualStudio.MefComponent**.  
  
5. İçinde **kaynak** emin olun, liste **mevcut çözümde bir proje** seçilir. İçinde **proje** liste kutusu, select **ShellEditorMargin**.  
  
6. Dosyayı kaydedin ve kapatın.  
  
7. Çözümü yeniden oluşturun ve yalıtılmış Kabuk hata ayıklamaya başlayın.  
  
8. Bir metin dosyası açın.  
  
     "Hello world!" sözcüklerini içeren bir yeşil bir kenar boşluğu metin dosyası penceresinin en altında görüntülenmesi gerekir.  
  
9. Uygulama hata ayıklamasını durdurun.  
  
## <a name="adding-a-generic-vsix-project"></a>Genel bir VSIX projesi ekleme  
  
#### <a name="to-add-a-generic-vsix-project"></a>Genel bir VSIX projesi eklemek için  
  
1. İçinde **Yeni Proje Ekle** iletişim kutusunun **Visual C#**, **genişletilebilirlik**, kullanın **VSIXProject** şablonunu bir projeye ekleyin. Adlandırın `EmptyVSIX`.  
  
2. ShellExtensionsVSIX projesinde tasarım görünümünde, kod görünümü Source.extensions.vsixmanifest dosyayı açın.  
  
3. İçinde `Assets` bölümünde, seçin **yeni**.  
  
4. İçinde **yeni varlık Ekle** penceresi içinde **türü** listesinde, eklemek istediğiniz içerik türü seçin.  
  
5. İçinde **kaynak**, emin **mevcut çözümde bir proje** seçeneği belirlenir. Liste kutusunda, VSIX projesinin adını seçin.  
  
6. Dosyayı kaydedin ve kapatın.  
  
7. Bu proje derlenmiş kodu içeriyorsa, projeyi derleme çıktısında dahildir böylece düzenlemeniz gerekir.  
  
    1. VSIX projeyi kaldırmak ve proje dosyasını açın.  
  
    2. İlk `<PropertyGroup>` değerini değiştirebilir, block `<CopyBuildOutputToOutputDirectory>` için `true`.  
  
    3. Kaydedin ve projeyi yeniden yükleyin.  
  
8. Derleme ve çözümü çalıştırın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: Temel Yalıtılmış Kabuk Uygulaması Oluşturma](../extensibility/walkthrough-creating-a-basic-isolated-shell-application.md)
