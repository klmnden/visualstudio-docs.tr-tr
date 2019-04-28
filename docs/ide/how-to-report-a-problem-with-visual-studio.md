---
title: Visual Studio ile ilgili bir sorun bildirme
description: Visual Studio ile ilgili bir sorun bildirme öğrenin
ms.date: 03/11/2018
ms.topic: conceptual
ms.assetid: bee01179-cde5-4419-9095-190ee0ba5902
ms.author: seiyer
author: seaniyer
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2b130c321e57cdeea6b703b0e439d6b0f15a1a96
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62947715"
---
# <a name="how-to-report-a-problem-with-visual-studio-or-visual-studio-installer"></a>Visual Studio veya Visual Studio Yükleyicisi ile ilgili bir sorun bildirme

> [!NOTE]
> Mac için Visual Studio için bkz: [Mac için Visual Studio'da bir sorun bildirme](/visualstudio/mac/report-a-problem).

Bunların içerdiği geri bildirim aracını kullanarak Visual Studio ya da yükleyicisi bir sorun bildirebilir. Geri bildirim aracı, tanılama bilgilerini bildiriminizi kolayca dahil etmenize imkan sağlar ve sorunları daha etkili bir şekilde tanılayıp Visual Studio takımlar yardımcı olur. Bir sorunu bildirmek için adımlar aşağıda verilmiştir.

1. **Visual Studio'da**, sağ üst köşede bulunan geri bildirim simgesini seçin ve seçin, bir sorun bildirin. Geri bildirim aracını menüsünden erişebilirsiniz **yardımcı** > **geri bildirim gönder** > **sorun bildir**.
![Bir sorun açılır pencere üzerinde Visual Studio Geliştirici topluluğu rapor](media/vsfeedbackentry.png) alternatif olarak, olası bir sorunu rapor **Visual Studio yükleyicisi** Visual Studio yükleyemezsiniz ya da Visual Studio geri bildirim aracında erişemiyor .  Yükleyici, sağ üst köşede bulunan geri bildirim simgesini seçin ve sorun bildir seçin.
![Visual Studio Geliştirici topluluğu üzerinde bir sorun açılan rapor](media/installer.png)

1. İmzalı değil, seçin **oturum** aşağıdaki ekran görüntüsünde gösterildiği gibi. Oturum açın ekrandaki yönergeleri izleyin.

   ![Bir sorunu bildirmek oturum açın](../ide/media/sign-in-new-ux.png)

   Yalnızca oturum açtınız ancak ayrıca oy verin ve açıklama üzerinde mevcut olan herhangi bir Geri bildiriminiz sorun bildirin.

1. Oturum açtıktan sonra görmek mümkün olmayacak, **sorunları** ve **etkinlik** üzerinde **takip ettiğim öğeler** ekranı

   ![Takip ettiğim öğeler](../ide/media/items-i-follow.png)

1. Visual Studio sorununuz için arama yapın ve başkalarının bunu bildiren, görmek için bir arabirim sağlar. Birisi bildirdi ise "yukarı-bize bildirmek için oy".
   > [!NOTE]
   > Aramak için arama kutusunu ve ENTER'a tıklayın istediğiniz metni girin veya arama simgesine basın.

   ![Arama ve benzer sorunlar için oy](../ide/media/search-and-vote.png)

1. Karşılaştığınız sorun bulamazsanız seçin **yeni sorun bildirme** ekranın alt kısmındaki.

   > [!NOTE]
   > **Yeni sorun bildirme** düğmesi yalnızca Visual Studio arabiriminde Geliştirici topluluğu için görünür. Doğrudan bir sorun raporlayamaz [Geliştirici topluluğu](https://developercommunity.visualstudio.com/) Web sitesi.

1. Doğru Visual Studio ekibine için yardımcı olacak sorun için açıklayıcı bir başlık oluşturun.

1. Bize ek ayrıntılar verin ve mümkünse sorunu yeniden oluşturma adımlarını sağlayın.

   ![Yeni sorun bildirin](../ide/media/report-new-problem.png)

1. Seçin **sonraki** taşımak için **ekleri** sekmesi. Burada, Microsoft'a göndermek için geçerli ekranınızın yakalayabilirsiniz. Ek ekran görüntüleri veya diğer dosyaları eklemek için seçtiğiniz **ek dosyalar iliştirmek**.

   ![Visual Studio sorun raporu için bir ekran ekleme](media/report-a-problem-screenshot.png)

1. Bir ekran eklemek istemiyorsanız veya [istiyorduk kayıt](#record-a-repro)seçin **sonraki** taşımak için **özeti** sekmesi.

1. Seçin **Gönder** raporunuzu tüm görüntü ve izleme ya da döküm dosyaları birlikte gönderilecek. (Varsa **Gönder** düğmesi gri, bir başlık ve açıklama raporun sağladığınızdan emin olun.)

   Hangi verinin toplanması hakkında daha fazla bilgi için bkz: [topladığımız veriler](developer-community-privacy.md#data-we-collect).

## <a name="record-a-repro"></a>Bir yineleme kaydedin

İzleme ve yığın dökümü dosyaları, sorunları tanılamamıza yardımcı yararlıdır. Kullandığınızda, bildiriminizden **sorun bildir** yeniden oluşturma adımlarınızı kaydetmek ve Microsoft'a veri göndermek için aracı. Bunun nasıl yapılacağı aşağıda verilmiştir:

1. Sorununuz için bir başlık ve açıklama girin, sonra seçin **sonraki** taşımak için **ekleri** sekmesi.

1. Seçin **kayıt** sekmesi.

1. Altında **eylemlerinizi kaydedin**, sorunu yeniden oluşturmak, geçerli Visual Studio örneğini seçin. Visual Studio kilitleniyorsa, örneğin olamaz, seçin  **\<yeni bir örnek oluşturun >** eylemleri Visual Studio'nun yeni bir örneğini kaydetmek için.

1. Seçin **kaydı Başlat**. Aracı çalıştırmak için izni verin.

   ![İzleme ve yığın döküm dosyasını Visual Studio sorun raporunda sağlamak için "kaydı Başlat" ı seçin](../ide/media/record-dialog-box.png)

1. Zaman **adımları Kaydedici** aracı görüntülenir, sorunu yeniden oluşturma adımları gerçekleştirin.

1. İşiniz bittiğinde seçin **kaydı durdurmak** düğmesi.

1. Toplama ve kaydettiğiniz bilgileri paketlemek Visual Studio için birkaç dakika bekleyin.

   Hangi verinin toplanması hakkında daha fazla bilgi için bkz: [topladığımız veriler](developer-community-privacy.md#data-we-collect).

## <a name="when-further-information-is-needed-need-more-info"></a>Ne zaman ek bilgiler (daha fazla bilgi gerekiyor) gereklidir

Visual Studio 2017 sürüm 15.5 sürümünde başlayarak, sorun raporları hakkında ek bilgiler sağlayan kullanıcılara yardımcı olmak için yeni bir iş akışı yok.

1. Ne zaman bir Microsoft mühendisi ayarlar [Visual Studio Geliştirici topluluğu](https://developercommunity.visualstudio.com/) için sorun **daha fazla bilgi gerekiyor** durum, gönderilen, oy, ardından veya sorunu açıklamalı herhangi bir kullanıcı bir bildirim alır **Bir sorun bildirme** Visual Studio'daki aracı.

   ![Visual Studio'da daha fazla bilgi bildirim gerekir](../ide/media/nmi-notification.png)

1. Tıklayarak **sorunları görüntüle** filtreleme ve dikkat gerektiren sorunlar görünümü sıralama için bağlantı. Bu sorunları yanında bir göstergesi de, ayırt etmek için bunları genel arayın.

1. Görüntüleme sorun ayrıntıları görmek için bir sorun tıklayın.

   ![Daha fazla bilgi bildirim gerekir](../ide/media/nmi-details-view.png)

1. Görüntülenecek **daha fazla bilgi gerekiyor** İste'ye tıklayın **kendi isteği görüntüleyin ve yanıt** sorun Ayrıntıları görünümünde bağlantı. İstek bir iletişim kutusu gösterir.

   ![Daha fazla bilgi bildirim gerekir](../ide/media/nmi-request.png)

1. Açıklamalar, ekler veya kayıt adımları ekleyerek daha fazla bilgi sağlayabilir. Bu deneyim, yeni sorun bildirme veya bir sorunu oylama sırasında ek bilgi sağlayarak benzerdir.

1. İstekte bulunan Microsoft mühendisi, ek bilgilerle hakkında bir bildirim alır. Bunlar araştırmak için yeterli bilgi varsa, sorunu durumu değişir. Aksi takdirde, mühendislik bile daha fazla bilgi için sorar.

   > [!NOTE]
   > * Yanıt, bildirim kaybolur. Bunun yerine, size teşekkür eder ve daha fazla bilgi sağlamak için bir yol kolaylaştıran bir başlık görürsünüz.
   > * Bildirim sorunu değişiklikleri durumu sorunu aşağıdaki herkes için kaybolduktan sonra.
   > * Birden fazla kişi aynı yanıtlayabilir **daha fazla bilgi gerekiyor** isteği.
   > * Hiç bir **daha fazla bilgi gerekiyor** akışında [Geliştirici topluluğu](https://developercommunity.visualstudio.com/) zaman doğrudan bir web tarayıcısı üzerinden erişim, ancak yorumlar ve orada ekler de sağlayabilirsiniz.

## <a name="search-for-solutions-or-provide-feedback"></a>Çözümler için arama yapın veya geri bildirimde bulunun

İstemediğiniz veya Visual Studio, bir sorunu bildirmek için kullanılamaz, yoktur sorun zaten bildirilmiştir şansı ve üzerinde gönderilen çözüm [Visual Studio Geliştirici topluluğu](https://developercommunity.visualstudio.com/) sayfası.

Rapor, ancak bir özellik önermek istediğiniz bir sorun yoksa yoktur, bir yer çok. Daha fazla bilgi için [özellik önerin](https://developercommunity.visualstudio.com/content/idea/post.html?space=8) sayfası.

## <a name="see-also"></a>Ayrıca bkz.

* [Bizimle iletişime geçin](../ide/talk-to-us.md)
* [Mac için Visual Studio ile ilgili bir sorun bildirin](/visualstudio/mac/report-a-problem)
* [C++ ile ilgili sorun](/cpp/how-to-report-a-problem-with-the-visual-cpp-toolset)
* [Visual Studio Geliştirici topluluğu](https://developercommunity.visualstudio.com/)
* [Geliştirici topluluğu veri gizliliği](developer-community-privacy.md)
