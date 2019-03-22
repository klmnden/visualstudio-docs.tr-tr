---
title: Windows üzerinde Docker için Visual Studio Araçları
description: Visual Studio'da Docker araçları ile tanışın
author: ghogen
ms.author: ghogen
ms.date: 03/20/2019
ms.technology: vs-azure
ms.openlocfilehash: 68364384a233defeb69203ed4f3ddc8f122e8bb7
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58356297"
---
# <a name="docker-in-visual-studio-on-windows"></a>Windows üzerinde Visual Studio'da docker

::: moniker range="vs-2017"
Kapsayıcılar ile geliştirmek için Visual Studio'ya dahil olan araçları kullanımı kolaydır ve derleme büyük ölçüde basitleştirme çalıştırın ve Görevler oluşturun. Ayrıca çalıştırmak ve kapsayıcılarınızı normal kullanarak hata ayıklama **F5** ve **Ctrl**+**F5** Visual Studio'dan anahtarları. Kapsayıcılarında aynı tanımlanmışsa, tüm çözüm bile ayıklayabilirsiniz *docker-compose.yml* çözüm düzeyinde dosya.
::: moniker-end
::: moniker range=">=vs-2019"
Kapsayıcılar ile geliştirmek için Visual Studio 2019 içinde dahil edilen araçlara kullanımı kolaydır ve derleme büyük ölçüde basitleştirme çalıştırın ve Görevler oluşturun. Ayrıca çalıştırmak ve kapsayıcılarınızı normal kullanarak hata ayıklama **F5** ve **Ctrl**+**F5** Visual Studio'dan anahtarları. Kapsayıcılarında aynı tanımlanmışsa, tüm çözüm bile ayıklayabilirsiniz *docker-compose.yml* çözüm düzeyinde dosya.
::: moniker-end

> [!NOTE]
> Bu makale Windows üzerinde Visual Studio ve Visual Studio değil, Mac için geçerlidir

