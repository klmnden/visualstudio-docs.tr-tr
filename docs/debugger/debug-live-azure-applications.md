---
title: Canlı ASP.NET Azure uygulamalarında hata ayıklama
description: Anlık görüntü noktaları ayarlamak ve anlık görüntü hata ayıklayıcısı ile anlık görüntüleri görüntüleme hakkında bilgi edinin.
ms.custom: ''
ms.date: 03/16/2018
ms.topic: conceptual
helpviewer_keywords:
- debugger
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
- azure
ms.openlocfilehash: 9bbd0aa8ea3d98077154225fb3a35aec5545ccfa
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68415737"
---
# <a name="debug-live-aspnet-azure-apps-using-the-snapshot-debugger"></a>Snapshot Debugger'ı kullanarak canlı ASP.NET Azure uygulamalarında hata ayıklama

Snapshot Debugger, ilgilendiğiniz kod yürütüldüğünde, üretim uygulamalarınızı anlık görüntüsünü alır. Bir anlık görüntüsünü almak için hata ayıklayıcı açmasını sağlamak için anlık görüntü noktaları ve günlüğe kaydetme noktaları kodunuzda ayarlayın. Hata ayıklayıcı, tam olarak üretim uygulamanızın trafiğini etkilemeden, çıktığına görmenizi sağlar. Snapshot Debugger, üretim ortamlarında ortaya çıkan sorunları çözmek için gereken süreyi ciddi ölçüde azaltmaya yardımcı olabilir.

Anlık görüntü noktaları ve günlüğe kaydetme noktaları da kesme noktaları için benzerdir, ancak kesme noktalarının aksine, anlık görüntü noktaları uygulamayı durdurmak yok isabet edildiğinde. Genellikle, bir anlık görüntü noktası bir anlık görüntüye yakalama 20 10 milisaniye cinsinden alır.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Snapshot Debugger'ı Başlat
> * Bir anlık görüntü noktası ayarlayın ve bir anlık görüntüyü Göster
> * Bir günlüğe kaydetme noktası ayarlayın

## <a name="prerequisites"></a>Önkoşullar

* Snapshot Debugger, **Azure geliştirme iş yükü**Ile yalnızca Visual Studio 2017 Enterprise sürüm 15,5 veya üzeri sürümlerde kullanılabilir. ( **Tek tek bileşenler** sekmesinde, **hata ayıklama ve test** > **anlık görüntü hata ayıklayıcısı**altında bulabilirsiniz.)

   ::: moniker range=">=vs-2019"
   Henüz yüklenmemişse, [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)' i yükleme. Önceki bir Visual Studio yüklemesinden güncelleştirme yapıyorsanız, Visual Studio Yükleyicisi çalıştırın ve **ASP.net ve Web geliştirme iş**yükünde Snapshot Debugger bileşenini denetleyin.
   ::: moniker-end
   ::: moniker range="<=vs-2017"
   Henüz yüklü değilse, yükleme [Visual Studio 2017 Enterprise sürüm 15.5](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) veya üzeri. Önceki bir Visual Studio 2017 yüklemesinden güncelleştirme yapıyorsanız, Visual Studio Yükleyicisi çalıştırın ve **ASP.net ve Web geliştirme iş**yükünde Snapshot Debugger bileşenini kontrol edin.
   ::: moniker-end

* Azure App Service planı temel veya daha yüksek.

* Anlık görüntü koleksiyonunu, Azure App Service'te çalışan aşağıdaki web uygulamaları için kullanılabilir:
  * .NET Framework 4.6.1 üzerinde çalışan ASP.NET uygulamalarından veya üzeri.
  * .NET Core 2.0 veya daha sonra Windows üzerinde çalışan ASP.NET Core uygulamaları.

## <a name="open-your-project-and-start-the-snapshot-debugger"></a>Snapshot Debugger'ı başlatın ve projenizi açın

1. Anlık görüntü hata ayıklama için istediğiniz projeyi açın.

   > [!IMPORTANT]
   > Anlık görüntü hata ayıklama, açmanıza gerek *kaynak kodu sürümüyle aynı sürümü* Azure App Service için yayımlanır.

