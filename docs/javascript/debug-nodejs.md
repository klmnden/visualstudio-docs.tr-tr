---
title: JavaScript veya TypeScript uygulamasında hata ayıklama
description: Visual Studio, JavaScript ve TypeScript uygulamaları Visual Studio'da hata ayıklama için destek sağlar
ms.date: 12/03/2018
ms.topic: conceptual
ms.devlang: javascript
author: mikejo5000
ms.author: mikejo
manager: jillfra
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: abfe762b354d11297aa4d0c574b8f0e0a081d349
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63438004"
---
# <a name="debug-a-javascript-or-typescript-app-in-visual-studio"></a>Visual Studio JavaScript veya TypeScript bir uygulamada hata ayıklama

Visual Studio kullanarak, JavaScript ve TypeScript kodu hata ayıklaması yapabilirsiniz. Ayarlayabilir ve kesme noktaları isabet, hata ayıklayıcının, değişkenlerini incelemek, çağrı yığınını görüntüleme ve diğer hata ayıklama özelliklerini kullanın.

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/) ücretsiz yüklemek için sayfa. Uygulama geliştirme yaptığınız türüne bağlı olarak, yüklemeniz gerekebilir **Node.js geliştirme iş yükü** Visual Studio ile.

## <a name="debug-server-side-script"></a>Sunucu tarafı komut dosyası hata ayıklama

1. Projenizi Visual Studio'da açın, sunucu tarafı JavaScript dosyasını açın (örneğin *server.js*), cilt payını sol kanaldaki bir kesme noktası ayarlamak için tıklayın:

    ![Bir kesme noktası ayarlayın](../javascript/media/tutorial-nodejs-react-set-breakpoint.png)

    Kesme noktaları güvenilir hata ayıklama en temel hem de temel özelliğidir. Bir kesme noktası değişkenlerin değerleri veya bellek davranışını göz olabilmesi için Visual Studio çalışan kodunuzu nereye askıya almanız ya da bir dal kod getting run olup olmadığını gösterir.

1. Uygulamanızı çalıştırmak için basın **F5** (**hata ayıklama** > **hata ayıklamayı Başlat**).

    Hata ayıklayıcı, kesme noktasında duraklatır (sarı renkli geçerli deyim işaretlenmiştir) kümesi. Şimdi, uygulama durumunuzu şu anda, kapsamındaki değişkenlerin üzerine gelerek gibi hata ayıklayıcı penceresini kullanarak inceleyebilirsiniz **Yereller** ve **Watch** windows.

1. Tuşuna **F5** uygulamaya devam etmek için.

1. Chrome geliştirme araçları veya F12 araçları kullanmak istiyorsanız, basın **F12**. DOM inceleyin ve JavaScript Konsolu'nu kullanarak uygulama ile etkileşim kurmak için bu araçları kullanabilirsiniz.

## <a name="debug-client-side-script"></a>İstemci tarafı betikte hata ayıklama

Visual Studio yalnızca Chrome ve Internet Explorer için hata ayıklama desteği sağlar. Bazı senaryolarda, hata ayıklayıcı kesme noktaları JavaScript ve TypeScript kodu ve HTML dosyaları ekli komut otomatik olarak kullanılabilir.

