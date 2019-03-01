---
title: Hata ayıklama Canlı ASP.NET Azure sanal makineler ve Azure sanal makine ölçek kümeleri
description: Anlık görüntü noktaları ayarlamak ve anlık görüntü hata ayıklayıcısı ile anlık görüntüleri görüntüleme hakkında bilgi edinin.
ms.custom: ''
ms.date: 02/06/2019
ms.topic: conceptual
helpviewer_keywords:
- debugger
author: poppastring
ms.author: madownie
manager: andster
monikerRange: '>= vs-2019'
ms.workload:
- aspnet
- azure
ms.openlocfilehash: 608745fc2c96836163e1406abda6869d52b1da1b
ms.sourcegitcommit: 62149c96de0811415e99bb1e0194e76c320e1a1e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2019
ms.locfileid: "57007281"
---
# <a name="debug-live-aspnet-apps-on-azure-virtual-machines-and-azure-virtual-machine-scale-sets-using-the-snapshot-debugger"></a>Azure sanal makinelerinde Canlı ASP.NET uygulamalarında hata ayıklamak ve Snapshot Debugger'ı kullanarak Azure sanal makine ölçek kümeleri

Snapshot Debugger, ilgilendiğiniz kod yürütüldüğünde, üretim uygulamalarınızı anlık görüntüsünü alır. Bir anlık görüntüsünü almak için hata ayıklayıcı açmasını sağlamak için anlık görüntü noktaları ve günlüğe kaydetme noktaları kodunuzda ayarlayın. Hata ayıklayıcı, tam olarak üretim uygulamanızın trafiğini etkilemeden, çıktığına görmenizi sağlar. Snapshot Debugger, üretim ortamlarında ortaya çıkan sorunları çözmek için gereken süreyi ciddi ölçüde azaltmaya yardımcı olabilir.

Anlık görüntü noktaları ve günlüğe kaydetme noktaları da kesme noktaları için benzerdir, ancak kesme noktalarının aksine, anlık görüntü noktaları uygulamayı durdurmak yok isabet edildiğinde. Genellikle, bir anlık görüntü noktası bir anlık görüntüye yakalama 20 10 milisaniye cinsinden alır.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Snapshot Debugger'ı Başlat
> * Bir anlık görüntü noktası ayarlayın ve bir anlık görüntüyü Göster
> * Bir günlüğe kaydetme noktası ayarlayın

## <a name="prerequisites"></a>Önkoşullar

