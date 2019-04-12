---
title: Windows üzerinde Visual Studio kapsayıcı araçları
description: Docker ile çalışmak için Visual Studio'da kullanılabilen araçlar tanıyalım
author: ghogen
ms.author: ghogen
ms.topic: overview
ms.date: 03/20/2019
ms.technology: vs-azure
ms.openlocfilehash: 4b03ccddadf954b8430b7ad9b5a4ed765fccc3f5
ms.sourcegitcommit: cd91a8a4f6086cda9ba6948be25864fc7d6b8e44
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "59537972"
---
# <a name="container-tools-in-visual-studio"></a>Visual Studio kapsayıcı araçları

Kapsayıcılar ile geliştirmek için Visual Studio'ya dahil olan araçları kullanımı kolaydır ve yapı, hata ayıklama ve dağıtım kapsayıcılı uygulamalar için büyük ölçüde basitleştirir. Tek bir proje için bir kapsayıcı çalışmak veya birden çok hizmetlerle kapsayıcılardaki ile çalışmak için Docker Compose, Service Fabric veya Kubernetes kapsayıcı düzenleme kullanın.

> [!NOTE]
> Bu makale Windows üzerinde Visual Studio ve Visual Studio değil, Mac için geçerlidir

> [!TIP]
> Docker için Windows yükleme hakkında daha fazla bilgi edinmek için [için Docker Masaüstü Windows](https://docs.docker.com/docker-for-windows/).

## <a name="docker-support-in-visual-studio"></a>Visual Studio'da docker desteği

Docker desteği, bazı .NET proje türleri için kullanılabilir.  ASP.NET projeleri, ASP.NET Core projeleri ve .NET Core ve .NET Framework konsol projeleri için kullanılabilir.

Visual Studio'da Docker desteği, bir müşteri gereksinimlerine yanıt sayısı üzerinden değişti. Bir projeye ekleyebilirsiniz Docker desteği iki düzeyi vardır ve proje türü ve Visual Studio sürümü tarafından desteklenen seçenekler farklılık gösterir. Yalnızca bir kapsayıcı için tek bir proje, düzenleme, kullanmadan istiyorsanız bazı desteklenen proje türleri ile bunu Docker desteği ekleyerek yapabilirsiniz.  Seçtiğiniz belirli bir orchestrator için uygun destek dosyaları ekler kapsayıcı düzenleme desteği sonraki düzeyidir.  

::: moniker range="vs-2017"

Visual Studio 2017 ile Docker Compose ve Service Fabric kapsayıcı düzenleme Hizmetleri kullanabilirsiniz.  Yüklerseniz de Kubernetes kullanabilirsiniz [Kubernetes için Visual Studio Araçları](https://aka.ms/get-vsk8stools).

> [!NOTE]
> Bir Visual Studio 2017 sürümünü 15,8 önce kullandığınız ya da .NET Framework proje şablonu (değil .NET Core), kullanmakta olduğunuz düzenleme desteği, Docker Compose kullanarak Docker desteği eklediğinizde otomatik olarak eklenir. Docker Compose, aracılığıyla kapsayıcı düzenleme desteği, Visual Studio 2017 sürüm 15.0 için 15.7 ve .NET Framework projeleri için otomatik olarak eklenir.

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio 2019 ile Docker Compose, Kubernetes ve Service Fabric kapsayıcı düzenleme Hizmetleri kullanabilirsiniz.

> [!NOTE]
> Docker Compose kullanarak düzenleme desteği, Docker desteği eklediğinizde, tam .NET Framework konsol projesi şablonunu kullanıyorsanız, otomatik olarak eklenir.
::: moniker-end

**Ekle > Docker desteği** ve **Ekle > kapsayıcı Düzenleyicisi desteği** komutları bulunan bir ASP.NET Core projesi için proje düğümünü sağ tıklama menüsünü (veya bağlam menüsü)  **Çözüm Gezgini**aşağıdaki ekran görüntüsünde gösterildiği gibi:

![Visual Studio'da Docker desteği menü seçeneği ekleyin](./media/overview/add-docker-support-menu.png)

### <a name="adding-docker-support-without-orchestration"></a>(Düzenleme) olmadan Docker desteği ekleme

Docker desteği seçerek mevcut bir projeye ekleyebilirsiniz **Ekle** > **Docker desteği** içinde **Çözüm Gezgini**. Seçerek proje oluşturma sırasında Docker desteğini etkinleştirebilirsiniz **Docker desteği etkinleştirme** aşağıdaki ekran görüntüsünde gösterildiği gibi yeni bir proje oluşturma sırasında:

::: moniker range="vs-2017"
![Visual Studio'da yeni bir ASP.NET Core web uygulaması için Docker desteğini etkinleştir](./media/overview/enable-docker-support-visual-studio.png)
::: moniker-end
::: moniker range=">=vs-2019"
![Visual Studio'da yeni bir ASP.NET Core web uygulaması için Docker desteğini etkinleştir](./media/overview/vs-2019/enable-docker-support-visual-studio.png)
::: moniker-end

Ekleyin veya Docker desteğini etkinleştirmek, Visual Studio aşağıdaki projeye ekler:

- bir *Dockerfile* dosyası
- .dockerignore dosyası
- Microsoft.VisualStudio.Azure.Containers.Tools.Targets NuGet paket başvurusu

::: moniker range=">=vs-2019"
Docker desteği eklediğinizde, çözüm şöyle görünür:

![Dockerfile ve .dockerignore dosyası ile çözüm Gezgini'nin ekran görüntüsü](media/overview/vs-2019/dockerfile-dockerignore.png)
::: moniker-end

::: moniker range="vs-2017"
> [!NOTE]
> Bilgisayarınızda Docker desteği için bir ASP.NET projesi (.NET Framework, .NET Core projesi) proje oluşturma sırasında aşağıdaki ekran görüntüsünde gösterildiği gibi etkinleştirdiğinizde, kapsayıcı düzenleme desteği de eklenir.

![Docker'ı etkinleştirme desteği için bir ASP.NET projesi oluşturma](media/overview/enable-docker-compose-support.png)
::: moniker-end

## <a name="docker-compose-support"></a>Docker Compose desteği

Docker Compose kullanarak bir çok kapsayıcılı çözüm oluşturmak istediğinizde, kapsayıcı düzenleme desteği, projenize ekleyin. Bu, çalıştırma ve aynı tanımlanan bir grup kapsayıcının (tam çözüm veya proje grubu) aynı anda hata ayıklaması sağlar *docker-compose.yml* dosya.

Docker Compose kullanarak kapsayıcı düzenleme desteği eklemek için çözümü veya proje düğümünü sağ **Çözüm Gezgini**ve **Ekle > kapsayıcı düzenleme desteği**. Ardından **Docker Compose** kapsayıcıları yönetmek için.

Kapsayıcı düzenleme desteği projenize ekledikten sonra gördüğünüz bir *Dockerfile* (olmadıysa bir var. zaten) projeye eklenir ve **docker-compose** çözümüneeklenmişklasörü **Çözüm Gezgini**, burada gösterildiği gibi:

![Visual Studio'daki Çözüm Gezgini'nde docker dosyaları](media/overview/docker-support-solution-explorer.png)

Varsa *docker-compose.yml* zaten var, Visual Studio yalnızca ekler gerekli yapılandırma kod satırı için.

Docker Compose kullanarak denetlemek için istediğiniz başka projelerle işlemi tekrarlayın.

## <a name="kubernetes-support"></a>Kubernetes desteği

::: moniker range="vs-2017"
Kubernetes desteği eklemek için yükleme [Kubernetes için Visual Studio Araçları](https://aka.ms/get-vsk8stools).
::: moniker-end

Kubernetes desteği sayesinde, yerel projenizi ve çalışan bir Kubernetes kümesi arasında bir bağlantı etkinleştirebilirsiniz [Azure Kubernetes Service (AKS)](/azure/aks)ve böylece değiştirmek ve hata ayıklama hizmetlerinizi Visual Studio kullanarak AKS içinde çalışır.  Bu hizmet tarafından sağlanan [Azure geliştirme alanları](/azure/dev-spaces/quickstart-netcore-visualstudio). Azure geliştirme alanları ayrıca Kubernetes hizmetlerinizin adlı ayrı dalları ayarlamanızı sağlar *geliştirme alanları* geliştirme amacıyla, bu nedenle, verimli bir şekilde yalıtmak geliştirme sürümlerinde çalışan üretim hizmetlerinden ve tutun farklı değişiklikler düzgün bir şekilde birbirinden ayrılmış.

Kubernetes desteği, projenize eklemek için **Kubernetes/Helm** eklediğinizde kapsayıcı düzenleme desteği. Çeşitli dosyalar, projenize eklenir dahil olmak üzere *azds.yaml*, Azure geliştirme alanları yapılandırır ve Helm grafikleri, Kubernetes hizmetlerinizi yapısını açıklar.

## <a name="service-fabric-support"></a>Service Fabric desteği

Visual Studio'da Service Fabric araçları ile geliştirin ve çalıştırın, Azure Service Fabric ve yerel olarak hata ayıklama için hata ayıklama ve Azure'a dağıtın.

::: moniker range="vs-2017"
Visual Studio 2017 sürüm 15,9 ve daha sonra Azure geliştirme iş yükü yüklenmiş olan, Windows kapsayıcıları ve Service Fabric düzenleme kullanarak kapsayıcılı mikro hizmet geliştirmeyi destekler.
::: moniker-end
::: moniker range=">=vs-2019"
Visual Studio 2019 Windows kapsayıcıları ve Service Fabric düzenleme kullanarak geliştirme kapsayıcılı mikro hizmetler destekler.
::: moniker-end

Ayrıntılı bir öğretici için bkz [Öğreticisi: Azure Service Fabric'e Windows kapsayıcısındaki bir .NET uygulaması dağıtma](/azure/service-fabric/service-fabric-host-app-in-a-container).

Azure Service Fabric hakkında daha fazla bilgi için bkz. [Service Fabric](/azure/service-fabric).

## <a name="continuous-delivery-and-continuous-integration-cicd"></a>Sürekli teslim ve sürekli tümleştirme (CI/CD)

Visual Studio, otomatik ve sürekli tümleştirme ve hizmet kod ve yapılandırma değişiklikleri teslimi için Azure işlem hatları ile kolayca tümleşir. Başlamak için bkz: [ilk işlem hattınızı oluşturma](/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=tfs-2018-2).

Service Fabric için bkz: [Öğreticisi: Azure DevOps projeleri'ni kullanarak ASP.NET Core uygulamanızı Azure Service Fabric'e dağıtma](/azure/devops-project/azure-devops-project-service-fabric).

Kubernetes için bkz: [Azure Kubernetes Service için Docker kapsayıcı uygulamasını dağıtma](/azure/devops/pipelines/apps/cd/deploy-aks?view=azure-devops).

## <a name="next-steps"></a>Sonraki adımlar

Hizmetler hakkında daha ayrıntılı bilgi için uygulama ve kapsayıcılar ile çalışmak için Visual Studio Araçları'nın kullanımı okuma aşağıdaki makaleleri:

[Yerel bir Docker kapsayıcısı uygulamalarında hata ayıklama](vs-azure-tools-docker-edit-and-refresh.md)

[ASP.NET kapsayıcısını bir kapsayıcı kayıt defterine Visual Studio kullanarak dağıtma](vs-azure-tools-docker-hosting-web-apps-in-docker.md)
