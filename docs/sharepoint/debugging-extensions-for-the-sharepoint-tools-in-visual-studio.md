---
title: Visual Studio'da SharePoint araçları için hata ayıklama uzantıları | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, debugging extensions
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 8f838363b52a85faff022f49542fcc2fcc7e450d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53950822"
---
# <a name="debug-extensions-for-the-sharepoint-tools-in-visual-studio"></a>Uzantıları Visual Studio'da SharePoint araçları için hata ayıklama
  SharePoint araç uzantıları deneysel örneğinde veya normal örneğinde Visual Studio'nun hata ayıklaması yapabilirsiniz. Uzantının davranış sorun gidermeniz gerekiyorsa, ek hata bilgileri görüntülemek ve Visual Studio'nun SharePoint komutlarını nasıl yürüteceğini yapılandırmak için kayıt defteri değerlerini de değiştirebilirsiniz.

## <a name="debug-extensions-in-the-experimental-instance-of-visual-studio"></a>Visual Studio'nun deneysel örneğinde uzantıların hatalarını ayıklama
 Yanlışlıkla Visual Studio geliştirme ortamınızı sınanmamış uzantılar tarafından korumak için Visual Studio SDK'sı olarak adlandırılan alternatif bir Visual Studio örneği sağlar *deneysel örneğinde*, kullanabileceğiniz uzantıları yüklemek ve sınamak için. Visual Studio'nun normal örneği kullanılarak yeni uzantılar geliştirmek, ancak hata ayıklama ve deneysel örneğinde çalıştırın. Daha fazla bilgi için [deneysel örneğinde](../extensibility/the-experimental-instance.md).

 Uzantınızı dağıtmak amacıyla VSIX projesi kullanın ve VSIX projesi çözümünüzdeki başlangıç projesi olduğundan, Visual Studio otomatik olarak yükler ve çözümünüzü hata ayıklaması yaparken uzantıyı deneysel örneğinde çalışır. Başlangıç projesi birden fazla proje içeren bir çözüme hata ayıklaması yaptığınızda başlatan projesidir. Uzantınızı dağıtmak amacıyla VSIX projesi kullanma hakkında daha fazla bilgi için bkz. [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

 Çeşitli Visual Studio'nun deneysel örneğinde uzantıların hatalarını ayıklama gösteren örnekler için aşağıdaki izlenecek yollara bakın:

-   [İzlenecek yol: Bir SharePoint proje öğesi türünü genişletme](../sharepoint/walkthrough-extending-a-sharepoint-project-item-type.md)

-   [İzlenecek yol: Bir öğe şablonu, bölüm 1 ile özel bir eylem proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-custom-action-project-item-with-an-item-template-part-1.md)

-   [İzlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturma](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md)

-   [İzlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md)

-   [İzlenecek yol: Sunucu Gezgini uzantısında SharePoint istemcisi nesne modelini çağırma](../sharepoint/walkthrough-calling-into-the-sharepoint-client-object-model-in-a-server-explorer-extension.md)

## <a name="debug-extensions-in-the-regular-instance-of-visual-studio"></a>Visual Studio normal örneğinde uzantıların hatalarını ayıklama
 İlk uzantısı projenizde Visual Studio normal örneğinde hata ayıklamak istiyorsanız, normal örneğe uzantıyı yükleyin. Ardından, hata ayıklayıcıyı ikinci bir Visual Studio işlemine iliştirin. İşlemi tamamladığınızda, böylece artık geliştirme bilgisayarına yükler uzantıyı kaldırabilirsiniz.

#### <a name="to-install-the-extension"></a>Uzantıyı yüklemek için

1.  Visual Studio'nun tüm örneklerini kapatın.

2.  Uzantı projesi yapı çıkış klasöründe açın *.vsix* dosyasını çift tıklatıp veya kısayol menüsünü açarak ve ardından **açın**:

3.  İçinde **Visual Studio Uzantı Yükleyicisi** iletişim kutusunda, uzantıyı yükleyin ve ardından istediğiniz Visual Studio sürümünü **yükleme** düğmesi.

     Visual Studio için %UserProfile%\AppData\Local\Microsoft\VisualStudio\11.0\Extensions uzantılarını yükler\\*yazar adı*\\*uzantı adı* \\ *sürüm*. Bu yol içerisindeki son üç klasör oluşturulan `Author`, `Name`, ve `Version` öğelerinde *extension.vsixmanifest* dosya uzantısı.

4.  Visual Studio uzantıyı yükledikten sonra seçin **Kapat** düğmesi.

#### <a name="to-debug-the-extension"></a>Uzantının hatalarını ayıklamak için

1.  Visual Studio'yu yönetici ayrıcalıklarıyla başlatın ve uzantı projesini açın. Aşağıdaki adımları olarak Visual Studio'nun bu örneğine başvurmaktadır *ilk örnek*.

2.  Başka bir örneği Visual Studio'nun yönetici ayrıcalıklarıyla başlatın. Aşağıdaki adımları olarak Visual Studio'nun bu örneğine başvurmaktadır *ikinci örneğini*.

3.  Visual Studio'nun ilk örneğine geçin.

4.  Menü çubuğunda, **hata ayıklama**, **iliştirme**.

5.  İçinde **kullanılabilir işlemler** listesinde *devenv.exe*. Bu giriş, Visual Studio'nun ikinci örneğine başvurur; Bu, proje Uzantınız için içerisinde hata ayıklamak istediğiniz örneğidir.

6.  Seçin **iliştirme** düğmesi.

     Visual Studio uzantı projesi hata ayıklama modunda çalıştırır.

7.  Visual Studio'nun ikinci örneğine geçin.

8.  Uzantınızı yükleyen yeni bir SharePoint projesi oluşturun. Örneğin, liste tanımı proje öğeleri için bir uzantı ayıklıyorsanız, oluşturun bir **liste tanımı** proje.

9. Uzantı kodunuzu sınamak için gereken tüm adımları gerçekleştirin.

10. Uzantı hata ayıklamasını tamamladığınızda, Visual Studio'nun ikinci örneğini kapatın.

#### <a name="to-remove-the-extension"></a>Uzantıyı kaldırmak için

1.  Visual Studio'da menü çubuğunda, **Araçları**, **Uzantılar ve güncelleştirmeler**.

     **Uzantılar ve güncelleştirmeler** iletişim kutusu açılır.

2.  Uzantılar listesinde, uzantı adını seçin ve ardından **kaldırma** düğmesi.

3.  Görünen iletişim kutusunda **Evet** uzantının yüklemesini kaldırmak istediğinizi onaylamak için düğme.

4.  Seçin **şimdi yeniden Başlat** kaldırma işlemini tamamlamak için düğme.

## <a name="debug-sharepoint-commands"></a>SharePoint komutları hata ayıklama
 SharePoint araçları uzantısının bir parçası olan bir SharePoint komutu hatasını ayıklamak istiyorsanız, hata ayıklayıcıyı iliştirmek *vssphost4.exe* işlem. Bu, SharePoint komutlarını yürüten 64-bit ana bilgisayar işlemidir. SharePoint komutları hakkında daha fazla bilgi ve *vssphost4.exe*, bkz: [SharePoint nesne modellerini çağırma](../sharepoint/calling-into-the-sharepoint-object-models.md).

#### <a name="to-attach-the-debugger-to-the-vssphost4exe-process"></a>Hata ayıklayıcı vssphost4.exe işlemine eklemek için

1.  Yukarıdaki yönergeleri izleyerek uzantınızın Visual Studio'nun deneysel örneğinde veya normal örneğinde Visual Studio'nun hata ayıklamayı başlatın.

2.  Visual Studio'nun içinde çalıştırdığınız hata ayıklayıcı, menü çubuğunda örneğinde seçin **hata ayıklama**, **iliştirme**.

3.  İçinde **kullanılabilir işlemler** listesinde *vssphost.exe*.

    > [!NOTE]
    >  Vssphost.exe listede görünmüyorsa, başlamalıdır *vssphost4.exe* uzantı içinde çalıştırdığınız Visual Studio örneğinde işlem. Genellikle, Visual Studio'nun geliştirme bilgisayarında SharePoint sitesine bağlanmasına neden olan eylemi gerçekleştirerek yaparsınız. Örneğin, Visual Studio başlatılır *vssphost4.exe* altında bir site bağlantı düğümü (site URL'sini görüntüleyen bir düğümü) genişlettiğinizde **SharePoint bağlantıları** düğümünde **Sunucu Gezgini**  penceresinde veya eklediğinizde, belirli bir SharePoint Proje öğeleri gibi **liste örneği** veya **olay alıcısı** , bir SharePoint projesine öğeler.