* Azure sanal makineler (VM) ve Azure sanal makine ölçek kümeleri (VMSS) için Snapshot Debugger, yalnızca Visual Studio 2019 Enterprise Önizleme veya üzeri ile **Azure geliştirme iş yükü**. (Altında **tek tek bileşenler** sekmesinde bulduğunuz altında **hata ayıklama ve test** > **anlık görüntü hata ayıklayıcısı**.)

    Henüz yüklü değilse, yükleme [Visual Studio 2019 Enterprise preview](https://visualstudio.microsoft.com/vs/preview/).

* Anlık görüntü koleksiyonu, aşağıdaki Azure VM/VMSS web uygulamaları için kullanılabilir:
  * .NET Framework 4.6.1 üzerinde çalışan ASP.NET uygulamalarından veya üzeri.
  * .NET Core 2.0 veya daha sonra Windows üzerinde çalışan ASP.NET Core uygulamaları.

## <a name="open-your-project-and-start-the-snapshot-debugger"></a>Snapshot Debugger'ı başlatın ve projenizi açın

1. Anlık görüntü hata ayıklama için istediğiniz projeyi açın.

    > [!IMPORTANT]
    > Anlık görüntü hata ayıklama, açmanıza gerek *kaynak kodu sürümüyle aynı sürümü* Azure VM/VMSS hizmetinize yayımlanmış.

1. Snapshot Debugger iliştirebilmek. Birkaç farklı yöntemden birini kullanabilirsiniz:

    * Seçin **hata ayıklama > Snapshot Debugger iliştirebilmek...** . Web uygulamanızın dağıtıldığı hedef Azure VM/VMSS ve bir Azure depolama hesabını seçin ve ardından **iliştirme**.

      ![Hata ayıklama menüsünden snapshot debugger'ı Başlat](../debugger/media/snapshot-debug-menu-attach.png)

    * Seçin ve proje üzerinde sağ tıklayın **Yayımla**ve ardından Yayımla Sayfası tıklatıldığında **Snapshot Debugger Ekle**. Web uygulamanızın dağıtıldığı hedef Azure VM/VMSS ve bir Azure depolama hesabını seçin ve ardından **iliştirme**.
    ![Snapshot debugger Yayımla sayfasından başlatın](../debugger/media/snapshot-publish-attach.png)

    * Aşağı açılan menüyü seçin hata ayıklama hedef **Snapshot Debugger**, isabet **F5** ve gerekirse, web uygulamanızın dağıtıldığı hedef Azure VM/VMSS ve bir Azure depolama seçeneğini belirlerseniz hesap ve ardından  **Ekleme**.
    ![F5 aşağı açılan menüden snapshot debugger'ı Başlat](../debugger/media/snapshot-F5-dropdown-attach.png)

    * Cloud Explorer'ı kullanarak (**Görüntüle > Cloud Explorer**), web uygulamanızın dağıtıldığı hedef Azure VM/VMSS sağ tıklayın ve bir Azure depolama hesabını seçin ve ardından **Snapshot Debugger Ekle**.

      ![Anlık görüntü Hata Ayıklayıcı'dan Cloud Explorer başlatma](../debugger/media/snapshot-launch.png)

    > [!IMPORTANT]
    > Seçtiğiniz ilk kez **Snapshot Debugger Ekle** VM'niz için IIS otomatik olarak yeniden başlatılır.
    > Seçtiğiniz ilk kez **Snapshot Debugger Ekle** , VMSS için VMSS her örneğinin el ile yükseltme gerektirir.

    Meta verileri **modülleri** başlangıçta etkinleştirilmeyecek, web uygulamasına gidin ve **toplamaya Başla** düğmesi etkin olacak. Visual Studio anlık hata ayıklama modu sunulmuştur.

    > [!NOTE]
    > Application Insights site uzantısı, anlık görüntü hata ayıklaması da destekler. Bir "site uzantısı güncel değil" hata iletisi ile karşılaşırsanız, bkz [sorun giderme ipuçları ve anlık görüntü hata ayıklama için bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md) ayrıntıları yükseltme.
    > VMSS için Snapshot Debugger için ilk kez ekledikten sonra onların VMSS örnekleri el ile yükseltme kullanıcısı gereklidir.

   ![Anlık görüntü hata ayıklama modu](../debugger/media/snapshot-message.png)

   **Modülleri** penceresi gösterir, tüm modüller için Azure VM/VMSS zaman yüklediniz (seçin **hata ayıklama > Windows > modülleri** bu pencereyi açmak için).

   ![Modüller penceresini denetleyin](../debugger/media/snapshot-modules.png)

## <a name="set-a-snappoint"></a>Bir anlık görüntü noktası ayarlayın

1. Kod Düzenleyicisi'nde bir anlık görüntü noktası ayarlamak ilginizi çeken bir kod satırının yanındaki sol kanaldaki tıklayın. Yürütecek bildiğiniz kod olduğundan emin olun.

   ![Bir anlık görüntü noktası ayarlayın](../debugger/media/snapshot-set-snappoint.png)

1. Tıklayın **toplamaya Başla** anlık görüntü noktasını etkinleştirmek için.

   ![Anlık görüntü noktasını Aç](../debugger/media/snapshot-start-collection.png)

    > [!TIP]
    > Anlık görüntü görüntülerken girilemiyor, ancak farklı satır kod yürütmeyi izlemek için kodunuzun birden çok anlık görüntü noktaları yerleştirebilirsiniz. Snapshot Debugger, kodunuzda birden çok anlık görüntü noktaları varsa, karşılık gelen anlık görüntüleri aynı son kullanıcı oturumunda olduğundan emin olur. Snapshot Debugger, uygulamanızı birçok kullanıcıları olsa bile bunu yapar.

## <a name="take-a-snapshot"></a>Bir anlık görüntüsünü alın

Bir anlık görüntü noktası etkinleştirildiğinde, anlık görüntü noktası yerleştirildiği kod satırının yürütür her bir anlık görüntüsünü yakalar. Bu yürütme sunucunuzdaki gerçek bir istek neden olabilir. İsabet, web sitenizin tarayıcı görünümüne gidin ve tüm eylemleri için anlık görüntü noktası zorlamak için anlık görüntü noktası ulaşılmasına neden gereklidir.

## <a name="inspect-snapshot-data"></a>Anlık görüntü verileri İnceleme

1. Anlık görüntü noktası isabet edildiğinde bir anlık görüntü tanılama araçları penceresinde görünür. Bu pencereyi açmak için seçin **hata ayıklama > Windows > tanılama araçlarını Göster**.

   ![Bir anlık görüntü noktası açın](../debugger/media/snapshot-diagsession-window.png)

1. Anlık görüntü noktası anlık görüntü Kod Düzenleyicisi'nde açmak için çift tıklayın.

   ![Anlık görüntü verileri İnceleme](../debugger/media/snapshot-inspect-data.png)

   Bu görünümden veri ipuçlarını görüntülemek için kullanmak için değişkenlerden gelerek **Yereller**, **izlemeleri**, ve **çağrı yığını** windows ve ayrıca ifadeleri değerlendirin.

    Web sitesinin kendisinde hala çalışıyor ve son kullanıcıların etkilenen değildir. Varsayılan olarak anlık görüntü noktası yalnızca bir anlık görüntüsü yakalanır: anlık görüntü yakalandıktan sonra anlık görüntü noktası devre dışı bırakır. Anlık görüntü noktası başka bir anlık görüntü yakalamak istiyorsanız, anlık görüntü noktası tıklayarak tekrar açabilirsiniz **koleksiyonu Güncelleştir**.

Ayrıca daha fazla anlık görüntü noktaları uygulamanıza ekleyin ve ile Aç **koleksiyonu Güncelleştir** düğmesi.

**Yardıma mı ihtiyacınız var?** Bkz: [sorun giderme ve bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md) ve [anlık görüntü hata ayıklama ile ilgili SSS](../debugger/debug-live-azure-apps-faq.md) sayfaları.

## <a name="set-a-conditional-snappoint"></a>Koşullu bir anlık görüntü noktası ayarlayın

Uygulamanızı belirli bir durumda yeniden oluşturmak zor ise, koşullu bir anlık görüntü noktası kullanımı yardımcı olup olmadığını göz önünde bulundurun. Koşullu bir anlık görüntü noktaları Yardım uygulama gibi bir değişken incelemek istediğiniz belirli bir değere sahip olduğunda istenen bir durum girene kadar anlık kaçının. İfadeler, filtreleri kullanarak koşulları ayarlama veya isabet sayıları.

#### <a name="to-create-a-conditional-snappoint"></a>Koşullu bir anlık görüntü oluşturmak için

1. Bir anlık görüntü noktası simgesi (boş Top) sağ tıklatın ve seçin **ayarları**.

   ![Ayarları seçin](../debugger/media/snapshot-snappoint-settings.png)

1. Anlık görüntü noktası ayarları penceresinde, bir ifade yazın.

   ![Bir ifade yazın](../debugger/media/snapshot-snappoint-conditions.png)

   Önceki çizimde, yalnızca anlık görüntü noktası için anlık görüntü oluşturulduğunda, `visitor.FirstName == "Dan"`.

## <a name="set-a-logpoint"></a>Bir günlüğe kaydetme noktası ayarlayın

Bir anlık görüntü noktası isabet edildiğinde bir anlık görüntü alma ek olarak, bir iletiyi günlüğe kaydetmek için anlık görüntü noktası da yapılandırabilirsiniz (diğer bir deyişle, bir günlüğe kaydetme noktası oluşturma). Günlüğe kaydetme noktaları, uygulamanızı yeniden dağıtmak zorunda kalmadan ayarlayabilirsiniz. Günlüğe kaydetme noktaları neredeyse yürütülür ve herhangi bir etkisi veya çalışan uygulamanıza yan etkilere neden.

#### <a name="to-create-a-logpoint"></a>Bir günlüğe kaydetme noktası oluşturmak için

1. Bir anlık görüntü noktası simgesi (mavi Altıgene) sağ tıklatın ve seçin **ayarları**.

1. Anlık görüntü noktası ayarları penceresinde, seçin **eylemleri**.

    ![Bir günlüğe kaydetme noktası oluşturma](../debugger/media/snapshot-logpoint.png)

1. İçinde **ileti** alan, oturum açmak istediğiniz yeni günlük iletisi girebilirsiniz. Ayrıca, kaşlı ayraçlar içinde yerleştirerek değişkenleri, bir günlük iletisinde değerlendirebilirsiniz.

    Seçerseniz **çıkış penceresine Gönder**, günlüğe kaydetme noktası gelindiğinde tanılama araçları penceresinde iletisi görüntülenir.

    ![Diagsession penceredeki verileri günlüğe kaydetme noktası](../debugger/media/snapshot-logpoint-output.png)

    Seçerseniz **uygulama günlüğüne Gönder**, günlüğe kaydetme noktası isabet edildiğinde iletilerden gördüğünüz herhangi bir ileti görüntülenir `System.Diagnostics.Trace` (veya `ILogger` .NET core'da), aşağıdakiler gibi [App Insights](/azure/application-insights/app-insights-asp-net-trace-logs).

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, Azure sanal makineler ve Azure sanal makine ölçek kümeleri için Snapshot Debugger kullanmayı öğrendiniz. Bu özellik hakkında daha fazla bilgi okumak isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Anlık görüntü hatalarını ayıklama hakkında SSS](../debugger/debug-live-azure-apps-faq.md)