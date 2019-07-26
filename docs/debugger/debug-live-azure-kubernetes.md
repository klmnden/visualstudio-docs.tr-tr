---
title: Live ASP.NET Azure Kubernetes hizmetlerinde hata ayıklama
description: Anlık görüntü noktaları ayarlamak ve anlık görüntü hata ayıklayıcısı ile anlık görüntüleri görüntüleme hakkında bilgi edinin.
ms.custom: ''
ms.date: 02/11/2019
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
ms.openlocfilehash: 6eb7af4ead7cd58a0ccf36cbeb2b9fc56e890315
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68415742"
---
# <a name="debug-live-aspnet-azure-kubernetes-services-using-the-snapshot-debugger"></a>Snapshot Debugger kullanarak canlı ASP.NET Azure Kubernetes hizmetlerinde hata ayıklayın

Snapshot Debugger, ilgilendiğiniz kod yürütüldüğünde, üretim uygulamalarınızı anlık görüntüsünü alır. Bir anlık görüntüsünü almak için hata ayıklayıcı açmasını sağlamak için anlık görüntü noktaları ve günlüğe kaydetme noktaları kodunuzda ayarlayın. Hata ayıklayıcı, tam olarak üretim uygulamanızın trafiğini etkilemeden, çıktığına görmenizi sağlar. Snapshot Debugger, üretim ortamlarında ortaya çıkan sorunları çözmek için gereken süreyi ciddi ölçüde azaltmaya yardımcı olabilir.

Anlık görüntü noktaları ve günlüğe kaydetme noktaları da kesme noktaları için benzerdir, ancak kesme noktalarının aksine, anlık görüntü noktaları uygulamayı durdurmak yok isabet edildiğinde. Genellikle, bir anlık görüntü noktası bir anlık görüntüye yakalama 20 10 milisaniye cinsinden alır.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Snapshot Debugger'ı Başlat
> * Bir anlık görüntü noktası ayarlayın ve bir anlık görüntüyü Göster
> * Bir günlüğe kaydetme noktası ayarlayın

## <a name="prerequisites"></a>Önkoşullar

* Azure Kubernetes Hizmetleri için Snapshot Debugger yalnızca **Azure geliştirme iş yüküyle**Visual Studio 2019 Enterprise veya üzeri sürümlerde kullanılabilir. ( **Tek tek bileşenler** sekmesinde, **hata ayıklama ve test** > **anlık görüntü hata ayıklayıcısı**altında bulabilirsiniz.)

    Henüz yüklenmemişse, [Visual Studio 2019 Enterprise](https://visualstudio.microsoft.com/vs/)'ı yükleme.

* Anlık görüntü koleksiyonu, aşağıdaki Azure Kubernetes Hizmetleri Web uygulamaları için kullanılabilir:
  * .NET Core 2,2 veya üzeri sürümlerde çalışan uygulamaları ASP.NET Core.
  * .NET Core 2,2 veya üzeri sürümlerde alp 3,8 üzerinde çalışan uygulamalar ASP.NET Core.
  * Ubuntu 18,04 üzerinde .NET Core 2,2 veya üzeri sürümlerde çalışan uygulamalar ASP.NET Core.

    > [!NOTE]
    > AKS 'de Snapshot Debugger desteğini etkinleştirmenize yardımcı olması için [, Docker görüntülerinin kurulumunu gösteren bir Dockerfiles kümesi içeren bir depo](https://github.com/Microsoft/vssnapshotdebugger-docker)sağladık.

## <a name="open-your-project-and-start-the-snapshot-debugger"></a>Snapshot Debugger'ı başlatın ve projenizi açın

1. Anlık görüntü hata ayıklama için istediğiniz projeyi açın.

    > [!IMPORTANT]
    > Hata ayıklamanın anlık görüntüsünü almak için Azure Kubernetes hizmetinize yayınlanan *kaynak kodu sürümünü* açmanız gerekir.

1. **Hata ayıkla > Snapshot Debugger Ekle...** seçeneğini belirleyin. Web uygulamanızın dağıtıldığı AKS kaynağını ve bir Azure Depolama hesabını seçin ve ardından **Ekle**' ye tıklayın. Snapshot Debugger Ayrıca, [](debug-live-azure-applications.md) [sanal makine ölçek kümelerini & Azure App Service ve Azure sanal makinelerini (VM)](debug-live-azure-virtual-machines.md)destekler.

    ![Hata ayıklama menüsünden Snapshot Debugger 'ı başlatın](../debugger/media/snapshot-debug-menu-attach.png)

    ![Azure kaynağı seçin](../debugger/media/snapshot-select-azure-resource-aks.png)

    > [!NOTE]
    > (Visual Studio 2019 sürüm 16,2 ve üstü) Snapshot Debugger Azure bulut desteğini etkinleştirdi. Seçtiğiniz Azure kaynağının ve Azure depolama hesabının aynı buluttan olduğundan emin olun. Kuruluşunuzun [Azure uyumluluk](https://azure.microsoft.com/overview/trusted-cloud/) yapılandırmalarına ilişkin sorularınız varsa lütfen Azure yöneticinize başvurun.

Visual Studio anlık hata ayıklama modu sunulmuştur.

   ![Anlık görüntü hata ayıklama modu](../debugger/media/snapshot-message.png)

   **Modüller** penceresi, tüm modüllerin Azure App Service için ne zaman yüklendiğini gösterir (Bu pencereyi açmak için **Windows > modülleri > Hata Ayıkla** ' yı seçin).

   ![Modüller penceresini denetleyin](../debugger/media/snapshot-modules.png)

## <a name="set-a-snappoint"></a>Bir anlık görüntü noktası ayarlayın

1. Kod Düzenleyicisi 'nde, bir anlık görüntü noktası ayarlamak için ilgilendiğiniz kod satırının yanındaki sol cilt payı tıklatın. Uygulamasının çalıştırabildiğinizi bildiğiniz kodun olduğundan emin olun.

   ![Bir anlık görüntü noktası ayarlayın](../debugger/media/snapshot-set-snappoint.png)

1. Tıklayın **toplamaya Başla** anlık görüntü noktasını etkinleştirmek için.

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

Bu öğreticide, Azure Kubernetes için Snapshot Debugger kullanmayı öğrendiniz. Bu özellik hakkında daha fazla bilgi okumak isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Anlık görüntü hatalarını ayıklama hakkında SSS](../debugger/debug-live-azure-apps-faq.md)