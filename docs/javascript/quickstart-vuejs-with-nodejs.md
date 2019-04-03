---
title: 'Hızlı Başlangıç: İlk Vue.js uygulamanızı oluşturma'
description: Bu hızlı başlangıçta, Visual Studio için Node.js araçları kullanarak Visual Studio'da bir Vue.js uygulaması oluşturma
ms.custom: seodec18
ms.date: 09/24/2018
ms.topic: quickstart
ms.devlang: javascript
ms.assetid: b0e4ebed-1a01-41ef-aad1-4d8465ce5322
author: mikejo5000
ms.author: mikejo
manager: jillfra
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: d28126c84312c13b04de6739340d2cfb6337a066
ms.sourcegitcommit: 05d104a14ff357d599ff274f97cd59d464ee4a46
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/03/2019
ms.locfileid: "58897601"
---
# <a name="quickstart-use-visual-studio-to-create-your-first-vuejs-app"></a>Hızlı Başlangıç: İlk Vue.js uygulamanızı oluşturmak için Visual Studio

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), oluşturun ve basit bir Vue.js web uygulaması çalıştırın.

> [!IMPORTANT]
> Bu makalede, Visual Studio 2017 sürüm 15,8'den itibaren kullanılabilmektedir Vue.js şablon gerektirir.

## <a name="prerequisites"></a>Önkoşullar

* Visual Studio yüklü ve Node.js geliştirme iş yükü olması gerekir.

    ::: moniker range=">=vs-2019"
    Visual Studio 2019'ı henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/) ücretsiz yüklemek için sayfa.
    ::: moniker-end
    ::: moniker range="vs-2017"
    Visual Studio 2017'ı henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/) ücretsiz yüklemek için sayfa.
    ::: moniker-end

    İş yükünü yükleyin, ancak Visual Studio zaten gerekiyorsa, Git **Araçları** > **araçları ve özellikleri Al...** , Visual Studio yükleyicisi açılır. Seçin **Node.js geliştirme** iş yükü, ardından **Değiştir**.

    ![Node.js iş yükü VS yükleyicisi](../ide/media/quickstart-nodejs-workload.png)

