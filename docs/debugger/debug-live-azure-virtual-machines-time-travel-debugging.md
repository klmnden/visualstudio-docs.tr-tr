---
title: Zaman seyahat hata ayıklama Canlı ASP.NET Azure sanal makineler
description: Kayıt ve Snapshot Debugger'ı kullanarak Azure sanal makinelerinde Canlı ASP.NET uygulamaları yeniden yürütme hakkında bilgi edinin.
ms.custom: ''
ms.date: 04/11/2019
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
ms.openlocfilehash: 3a81f6aa138b361a44a272ebda3557d27a914c64
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60112363"
---
# <a name="record-and-replay-live-aspnet-apps-on-azure-virtual-machines-using-the-snapshot-debugger"></a>Kayıt ve yeniden yürütme Canlı Snapshot Debugger'ı kullanarak Azure sanal makinelerinde ASP.NET uygulamaları

Visual Studio Enterprise zaman seyahat hata ayıklama (TTD) önizlemede Azure sanal makinesi (VM) üzerinde çalışan bir Web uygulaması kaydetme olanağı sağlar doğru bir şekilde yeniden oluşturmak ve yürütme yolunu yeniden yürüt. TTD anlık görüntü hata ayıklayıcısı ile tümleşir ve yalıtmak ve üretim ortamlarında yalnızca oluşabilecek sorunları belirlemenize yardımcı olmak istediğiniz durumlar herhangi bir sayıda geri sarabilir ve kodun her satırını yeniden olanak sağlar.

TTD kaydı yakalama uygulamayı durdurmak değil. Ancak, TDD kaydı önemli ölçüde işlem boyutu ve etkin iş parçacığı sayısı temel alınarak Etkenler yavaşlatmasını, çalışan bir işleme ekler.

Bu özellik, Visual Studio 2019'ın yayınlanmasıyla birlikte bir go live lisans için önizlemeye sunulmuştur.

Bu öğreticide şunları yapacaksınız:

> [!div class="checklist"]
> * Snapshot Debugger zaman seyahat etkin hata ayıklama ile Başlat
> * Bir anlık görüntü noktası ayarlayın ve toplama bir zaman seyahat kaydetme
> * Bir zaman hata ayıklama Başlangıç kaydı seyahat

## <a name="prerequisites"></a>Önkoşullar