Kaynağınızı küçültülmüş ya da bir transpiler TypeScript veya Babel, kullanımı gibi tarafından oluşturulan [kaynak eşlemeleri](#generate_sourcemaps) en iyi hata ayıklama deneyimi için gereklidir. Kaynak eşlemeleri ' bir çalışan istemci tarafı komut dosyası hata ayıklayıcı hala ekleyebilirsiniz. Ancak, yalnızca ayarlayın ve küçültülmüş veya transpiled dosyasında, özgün kaynak dosyası değil, kesme noktaları isabet mümkün olabilir. Örneğin, bir Vue.js uygulamasında küçültülmüş komut bir dize olarak geçilen bir `eval` deyimi ve kaynak eşlemeleri kullanmadığınız sürece etkin Visual Studio hata ayıklayıcısını kullanarak bu kodda adım adım bir yolu yoktur. Karmaşık bazı hata ayıklama senaryolarda, Microsoft Edge için Chrome geliştirme araçları veya F12 araçları da kullanabilirsiniz.

Visual Studio ve istemci tarafı kod kesme noktaları isabet hata ayıklayıcıyı iliştirmek için hata ayıklayıcı genellikle doğru işlemi tanımlamak için Yardım gerekiyor. Bu Chrome kullanarak etkinleştirmek için yöntemlerinden biri aşağıda verilmiştir.

### <a name="attach-the-debugger-to-client-side-script-using-chrome"></a>Chrome kullanarak istemci tarafı komut dosyası için hata ayıklayıcının

1. Tüm Chrome pencerelerini kapatın.

    Chrome hata ayıklama modunda çalıştırmadan önce bu eylem gerekli değildir.

2. Açık **çalıştırma** Windows komutunu **Başlat** düğmesine (sağ tıklatın ve seçin **çalıştırma**) ve aşağıdaki komutu girin:

    `chrome.exe --remote-debugging-port=9222`

    Bu komut, hata ayıklama etkin olan Chrome başlatır.

    ::: moniker range=">=vs-2019"

    > [!NOTE]
    > Ayrıca `--remote-debugging-port` seçerek tarayıcı başlatma bayrağı **şununla Gözat...**  > öğesinden **hata ayıklama** ardından araç çubuğunda **Ekle**ve ardından bayrağı ayarı **bağımsız değişkenleri** alan. Tarayıcı için farklı bir kolay ad gibi kullanın **Chrome ile hata ayıklama**. Ayrıntılar için bkz [sürüm notları](https://docs.microsoft.com/visualstudio/releases/2019/release-notes-preview#browser-cli-params-support).

    ::: moniker-end

3. Visual Studio'ya geçiş yapın ve kaynak kodunuzda bir kesme noktası ayarlayın. (Kesme noktaları, gibi veren kod satırında kesme noktası ayarlamak bir `return` deyimi veya bir `var` bildirimi).

    ![Bir kesme noktası ayarlayın](../javascript/media/tutorial-nodejs-react-set-breakpoint-client-code.png)

    Büyük, oluşturulan bir dosyada belirli kodu bulmak ihtiyacınız varsa **Ctrl**+**F** (**Düzenle** > **Değiştir**  >  **Hızlı Bul**).

4. Visual Studio'da hata ayıklama hedefi olarak seçilen Chrome ile basın **Ctrl**+**F5** (**hata ayıklama** > **hata ayıklama olmadan Başlat** ) tarayıcı içinde uygulamayı çalıştırmak için.

    Uygulama yeni bir tarayıcı sekmesinde açılır.

    Chrome makinenizde kullanılabilir, ancak bir seçenek olarak görünmez, seçin **şununla Gözat** hata ayıklama hedef açılır liste ve select Chrome varsayılan tarayıcı hedefi olarak (seçin **varsayılan olarak ayarla**).

5. Seçin **hata ayıklama** > **işleme**.

6. İçinde **iliştirme** iletişim kutusunda **WebKit kod** içinde **ekleme** alanına **chrome** filtrelemek için filtre kutusundaki arama sonucu.

    **WebKit kod** Webkit tabanlı bir tarayıcı Chrome için gerekli değerdir.

7. Doğru konak Chrome işlemle (Bu şekildeki 1337) bağlantı noktası seçin seçip **iliştirme**.

    ![İşleme](../javascript/media/tutorial-nodejs-react-attach-to-process.png)

    DOM Gezgini ve JavaScript Konsolu Visual Studio'da açtığınızda hata ayıklayıcı düzgün eklenmiş biliyor. Bu hata ayıklama araçları, Chrome geliştirme araçları ve Microsoft Edge için F12 araçlarındaki benzerdir.

    > [!NOTE]
    > Hata ayıklayıcıyı iliştirmek değil "işleme yüklenemiyor. iletiyi görürseniz Bir işlemi şu andaki durumunda yasal değil", Görev Yöneticisi'ni kullanarak hata ayıklama modu Chrome başlatmadan önce Chrome tüm örneklerini kapatın. Chrome uzantıları çalıştıran ve tam hata ayıklama modu engelliyor.

8. Kesme noktası koduyla zaten çalıştırıldığında, kesme noktasına isabet için tarayıcı sayfanızı yenileyin.

    Hata ayıklayıcıda duraklatıldığı sırada değişkenlerin gelin ve hata ayıklayıcı penceresini kullanarak, uygulama durumunu inceleyebilirsiniz. Hata ayıklayıcı kod içerisinde ilerlemeye tarafından ilerletebilirsiniz (**F5**, **F10**, ve **F11**).

    Küçültülmüş için veya JavaScript transpiled, isabet ya da transpiled JavaScript dosyasında kesme ya da eşlenen konumunu (kaynak eşlemeleri kullanarak) TypeScript dosyanızda, ortam ve tarayıcı durumuna bağlı olarak. Her iki durumda da, kod içinde gezinebilmek ve değişkenleri inceleyin.

    * Bir TypeScript dosyasında break into code gerekir ve bunu, kullanın **iliştirme** hata ayıklayıcıyı iliştirmek için önceki adımlarda açıklandığı gibi. Dinamik olarak üretilen TypeScript dosyayı açarak Çözüm Gezgini'nden açın **betik belgelerini** > **filename.tsx**, bir kesme noktası ayarlayın ve tarayıcınızda sayfayı yenileyin (ayarlayın kesme noktaları, gibi veren kod satırında kesme noktası `return` deyimi veya bir `var` bildirimi).

        Bir TypeScript dosyası veya olan yapmak yüklenemiyor'break into code gerekiyorsa, bunun yerine, kullanmayı deneyin `debugger;` TypeScript deyiminde dosya veya Chrome geliştirici araçları kesme noktaları ayarlayın.

    * Break into code transpiled JavaScript dosyasında ihtiyacınız varsa (örneğin, *uygulama bundle.js*) ve bunu, kaynak eşleme dosyası Kaldır *filename.js.map*.

     > [!TIP]
     > Aşağıdaki adımları izleyerek ilk kez eklediğiniz işleme sonra hızlı bir şekilde aynı işleme seçerek iliştirebilirsiniz **hata ayıklama** > **İliştir**.

## <a name="generate_sourcemaps"></a> Hata ayıklama için kaynak eşlemeleri üret

Visual Studio kullanın ve JavaScript kaynak dosyaları kaynak eşlemeleri üret yeteneğine sahiptir. Bu genellikle kaynak küçültülmüş ya da bir transpiler TypeScript veya Fish gibi tarafından oluşturulan gereklidir. Kullanılabilir seçenekler, proje türüne bağlıdır.

* Visual Studio'da TypeScript projesi kaynak eşlemeleri, varsayılan olarak oluşturur.

* Bir JavaScript projesinde bir bundler gibi Web projenize eklediğiniz bir derleyici TypeScript derleyicisi (veya Babel) gibi kullanıp Kaynak eşlemeleri üret gerekir. Ayrıca eklemelisiniz TypeScript derleyicisi için bir *tsconfig.json* dosya. Temel Web yapılandırması kullanılarak bunun nasıl yapılacağını gösteren bir örnek için bkz: [React ile Node.js uygulaması oluşturma](../javascript/tutorial-nodejs-with-react-and-jsx.md).

> [!NOTE]
> Okuyun, kaynak eşlemeleri için yeni [JavaScript kaynak eşlemelerinin giriş](https://www.html5rocks.com/en/tutorials/developertools/sourcemaps/) devam etmeden önce.

Kaynak haritaları için Gelişmiş ayarları yapılandırmak için ya da kullanmak bir *tsconfig.json* veya proje ayarlarını bir TypeScript projesi, ancak ikisine birden değil.

### <a name="configure-source-maps-using-a-tsconfigjson-file"></a>Bir tsconfig.json dosyası kullanarak kaynak eşlemeleri yapılandırma

Eklerseniz bir *tsconfig.json* dosya Visual Studio projenize bir TypeScript projesi olarak kök dizinini değerlendirir. Bir dosyayı eklemek için Çözüm Gezgini'nde projenize sağ tıklayın ve ardından **Ekle > Yeni Öğe > Web > betikleri > TypeScript JSON yapılandırma dosyası**. A *tsconfig.json* aşağıdaki projenize eklendikten gibi dosya.

```json
{
  "compilerOptions": {
    "noImplicitAny": false,
    "noEmitOnError": true,
    "removeComments": false,
    "sourceMap": true,
    "target": "es5"
  },
  "exclude": [
    "node_modules",
    "wwwroot"
  ]
}
```

#### <a name="compiler-options-for-tsconfigjson"></a>Tsconfig.json için derleyici seçenekleri

* **inlineSourceMap**: Her kaynak dosyası için ayrı bir kaynak eşlemesi oluşturmak yerine, kaynak eşlemeleri ile tek bir dosya gösterin.
* **inlineSources**: Tek bir dosya içinde kaynak eşlemeleri yanı sıra kaynak yayma; gerektirir *inlineSourceMap* veya *kaynak eşlemesi* ayarlanacak.
* **mapRoot**: Hata ayıklayıcı nereden kaynak eşlemesi konumunu belirtir (*.map*) dosyaları varsayılan konumu yerine. Bu bayrak kullanırsanız çalışma zamanı *.map* dosyaları farklı bir konumda olması gerekir *.js* dosyaları. Belirtilen konumda hata ayıklayıcı konumunu yönlendirmek için kaynak eşlemesi katıştırılmış *.map* dosyaları.
* **Kaynak eşlemesi**: Karşılık gelen oluşturur *.map* dosya.
* **sourceRoot**: Hata ayıklayıcının TypeScript dosyalarını kaynak konumlar yerine nerede konumu belirtir. Çalışma zamanı kaynakları tasarım zamanında konumdan farklı bir konumda olması gerekiyorsa bu bayrağı kullanın. Hata ayıklayıcı kaynak dosyalarının bulunduğu için doğrudan kaynak eşlemesi içinde belirtilen konuma eklenir.

Derleyici seçenekleri hakkında daha fazla ayrıntı için sayfasını gözden geçirin [derleyici seçenekleri](https://www.typescriptlang.org/docs/handbook/compiler-options.html) TypeScript el kitabı üzerinde.

### <a name="configure-source-maps-using-project-settings"></a>Proje ayarlarını kullanarak kaynak eşlemeleri yapılandırma

Projeye sağ tıklayıp ardından seçerek proje özelliklerini kullanarak kaynak eşlemesi ayarları da yapılandırabilirsiniz **Proje > Özellikler > TypeScript derleme > hata ayıklama**.

Bu proje ayarları kullanılabilir.

* **Kaynak eşlemeleri üret** (eşdeğer **kaynak eşlemesi** içinde *tsconfig.json*): Karşılık gelen oluşturur *.map* dosya.
* **Kaynak eşlemelerinin kök dizinini belirt** (eşdeğer **mapRoot** içinde *tsconfig.json*): Hata ayıklayıcının, eşlem dosyalarını üretilen konumlar yerine nerede bulmanız gerekir konumunu belirtir. Bu bayrak kullanırsanız çalışma zamanı *.map* dosyaları .js dosyalarının farklı bir konumda bulunması gerekir. Hata ayıklayıcının eşleme dosyalarının bulunduğu yere yönlendirmek için kaynak eşlemesi içinde belirtilen konuma eklenir.
* **TypeScript dosyalarının kök dizinini belirt** (eşdeğer **sourceRoot** içinde *tsconfig.json*): Hata ayıklayıcının TypeScript dosyalarını kaynak konumlar yerine nerede konumu belirtir. Çalışma zamanı kaynak dosyaları tasarım zamanında konumdan farklı bir konumda olması gerekiyorsa bu bayrağı kullanın. Hata ayıklayıcı kaynak dosyalarının bulunduğu için doğrudan kaynak eşlemesi içinde belirtilen konuma eklenir.

## <a name="debug-javascript-in-dynamic-files-using-razor-aspnet"></a>Razor (ASP.NET) kullanarak dinamik dosyaları JavaScript'te hata ayıklama

Visual Studio yalnızca Chrome ve Internet Explorer için hata ayıklama desteği sağlar. Bu otomatik olarak kesme noktaları JavaScript/TypeScript ve HTML dosyaları ekli komut bağlanacağı.

Hata ayıklama dinamik olarak üretilen dosyaları otomatik değildir. Otomatik olarak Razor sözdizimi olan (cshtml, vbhtml) oluşturulan dosyalar üzerinde kesme noktaları isabet edilemiyor. Bu tür bir dosyayı hata ayıklamak için kullanabileceğiniz iki yaklaşım vardır:

* **Bir yerde `debugger;` deyimi, kesmek istediğiniz**: Bu, yürütmeyi durdurun ve hemen bu oluşturulurken hata ayıklamayı başlatmak için dinamik betiği neden olur.
* **Sayfayı yüklemek ve Visual Studio üzerinde dinamik belge açma**: , Hata ayıklama sırasında dinamik dosyayı açmak için kesme noktası ayarlayın ve bu yöntemin çalışma sayfayı yenileyin. Olup, Chrome veya Internet Explorer kullanıyorsanız bağlı olarak, aşağıdaki stratejilerden birini kullanarak dosyayı bulabilirsiniz:

   Chrome için Git **Çözüm Gezgini > betik belgelerini > YourPageName**.

    > [!NOTE]
    > Chrome kullanırken, bir ileti alabilirsiniz **arasında hiçbir kaynak kullanılabilir \<script > etiketleri**. Bu sorun, yalnızca hata ayıklamaya devam et.

   Internet Explorer için Git **Çözüm Gezgini > betik belgelerini > Windows Internet Explorer > YourPageName**.

Daha fazla bilgi için [istemci-tarafı Google chrome'da ASP.NET projeleri hata ayıklama](https://devblogs.microsoft.com/aspnet/client-side-debugging-of-asp-net-projects-in-google-chrome/).