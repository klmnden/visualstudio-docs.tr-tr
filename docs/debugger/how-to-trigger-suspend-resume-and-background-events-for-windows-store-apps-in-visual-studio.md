---
title: UWP hata ayıklarken askıya alma/sürdürülme/arka plan olaylarını Tetikle
ms.custom: seodec18
ms.date: 01/16/2018
ms.topic: conceptual
f1_keywords:
- vs.debug.error.background_task_activate_failure
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: 8f5f650860c520f5fbe62ff49bbbb6190e163af8
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925469"
---
# <a name="how-to-trigger-suspend-resume-and-background-events-while-debugging-uwp-apps-in-visual-studio"></a>Nasıl tetikleyeceğinizi askıya alma, sürdürme ve UWP uygulamaları Visual Studio'da hata ayıklarken arka plan olayları

Ne zaman değil ayıkladığınız Windows **işlem ömrü Yönetimi** (PLM), uygulamanızın yürütme durumunu denetler — başlatma, askıya alma, sürdürme ve uygulama yanıt kullanıcı eylemleri ve cihaz durumu olarak sonlandırılıyor. Windows hata ayıklaması yapıyorsanız, bu etkinleştirme olaylarını devre dışı bırakır. Bu konu, hata ayıklayıcı bu olayları tetiklemesine açıklar.

Bu konuda ayrıca hata ayıklama işlemini açıklamaktadır **arka plan görevleri**. Arka plan görevleri, uygulamanız çalışmıyor olsa bile, bir arka plan işleminde belirli işlemleri gerçekleştirmenize olanak tanır. Uygulamanızı hata ayıklama moduna için hata ayıklayıcı kullanabilirsiniz ve ardından — UI başlatmadan — başlatın ve arka plan görevinin hatalarını ayıklama.

Işlem ömrü yönetimi ve arka plan görevleri hakkında daha fazla bilgi için bkz. [başlatma, sürdürme ve çoklu görev](/windows/uwp/launch-resume/index).

## <a name="BKMK_Trigger_Process_Lifecycle_Management_events"></a> Tetikleyici işlem ömrü Yönetimi olayları
 Windows, Kullanıcı bu bilgisayardan uzaklaştığınızda veya Windows düşük güç durumuna girdiğinde uygulamanızı askıya alabilir. Yanıt verebilirsiniz `Suspending` olay kalıcı depolama için ilgili uygulama ve kullanıcı verileri kaydetmeyi ve kaynaklar serbest bırakılacaksa. Ne zaman uygulama sürdürüldü gelen **askıya alındı** durum geçirilmeden **çalıştıran** durum ve askıya alındığında sırada nerede olduğu gelen devam eder. Yanıt verebilirsiniz `Resuming` geri yüklemek veya uygulama durumunu yenileyin ve kaynaklarınızı geri kazanmanız için olay.

 Bellekte mümkün olduğunca çok askıya alınan uygulamaları korumak Windows çalışır ancak bellekte tutmak için yeterli kaynak yoksa Windows uygulamanızı sonlandırabilirsiniz. Bir kullanıcı da açıkça uygulamanızı kapatabilirsiniz. Kullanıcı bir uygulamanın kapatıldığını belirten özel olay yok.

 Visual Studio hata ayıklayıcıda, el ile askıya alma, sürdürme ve uygulamalarınızın yaşam döngüsü olayları işleme hata ayıklama sonlandırın. Bir işlem yaşam döngüsü olayı hata ayıklamak için:

1. Hata ayıklamak istediğiniz olayın işleyicisinde bir kesme noktası ayarlayın.

2. Hata ayıklamaya başlamak için **F5**'e basın.

3. Üzerinde **hata ayıklama konumu** araç ateşlenmesine istediğiniz olayı seçin:

     ![Askıya alma, sürdürülme, sonlandırma ve arka plan görevleri](../debugger/media/dbg_suspendresumebackground.png)

     **Askıya al ve Sonlandır** , uygulamayı kapatır ve hata ayıklama oturumunu sonlandırır.