* Zaman seyahat Azure sanal makineler (VM) için hata ayıklama, yalnızca Visual Studio 2019 Enterprise için kullanılabilir veya üzeri ile **Azure geliştirme iş yükü**. (Altında **tek tek bileşenler** sekmesinde bulduğunuz altında **hata ayıklama ve test** > **anlık görüntü hata ayıklayıcısı**.)

    Henüz yüklü değilse, yükleme [Visual Studio 2019 Enterprise](https://visualstudio.microsoft.com/vs/).

* Seyahat süresi hata ayıklama, şu Azure VM web uygulamaları için kullanılabilir:
  * .NET Framework 4.8 veya sonraki sürümlerde çalışan ASP.NET uygulamalarından (AMD64).

## <a name="open-your-project-and-start-the-snapshot-debugger-with-time-travel-debugging-enabled"></a>Zaman seyahat hata ayıklama etkin olan anlık görüntü hata ayıklayıcıyı başlatın ve projenizi açın

1. Projeyi açmak, bir zaman toplamak istediğiniz için seyahat kaydı.

    > [!IMPORTANT]
    > Açmanıza gerek TTD başlatmak için *kaynak kodu sürümüyle aynı sürümü* Azure VM'yi hizmetinizle yayımlanır.

1. Seçin **hata ayıklama > Snapshot Debugger iliştirebilmek...** . Azure web uygulamanız için Dağıtılmış VM ve bir Azure depolama hesabı seçin. Seçin **zaman seyahat hata ayıklamayı etkinleştir** Önizleme seçeneğini ve ardından **iliştirme**.

      ![Azure kaynağı seçin](../debugger/media/time-travel-debugging-select-azure-resource-vm.png)

    > [!IMPORTANT]
    > Seçtiğiniz ilk kez **Snapshot Debugger Ekle** VM'niz için IIS otomatik olarak yeniden başlatılır.

    Meta verileri **modülleri** başlangıçta etkinleştirilmedi. Web uygulamasına gidin ve **toplamaya Başla** düğmesi sonra etkin hale gelir. Visual Studio anlık hata ayıklama modu sunulmuştur.

   ![Anlık görüntü hata ayıklama modu](../debugger/media/snapshot-message.png)

    > [!NOTE]
    > Application Insights site uzantısı, anlık görüntü hata ayıklaması da destekler. Bir "site uzantısı güncel değil" hata iletisi ile karşılaşırsanız, bkz [sorun giderme ipuçları ve anlık görüntü hata ayıklama için bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md) ayrıntıları yükseltme.

   **Modülleri** penceresi gösterir, tüm modülleri Azure VM için ne zaman yüklenir (seçin **hata ayıklama > Windows > modülleri** bu pencereyi açmak için).

   ![Modüller penceresini denetleyin](../debugger/media/snapshot-modules.png)

## <a name="set-a-snappoint-and-collect-a-time-travel-recording"></a>Bir anlık görüntü noktası ayarlayın ve toplama bir zaman seyahat kaydetme

1. Kod Düzenleyicisi'nde sol kanalda bir anlık görüntü noktası ayarlamak ilginizi çeken bir yöntemi tıklayın. Yürütecek bildiğiniz kod olduğundan emin olun.

   ![Bir anlık görüntü noktası ayarlayın](../debugger/media/time-travel-debugging-set-snappoint-settings.png)

1. Anlık görüntü noktası (boş Top) simgesine sağ tıklayın ve seçin **eylemleri**. İçinde **anlık görüntü ayarları** penceresinde tıklayın **eylem** onay kutusu. Ardından **bu yöntemin sonuna bir zaman seyahat izleme toplama** onay kutusu.

   ![Yönteminin sonuna bir zaman seyahat izleme Topla](../debugger/media/time-travel-debugging-set-snappoint-action.png)

1. Tıklayın **toplamaya Başla** anlık görüntü noktasını etkinleştirmek için.

   ![Anlık görüntü noktasını Aç](../debugger/media/snapshot-start-collection.png)

## <a name="take-a-snapshot"></a>Bir anlık görüntüsünü alın

Bir anlık görüntü noktası etkinleştirildiğinde, anlık görüntü noktası yerleştirildiği kod satırının yürütür her bir anlık görüntüsünü yakalar. Bu yürütme sunucunuzdaki gerçek bir isteği nedeni olabilir. İsabet, web sitenizin tarayıcı görünümüne gidin ve tüm eylemleri için anlık görüntü noktası zorlamak için anlık görüntü noktası ulaşılmasına neden gereklidir.

## <a name="start-debugging-a-time-travel-recording"></a>Bir zaman hata ayıklama Başlangıç kaydı seyahat

1. Anlık görüntü noktası isabet edildiğinde bir anlık görüntü tanılama araçları penceresinde görünür. Bu pencereyi açmak için seçin **hata ayıklama > Windows > tanılama araçlarını Göster**.

   ![Bir anlık görüntü noktası açın](../debugger/media/snapshot-diagsession-window.png)

1. Kod düzenleyicisinde kaydetmeyi zaman seyahat açılacak anlık görüntüsünü görüntüle bağlantısına tıklayın.
  
   Her satır kod kullanarak TTD tarafından kaydedilen yürütebilir **devam** ve **ters devam** düğmeleri. Ayrıca, **hata ayıklama** araç için kullanılabilir **Göster sonraki deyimi**, **içine adımla**, **Step Over**, **Step Out**, **Adım geri**, **üzerinden geri adım**, **adım geriye**.

   ![Hata Ayıklamayı Başlat](../debugger/media/time-travel-debugging-step-commands.png)

   Ayrıca **Yereller**, **izlemeleri**, ve **çağrı yığını** windows ve ayrıca nevyhodnocovat.

   ![Anlık görüntü verileri İnceleme](../debugger/media/time-travel-debugging-start-debugging.png)

    Web sitesinin kendisinde hala çalışıyor ve son kullanıcıların herhangi bir sonraki TTD etkinliği tarafından etkilenen değildir. Varsayılan olarak anlık görüntü noktası yalnızca bir anlık görüntüsü yakalanır: anlık görüntü yakalandıktan sonra anlık görüntü noktası devre dışı bırakır. Anlık görüntü noktası başka bir anlık görüntü yakalamak istiyorsanız, anlık görüntü noktası tıklayarak tekrar açabilirsiniz **koleksiyonu Güncelleştir**.

**Yardıma mı ihtiyacınız var?** Bkz: [sorun giderme ve bilinen sorunlar](../debugger/debug-live-azure-apps-troubleshooting.md) ve [anlık görüntü hata ayıklama ile ilgili SSS](../debugger/debug-live-azure-apps-faq.md) sayfaları.

## <a name="set-a-conditional-snappoint"></a>Koşullu bir anlık görüntü noktası ayarlayın

Uygulamanızı belirli bir durumda yeniden oluşturmak zor ise, koşullu bir anlık görüntü noktası kullanımı yardımcı olup olmadığını göz önünde bulundurun. Bir zaman'ı toplamaktan kaçınma koşullu anlık görüntü noktaları Yardım uygulama gibi bir değişken incelemek istediğiniz belirli bir değere sahip olduğunda istenen bir durum girene kadar kaydı seyahat. [İfadeler, filtreleri kullanarak koşulları ayarlayın veya isabet sayıları](../debugger/debug-live-azure-apps-troubleshooting.md).

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticide, Azure sanal makineler için kaydı zaman seyahat toplanacak öğrendiniz. Snapshot Debugger hakkında daha fazla bilgi okumak isteyebilirsiniz.

> [!div class="nextstepaction"]
> [Anlık görüntü hatalarını ayıklama hakkında SSS](../debugger/debug-live-azure-apps-faq.md)