* Node.js çalışma zamanı yüklü olması gerekir.

    LTS sürümünden yüklü yoksa, yükleme [Node.js](https://nodejs.org/en/download/) Web sitesi. Genel olarak, Visual Studio yüklü Node.js çalışma zamanı otomatik olarak algılar. Yüklü bir çalışma zamanı algılayan değil, projenizi yüklü çalışma zamanı özellikleri sayfasında başvurmak için yapılandırabilirsiniz (bir proje oluşturduğunuzda, proje düğümüne sağ tıklayın ve seçin **özellikleri**).

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, bir Vue.js web uygulaması projesi oluşturacaksınız.

1. LTS sürümü zaten yüklü olan bir Node.js çalışma zamanı yoksa, yükleme [Node.js](https://nodejs.org/en/download/) Web sitesi.

    Genel olarak, Visual Studio yüklü Node.js çalışma zamanı otomatik olarak algılar. Yüklü bir çalışma zamanı algılayan değil, projenizi yüklü çalışma zamanı özellikleri sayfasında başvurmak için yapılandırabilirsiniz (bir proje oluşturduğunuzda, proje düğümüne sağ tıklayın ve seçin **özellikleri**).

1. Visual Studio'yu açın.

1. Yeni bir proje oluşturun.

    ::: moniker range=">=vs-2019"
    Tuşuna **Esc** başlangıç penceresini kapatın. Tür **Ctrl + Q** arama kutusunu açmak için şunu yazın **temel Vue.js**, ardından **temel Vue.js Web uygulaması** (JavaScript veya TypeScript). Görünen iletişim kutusunda **Oluştur**.

    ![VUE.js şablonu](../javascript/media/vs-2019/vuejs-template.png)
    ::: moniker-end
    ::: moniker range="vs-2017"
    Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**. Sol bölmesinde **yeni proje** iletişim kutusunda **JavaScript** veya **TypeScript**, ardından **Node.js**. Orta bölmede seçin **temel Vue.js Web uygulaması**, ardından **Tamam**.

    ![VUE.js şablonu](../javascript/media/vuejs-template.png)
    ::: moniker-end
    Görmüyorsanız **temel Vue.js Web uygulaması** proje şablonu, eklemelisiniz **Node.js geliştirme** iş yükü. Ayrıntılı yönergeler için bkz. [önkoşulları](#prerequisites).

    Visual Studio yeni proje oluşturur. Yeni projeyi, Çözüm Gezgini'nde (sağ bölme) açar.

1. Uygulama için gerekli npm paketlerini yükleme ilerleme durumu için çıkış penceresine (alt bölme) denetleyin.

1. Çözüm Gezgini'nde açın **npm** düğümü ve tüm listelenen npm paketleri yüklü olduğundan emin olun.

    Tüm paketler (ünlem simgesi) eksikse, sağ tıklayabilirsiniz **npm** düğümünü seçip **eksik npm paketlerini yükle**.

## <a name="explore-the-ide"></a>IDE'yi keşfedin

1. Bir göz atın **Çözüm Gezgini** sağ bölmede.

     ![VUE.js çözümü](../javascript/media/vuejs-solution.png)

   - Kalın yazı tipinde vurgulanmış olduğu içinde verdiğiniz ad kullanarak projenize **yeni proje** iletişim kutusu. Disk üzerinde bu proje tarafından temsil edilen bir. *njsproj* proje klasörünüzdeki dosya.

   - En üst düzeyinde ve proje ile aynı ada sahip varsayılan bir çözümdür. Bir çözüm tarafından temsil edilen bir. *sln* dosya diskte, bir veya daha fazla ilgili proje için bir kapsayıcıdır.

   - **Npm** düğüm tüm yüklü npm paketlerini gösterir. İçin arama yapın ve iletişim kutusunu kullanarak npm paketlerini yüklemek için npm düğümünü sağ tıklayabilirsiniz.

2. Npm paketlerini yükle veya bir komut istemi'nden Node.js komutları çalıştırmak, proje düğümüne sağ tıklayın ve seçin, isterseniz **burada açık komut istemi**.

## <a name="add-a-vue-file-to-the-project"></a>.Vue dosya projeye ekleyin.

1. Çözüm Gezgini'nde gibi herhangi bir klasörü sağ tıklatın *src/components* klasöründe ve ardından **Ekle** > **yeni öğe**.

1. Şunlardan birini seçin **JavaScript Vue tek dosya bileşen** veya **TypeScript Vue tek dosya bileşen**ve ardından **Ekle**.

    Visual Studio yeni dosyayı projeye ekler.

## <a name="build-the-project"></a>Proje derleme

1. (Yalnızca TypeScript Proje) Visual Studio'dan seçin **derleme** > **çözümü Temizle**.

1. Ardından, **derleme** > **Çözümü Derle** Projeyi derlemek için. Denetleme **çıkış** penceresini derleme sonuçları ve seçin **derleme** gelen **çıktıyı Göster** listesi.

    Vue.js proje şablonu kullanan `build` olay npm betiği yapılandırarak bir gönderi oluşturun. Bu ayarı değiştirmek istiyorsanız, proje dosyasını açın (*\<projectname\>.njsproj*) Windows Gezgini'nden ve bu kod satırı bulun:

    ```xml
    <PostBuildEvent>npm run build</PostBuildEvent>
    ```

## <a name="run-the-application"></a>Uygulamayı çalıştırın

1. Tuşuna **Ctrl**+**F5** (veya **hata ayıklama > hata ayıklama olmadan Başlat**) uygulamayı çalıştırın.

   Bir ileti görürsünüz konsolda *geliştirme sunucusu başlatma*.

   Ardından, uygulamayı bir tarayıcıda açılır.

   ![Tarayıcıda çalışan Vue.js uygulama](../javascript/media/vuejs-running-app.png)

1. Web tarayıcısını kapatın.

Bu hızlı başlangıcı tamamladığınızda Tebrikler! Visual Studio IDE ile Vue.js kullanma hakkında biraz öğrenilen umuyoruz. Bir öğreticide özelliklerini daha ayrıntılı olarak inceleyin istiyorsanız, devam **öğreticiler** İçindekiler bölümünde.

## <a name="next-steps"></a>Sonraki adımlar

- Git aracılığıyla [Node.js ve Express Öğreticisi](../nodejs/tutorial-nodejs.md)
- Git aracılığıyla [Node.js ve React öğretici](/visualstudio/javascript/tutorial-nodejs-with-react-and-jsx)
- [Uygulamayı Linux App Service'e dağıtma](../javascript/publish-nodejs-app-azure.md)