4.  Seçin **iliştirme** düğmesi.

5.  Hatası ayıklanmakta olan Visual Studio örneğinde, komutunuzu yürütmek için gerekli adımları gerçekleştirin.

## <a name="modify-registry-values-to-help-debug-sharepoint-tools-extensions"></a>SharePoint araç uzantıları hata ayıklama yardımcı olmak için kayıt defteri değerlerini değiştirme
 Visual Studio'daki SharePoint araçlarının uzantısına hata ayıklaması yaparken uzantı sorunlarını gidermenize yardımcı olmak için kayıt defteri değerlerini değiştirebilirsiniz. Değerleri altında mevcut **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\11.0\SharePointTools** anahtarı. Bu değerler varsayılan olarak bulunmaz.

 SharePoint araçlarının herhangi bir uzantı sorunlarını gidermenize yardımcı olmak için oluşturabilir ve EnableDiagnostics değerini ayarlayın. Aşağıdaki tabloda, bu değeri açıklamaktadır.

|Değer|Açıklama|
|-----------|-----------------|
|EnableDiagnostics|Tanılama iletilerinin görüntülenip görüntülenmeyeceğini belirten REG_DWORD **çıkış** penceresi.<br /><br /> Tanı iletileri görüntülemek için bu değeri 1 olarak ayarlayın. İletileri görüntülemeyi durdurmak için bu değeri 0 olarak ayarlayın veya bu değeri silin.<br /><br /> İleti yazmak için **çıkış** penceresinden bir SharePoint araçları uzantısından, SharePoint Proje hizmetini kullanın. Daha fazla bilgi için [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).|

 Uzantınızı bir SharePoint komutu içeriyorsa, oluşturabilir ve komutun sorun gidermesi amacıyla ek değerler ayarlayın. Aşağıdaki tabloda, bu değerleri açıklamaktadır.