::: moniker range="<=vs-2017"

2. Bulut Gezgini'nde (**Görüntüle > Cloud Explorer**), projeniz için dağıtıldığı Azure App Service'ı sağ tıklatın ve seçin **Snapshot Debugger Ekle**.

   ![Snapshot debugger'ı Başlat](../debugger/media/snapshot-launch.png)

::: moniker-end

::: moniker range=">=vs-2019"

2. **Hata ayıkla > Snapshot Debugger Ekle...** seçeneğini belirleyin. Projenizin dağıtıldığı Azure App Service seçin ve bir Azure depolama hesabına ve ardından **Ekle**' ye tıklayın. Snapshot Debugger Ayrıca, sanal makine ölçek kümeleri & [Azure Kubernetes hizmetini](debug-live-azure-kubernetes.md) ve [Azure sanal makinelerini (VM)](debug-live-azure-virtual-machines.md)destekler.

   ![Hata ayıklama menüsünden Snapshot Debugger 'ı başlatın](../debugger/media/snapshot-debug-menu-attach.png)

   ![Azure kaynağı seçin](../debugger/media/snapshot-select-azure-resource-appservices.png)

::: moniker-end

   > [!IMPORTANT]
   > Seçtiğiniz ilk kez **Snapshot Debugger Ekle**, Azure App Service üzerinde Snapshot Debugger site uzantısını yüklemeniz istenir. Bu yükleme, Azure App service'inizi yeniden başlatılması gerekir.

   ::: moniker range="<=vs-2017"
   > [!NOTE]
   > Application Insights site uzantısı, anlık görüntü hata ayıklaması da destekler. "Site uzantısı güncel değil" hata iletisiyle karşılaşırsanız, ayrıntıları yükseltmek için bkz. [sorun giderme ipuçları ve anlık görüntü hata ayıklaması için bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md) .
   ::: moniker-end
   ::: moniker range=">=vs-2019"
   > [!NOTE]
   > (Visual Studio 2019 sürüm 16,2 ve üstü) Snapshot Debugger Azure bulut desteğini etkinleştirdi. Seçtiğiniz Azure kaynağının ve Azure depolama hesabının aynı buluttan olduğundan emin olun. Kuruluşunuzun [Azure uyumluluk](https://azure.microsoft.com/overview/trusted-cloud/) yapılandırmalarına ilişkin sorularınız varsa lütfen Azure yöneticinize başvurun.
   ::: moniker-end

   Visual Studio anlık hata ayıklama modu sunulmuştur.
   ![Anlık görüntü hata ayıklama modu](../debugger/media/snapshot-message.png)

   **Modüller** penceresi, tüm modüllerin Azure App Service için ne zaman yüklendiğini gösterir (Bu pencereyi açmak için **Windows > modülleri > Hata Ayıkla** ' yı seçin).

   ![Modüller penceresini denetleyin](../debugger/media/snapshot-modules.png)

## <a name="set-a-snappoint"></a>Bir anlık görüntü noktası ayarlayın

1. Kod Düzenleyicisi 'nde, bir anlık görüntü noktası ayarlamak için ilgilendiğiniz kod satırının yanındaki sol cilt payı tıklatın. Uygulamasının çalıştırabildiğinizi bildiğiniz kodun olduğundan emin olun.

   ![Bir anlık görüntü noktası ayarlayın](../debugger/media/snapshot-set-snappoint.png)

2. Tıklayın **toplamaya Başla** anlık görüntü noktasını etkinleştirmek için.

   ![Anlık görüntü noktasını Aç](../debugger/media/snapshot-start-collection.png)

   > [!TIP]
   > Anlık görüntü görüntülerken girilemiyor, ancak farklı satır kod yürütmeyi izlemek için kodunuzun birden çok anlık görüntü noktaları yerleştirebilirsiniz. Snapshot Debugger, kodunuzda birden çok anlık görüntü noktaları varsa, karşılık gelen anlık görüntüleri aynı son kullanıcı oturumunda olduğundan emin olur. Snapshot Debugger, uygulamanızı birçok kullanıcıları olsa bile bunu yapar.

## <a name="take-a-snapshot"></a>Bir anlık görüntüsünü alın

Bir anlık görüntü noktası ayarlandıktan sonra, Web sitenizin tarayıcı görünümüne gidip, işaretlenmiş kod satırını çalıştırarak veya kullanıcılarınızın site kullanımlarından bir tane oluşturması için bekleyen bir anlık görüntüyü el ile oluşturabilirsiniz.


## <a name="inspect-snapshot-data"></a>Anlık görüntü verileri İnceleme

1. Anlık görüntü noktası isabet edildiğinde bir anlık görüntü tanılama araçları penceresinde görünür. Bu pencereyi açmak için **hata ayıkla > Windows > tanılama araçları göster**' i seçin.

   ![Bir anlık görüntü noktası açın](../debugger/media/snapshot-diagsession-window.png)

1. Anlık görüntü noktası anlık görüntü Kod Düzenleyicisi'nde açmak için çift tıklayın.

   ![Anlık görüntü verileri İnceleme](../debugger/media/snapshot-inspect-data.png)

   Bu görünümden veri ipuçlarını görüntülemek için kullanmak için değişkenlerden gelerek **Yereller**, **izlemeleri**, ve **çağrı yığını** windows ve ayrıca ifadeleri değerlendirin.

   Web sitesinin kendisi de canlı ve son kullanıcılar etkilenmemektedir. Varsayılan olarak anlık görüntü noktası yalnızca bir anlık görüntüsü yakalanır: anlık görüntü yakalandıktan sonra anlık görüntü noktası devre dışı bırakır. Anlık görüntü noktası başka bir anlık görüntü yakalamak istiyorsanız, anlık görüntü noktası tıklayarak tekrar açabilirsiniz **koleksiyonu Güncelleştir**.

Ayrıca daha fazla anlık görüntü noktaları uygulamanıza ekleyin ve ile Aç **koleksiyonu Güncelleştir** düğmesi.

**Yardıma mı ihtiyacınız var?** Bkz: [sorun giderme ve bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md) ve [anlık görüntü hata ayıklama ile ilgili SSS](../debugger/debug-live-azure-apps-faq.md) sayfaları.

## <a name="set-a-conditional-snappoint"></a>Koşullu bir anlık görüntü noktası ayarlayın

Uygulamanızda belirli bir durumu yeniden oluşturmayı zorlaştırıyorsa, koşullu bir anlık görüntü noktası kullanmayı düşünün. Koşullu anlık görüntü noktaları, bir değişken, incelemek istediğiniz belirli bir değeri içerdiğinde olduğu gibi, bir anlık görüntünün ne zaman ele alıp denetistemediğinizi denetlemenize yardımcı olur. İfadeler, filtreleri kullanarak koşulları ayarlama veya isabet sayıları.

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

1. **İleti** alanına, günlüğe kaydetmek istediğiniz yeni günlük iletisini girebilirsiniz. Ayrıca, kaşlı ayraçlar içinde yerleştirerek değişkenleri, bir günlük iletisinde değerlendirebilirsiniz.

   Seçerseniz **çıkış penceresine Gönder**, günlüğe kaydetme noktası gelindiğinde tanılama araçları penceresinde iletisi görüntülenir.

   ![Tanılama Araçları penceresindeki logpoint verileri](../debugger/media/snapshot-logpoint-output.png)

   Seçerseniz **uygulama günlüğüne Gönder**, günlüğe kaydetme noktası isabet edildiğinde iletilerden gördüğünüz herhangi bir ileti görüntülenir `System.Diagnostics.Trace` (veya `ILogger` .NET core'da), aşağıdakiler gibi [App Insights](/azure/application-insights/app-insights-asp-net-trace-logs).

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, uygulama hizmetleri için Snapshot Debugger kullanmayı öğrendiniz. Bu özellik hakkında daha fazla bilgi okumak isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Anlık görüntü hatalarını ayıklama hakkında SSS](../debugger/debug-live-azure-apps-faq.md)