## <a name="BKMK_Trigger_background_tasks"></a> Tetikleyici arka plan görevleri
 Herhangi bir uygulama bile uygulama çalışmıyorken belirli sistem olaylara yanıt vermek için bir arka plan görevi olarak kaydedebilirsiniz. Arka plan görevleri doğrudan kullanıcı Arabirimi güncelleştirmeleri kod çalıştıramazsınız; Bunun yerine, bunlar kullanıcıya güncelleştirmeleri kutucuk, rozet güncelleştirmeleri ve kutlama bildirimleri için bilgileri gösterir. Daha fazla bilgi için bkz. [uygulamanızı arka plan görevleriyle destekleme](https://msdn.microsoft.com/library/4c7bb148-eb1f-4640-865e-41f627a46e8e).

 Uygulamanız için arka plan görevleri, hata ayıklayıcı'dan başlayan olayları tetikleyebilir.

> [!NOTE]
> Hata ayıklayıcı, cihaz durumu değişikliği belirten olaylar gibi verileri içermeyen olayları tetikleyebilir. Kullanıcı girişini veya diğer veri gerektiren bir arka plan görevleri el ile tetiklemek sahip.

 Uygulamanız çalışmıyorken bir arka plan görev olayı tetiklemek için en gerçekçi yoludur. Ancak, standart hata ayıklama oturumunda olarak olay tetiklemeyi de desteklenir.

### <a name="BKMK_Trigger_a_background_task_event_from_a_standard_debug_session"></a> Standart hata ayıklama oturumunda bir arka plan görevi olay tetikleme

1. Arka plan görevi kodda hata ayıklamak istediğiniz bir kesme noktası ayarlayın.

2. Tuşuna **F5** hata ayıklama başlatılamıyor.

3. Üzerinde olaylar listesinden **hata ayıklama konumu** araç başlamak istiyorsanız arka plan görevi seçin.

     ![Askıya alma, sürdürülme, sonlandırma ve arka plan görevleri](../debugger/media/dbg_suspendresumebackground.png)

### <a name="BKMK_Trigger_a_background_task_when_the_app_is_not_running"></a> Uygulamayı çalışır durumda değilken bir arka plan görevi tetikleyin

1. Arka plan görevi kodda hata ayıklamak istediğiniz bir kesme noktası ayarlayın.

2. Başlangıç projesi için hata ayıklama özellik sayfasını açın. Çözüm Gezgini'nde projeyi seçin. Üzerinde **hata ayıklama** menüsünde seçin **özellikleri**.

     Projeler C++ Için **yapılandırma özellikleri** ' ni genişletin ve **hata ayıklama**öğesini seçin.

3. Aşağıdakilerden birini yapın:

    - Visual C# ve Visual Basic projeleri seçin **başlatma, ancak başlatıldığında kodumda Hata Ayıkla**

         ![C&#35;&#47;VB hata ayıklama başlatma uygulama özelliği](../debugger/media/dbg_csvb_dontlaunchapp.png "DBG_CsVb_DontLaunchApp")

    - Görsel C++ projeler için, **Uygulamayı Başlat** listesinden **Hayır** ' ı seçin.

         ![C&#43;&#43;&#47;VB başlatma uygulama hata ayıklama özelliği](../debugger/media/dbg_cppjs_dontlaunchapp.png "DBG_CppJs_DontLaunchApp")

4. Tuşuna **F5** uygulama hata ayıklama moduna yerleştirilecek. Not **işlem** listesini **hata ayıklama konumu** araç, hata ayıklama modunda olduğunu belirtmek için uygulama paketi adı görüntüler.

     ![Arka plan görev işlemi listesi](../debugger/media/dbg_backgroundtask_processlist.png "DBG_BackgroundTask_ProcessList")

5. Üzerinde olaylar listesinden **hata ayıklama konumu** araç başlamak istiyorsanız arka plan görevi seçin.

     ![Askıya alma, sürdürme, sonlandırma ve arka plan görevleri](../debugger/media/dbg_suspendresumebackground.png "DBG_SuspendResumeBackground")

## <a name="BKMK_Trigger_Process_Lifetime_Management_events_and_background_tasks_from_an_installed_app"></a> İşlem ömrü yönetimi olaylarını tetiklemek ve arka plan görevleri yüklü bir uygulamadan
 Kullanım **yüklenen uygulama paketinin hatalarını ayıklama** hata ayıklayıcıya zaten yüklü bir uygulama yüklemek için iletişim kutusu. Örneğin, Microsoft Store yüklü olduğu bir uygulamanın hatalarını ayıklamak veya uygulama için kaynak dosyaları, ancak değil uygulama için Visual Studio projesi varsa, bir uygulamanın hatalarını ayıklamak. **Yüklü uygulama paketini hata ayıkla** iletişim kutusu, Visual Studio makinesinde veya uzak bir cihazda hata ayıklama modunda bir uygulamayı başlatabilir veya uygulamayı hata ayıklama modunda çalışacak ancak başlatmanıza izin verir. Daha fazla bilgi için [yüklü uygulama paketinin hatalarını ayıklama](../debugger/debug-installed-app-package.md).

 Hata ayıklayıcıya uygulama yüklendikten sonra yukarıda açıklanan yordamlardan herhangi birini kullanabilirsiniz.

## <a name="BKMK_Diagnosing_background_task_activation_errors"></a> Arka plan görevi etkinleştirmesi hatalarını tanılama
 Arka plan altyapısı için Windows Olay Görüntüleyicisi 'de tanılama günlükleri, arka plan görev hatalarını tanılamak ve gidermek için kullanabileceğiniz ayrıntılı bilgiler içerir. Günlüğü görüntülemek için:

1. Olay Görüntüleyici uygulamasını açın.

2. İçinde **eylemleri** bölmesinde seçin **görünümü** emin **Analitik ve hata ayıklama günlüklerini göster** denetlenir.

3. Üzerinde **Olay Görüntüleyicisi'ni (yerel)** ağacında, düğümleri genişletin **uygulama ve hizmet günlükleri** > **Microsoft** > **Windows**   >  **BackgroundTasksInfrastructure**.

4. Seçin **tanılama** günlük.

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio ile UWP uygulamalarını test etme](../test/testing-store-apps-with-visual-studio.md)
- [Visual Studio’da uygulamaların hatalarını ayıklama](/visualstudio/debugger/debugging-windows-store-and-windows-universal-apps)
- [Uygulama yaşam döngüsü](/windows/uwp/launch-resume/app-lifecycle)
- [Başlatma, sürdürme ve çoklu görev gerçekleştirme](/windows/uwp/launch-resume/index)