|Değer|Açıklama|
|-----------|-----------------|
|AttachDebuggerToHostProcess|Hata ayıklayıcının olanak tanıyan bir iletişim kutusunun görüntülenip görüntülenmeyeceğini belirten REG_DWORD *vssphost4.exe* başladıktan hemen sonra. Bu, hata ayıklamak istediğiniz komut başladıktan hemen sonra vssphost.exe tarafından yürütülürse yararlı olur ve hata ayıklayıcıyı komutu yürütülmeden önce el ile eklemek için yeterli zaman değildir. İletişim kutusunu görüntülemek için *vssphost4.exe* çağrıları <xref:System.Diagnostics.Debugger.Break%2A> başlatıldığında yöntemi.<br /><br /> Bu davranışı etkinleştirmek için bu değeri 1 olarak ayarlayın. Bu davranışı devre dışı bırakmak için bu değeri 0 olarak ayarlayın veya bu değeri silin.<br /><br /> Bu değer 1 olarak ayarlarsanız, ayrıca kendiniz Visual Studio bekliyor eklemek için yeterli süre vermek amacıyla HostProcessStartupTimeout değerini artırmak isteyebilirsiniz *vssphost4.exe* sinyal başarıyla başlatıldı.|
|ChannelOperationTimeout|Bir SharePoint komutu yürütmek Visual Studio bekleyeceği saniye cinsinden süreyi belirten REG_DWORD. Zaman içinde komut yürütülemezse bir <xref:Microsoft.VisualStudio.SharePoint.SharePointConnectionException> oluşturulur.<br /><br /> Varsayılan değer 120 saniyedir.|
|HostProcessStartupTimeout|Visual Studio süreyi saniye cinsinden belirten REG_DWORD, bekler *vssphost4.exe* sinyal başarıyla başlatıldı. Varsa *vssphost4.exe* zaman içinde başarılı bir başlangıç sinyali bir <xref:Microsoft.VisualStudio.SharePoint.SharePointConnectionException> oluşturulur.<br /><br /> Varsayılan değer 60 saniyedir.|
|maxReceivedMessageSize|Visual Studio arasında geçilen WCF iletilerinin bayt cinsinden boyutu, izin verilen maksimum belirten REG_DWORD ve *vssphost4.exe*.<br /><br /> Varsayılan 1.048.576 bayttır (1 MB) ' dir.|
|MaxStringContentLength|Visual Studio arasında geçirildiği dizelere bayt cinsinden boyutu, izin verilen maksimum belirten REG_DWORD ve *vssphost4.exe*.<br /><br /> Varsayılan 1.048.576 bayttır (1 MB) ' dir.|

## <a name="see-also"></a>Ayrıca bkz.

- [SharePoint araçlarını Visual Studio'da genişletme](../sharepoint/extending-the-sharepoint-tools-in-visual-studio.md)
- [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md)