> [!TIP]
> Docker için Windows yükleme hakkında daha fazla bilgi edinmek için [için Docker Masaüstü Windows](https://docs.docker.com/docker-for-windows/).

## <a name="docker-support-in-visual-studio"></a>Visual Studio'da docker desteği

::: moniker range="vs-2017"
Bir projeye ekleyebilirsiniz Docker desteği iki düzeyi vardır. ASP.NET Core projelerinde, yalnızca ekleyebilirsiniz bir *Dockerfile* Docker desteği etkinleştirerek projeye dosya. İleri düzey ekler kapsayıcı düzenleme desteği olan bir *Dockerfile* (zaten yoksa) projeye ve *docker-compose.yml* çözüm düzeyinde dosya. Docker Compose, aracılığıyla kapsayıcı düzenleme desteği, varsayılan olarak Visual Studio 2017 sürüm 15.0 için 15.7 eklenir. Kapsayıcı düzenleme 15,8 ya da üzeri bir Tercihli özellik Visual Studio 2017 sürümleri desteğidir. Docker Compose ve Service Fabric 15,8 ve sonraki sürümleri destekler.
::: moniker-end
::: moniker range=">=vs-2019"
Bir projeye ekleyebilirsiniz Docker desteği iki düzeyi vardır. ASP.NET Core projelerinde, yalnızca ekleyebilirsiniz bir *Dockerfile* Docker desteği etkinleştirerek projeye dosya. İleri düzey ekler kapsayıcı düzenleme desteği olan bir *Dockerfile* (zaten yoksa) projeye ve *docker-compose.yml* çözüm düzeyinde dosya.  Kapsayıcı düzenleme desteği, Docker Compose, Kubernetes ve Service Fabric destekleyen Visual Studio 2019, isteğe bağlı bir özelliktir.
::: moniker-end

**Ekle > Docker desteği** ve **Ekle > kapsayıcı Düzenleyicisi desteği** komutları bulunan bir ASP.NET Core projesi için proje düğümünü sağ tıklama menüsünü (veya bağlam menüsü)  **Çözüm Gezgini**aşağıdaki ekran görüntüsünde gösterildiği gibi:

![Visual Studio'da Docker desteği menü seçeneği ekleyin](./media/visual-studio-tools-for-docker/add-docker-support-menu.png)

### <a name="add-docker-support"></a>Docker desteği Ekle

Docker desteği seçerek mevcut bir ASP.NET Core projesine ekleyebilirsiniz **Ekle** > **Docker desteği** içinde **Çözüm Gezgini**. Seçerek proje oluşturma sırasında Docker desteğini etkinleştirebilirsiniz **Docker desteği etkinleştirme** içinde **yeni ASP.NET Core Web uygulaması** tıkladığınızda açılan iletişim kutusunda **Tamam** içinde **yeni proje** iletişim kutusunda, aşağıdaki ekran görüntüsünde gösterildiği gibi.

::: moniker range="vs-2017"
![Visual Studio'da yeni bir ASP.NET Core web uygulaması için Docker desteğini etkinleştir](./media/visual-studio-tools-for-docker/enable-docker-support-visual-studio.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Visual Studio'da yeni bir ASP.NET Core web uygulaması için Docker desteğini etkinleştir](./media/visual-studio-tools-for-docker/vs-2019/enable-docker-support-visual-studio.png)
::: moniker-end

Visual Studio ekleyin ya da Docker desteğini etkinleştirmek ekler bir *Dockerfile* projeye dosya.

::: moniker range="vs-2017"
> [!NOTE]
> Docker Compose desteği için bir ASP.NET projesi (.NET Framework, .NET Core projesi) proje oluşturma sırasında aşağıdaki ekran görüntüsünde gösterildiği gibi etkinleştirmeniz, kapsayıcı düzenleme desteği de eklenir.

![Docker'ı etkinleştirme desteği için bir ASP.NET projesi oluşturma](media/visual-studio-tools-for-docker/enable-docker-compose-support.png)
::: moniker-end

### <a name="add-container-orchestration-support"></a>Kapsayıcı düzenleme desteği ekleme

Çok kapsayıcılı bir çözüm oluşturmak istediğinizde, kapsayıcı düzenleme desteği, projenize ekleyin. Bu, çalıştırma ve aynı tanımlanan bir grup kapsayıcının (tam çözüm) aynı anda hata ayıklaması sağlar *docker-compose.yml* dosya.

Kapsayıcı düzenleme desteği eklemek için çözümü veya proje düğümünü sağ **Çözüm Gezgini**ve **Ekle > kapsayıcı düzenleme desteği**. Ardından **Docker Compose**, **Kubernetes/Helm**, veya **Service Fabric** kapsayıcıları yönetmek için.

Kapsayıcı düzenleme desteği projenize ekledikten sonra gördüğünüz bir *Dockerfile* projeye eklenir ve **docker-compose** çözümüne eklenmiş klasör **ÇözümGezgini**, burada gösterildiği gibi:

![Visual Studio'daki Çözüm Gezgini'nde docker dosyaları](media/visual-studio-tools-for-docker/docker-support-solution-explorer.png)

Varsa *docker-compose.yml* zaten var, Visual Studio yalnızca ekler gerekli yapılandırma kod satırı için.

## <a name="configure-docker-tools"></a>Docker araçları yapılandırma

Ana menüden **Araçlar > Seçenekler**, genişletin **kapsayıcı araçları > ayarları**. Kapsayıcı Araçları ayarları görüntülenir.

![Visual Studio Docker seçenekleri gösteren araçları: Otomatik olarak proje yükünde gerekli Docker görüntülerini çekme, kapsayıcıları arka planda otomatik olarak Başlat, Kapat çözümdeki kapsayıcıları otomatik olarak sonlandırmak ve SSL sertifikasına güvenme istemi yapma.](./media/visual-studio-tools-for-docker/visual-studio-docker-tools-options.png)

Aşağıdaki tabloda, bu seçenekleri ayarlamak nasıl karar vermenize yardımcı olabilir.

| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Otomatik olarak proje yükünde gerekli Docker görüntülerini çekme | Açık | Docker Compose | Proje yüklenirken performansı artırmak için Visual Studio Docker çekme işlemi arka planda böylece kodunuzu çalıştırmak hazır olduğunuzda, görüntü zaten yüklenene veya yükleme sürecinde başlar. Yalnızca projeler yükleniyor ve kod gözatma ise, ihtiyacınız olmayan kapsayıcı görüntülerini yüklenmesini önlemek için kapatabilirsiniz. |
| Kapsayıcıları arka planda otomatik olarak Başlat | Açık | Docker Compose | Yeniden performansı artırmak için Visual Studio kapsayıcı ile birim başlatmalar, derleme ve kapsayıcı çalıştırma için hazır oluşturur. Kapsayıcı oluşturulduğunda denetlemek istiyorsanız, kapatır. |
| KILL çözümdeki kapsayıcıları otomatik olarak Kapat | Açık | Docker Compose | Kapsayıcıları çözümünüzün çözümün kapatılması veya Visual Studio kapatıldıktan sonra çalışmaya devam etmesini istiyorsanız kapatır. |
| İçin localhost SSL sertifikasına güvenme istemi yapma | Kapalı | ASP.NET Core 2.1 projeleri | Localhost SSL sertifikasına güvenilir değilse, bu onay kutusu işaretli değilse, projenizi her çalıştırdığınızda Visual Studio ister. |

> [!WARNING]
> Ardından localhost SSL sertifikasına güvenilmiyor ve isteyen bastırmak için kutuyu işaretleyin, HTTPS isteklerine uygulamanızı veya hizmetinizi çalışma zamanında başarısız olabilir. Bu durumda, onay kutusunu temizleyin **sorma** onay kutusunu projenizi çalıştırmak ve güven isteminde gösterir.

## <a name="next-steps"></a>Sonraki adımlar

Hizmetler hakkında daha ayrıntılı bilgi için uygulama ve kapsayıcılar ile çalışmak için Visual Studio Araçları'nın kullanımı okuma aşağıdaki makaleleri:

[Yerel bir Docker kapsayıcısı uygulamalarında hata ayıklama](vs-azure-tools-docker-edit-and-refresh.md)

[ASP.NET kapsayıcısını bir kapsayıcı kayıt defterine Visual Studio kullanarak dağıtma](vs-azure-tools-docker-hosting-web-apps-in-docker.md)
