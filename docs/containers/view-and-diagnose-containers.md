---
title: Kapsayıcı günlükleri, ortam değişkenleri, & dosya sistemi erişimi
description: Uygulamanızı barındıran kapsayıcılar içinde neler olduğunu görmek için bir araç penceresi kullanarak Visual Studio 'da kapsayıcı tabanlı uygulamalarınızı hata ayıklama ve tanılama olanağından nasıl iyileştirebileceğinizi açıklar.
author: ghogen
ms.author: ghogen
ms.topic: conceptual
ms.date: 05/06/2019
ms.technology: vs-azure
monikerRange: vs-2019
ms.openlocfilehash: 3fb9a52f990a2e492c63a6e71a7cc2063110c816
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70179836"
---
# <a name="how-to-view-and-diagnose-containers-in-visual-studio"></a>Visual Studio 'da kapsayıcıları görüntüleme ve tanılama

**Kapsayıcılar** penceresini kullanarak uygulamanızı barındıran kapsayıcılar içinde neler olduğunu görüntüleyebilirsiniz. Kapsayıcılarınız ile neler olduğunu görüntülemek ve tanılamak için Docker komutlarını çalıştırmak üzere komut istemi 'ni kullanmak üzere kullandıysanız, bu pencere, Visual Studio IDE 'den çıkmadan Kapsayıcılarınızı izlemeye yönelik daha uygun bir yol sağlar.

> [!NOTE]
> Kapsayıcılar penceresi şu anda Visual Studio 2019 için indirebileceğiniz bir önizleme uzantısı [](https://aka.ms/vscontainerspreview) olarak sunulmaktadır.

## <a name="prerequisites"></a>Önkoşullar

- [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
- [Visual Studio 2019](https://visualstudio.microsoft.com/downloads) 'yi yükler
- [Kapsayıcılar pencere uzantısını](https://aka.ms/vscontainerspreview) yükler

## <a name="view-information-about-your-containers"></a>Kapsayıcılarınız hakkındaki bilgileri görüntüleyin

Kapsayıcılı bir .NET projesi başlattığınızda **kapsayıcılar** penceresi otomatik olarak açılır. İstediğiniz zaman, Visual Studio 'da kapsayılarınızı görüntülemek için, **CTRL**+**Q** ' ı kullanarak Visual Studio arama kutusunu etkinleştirin ve ilk öğeyi `Containers` yazın ve seçin. Ayrıca, ana menüden **kapsayıcılar** penceresini açabilirsiniz.  > **Diğer**Windowskapsayıcılarını > görüntülemek için menü yolunu kullanın.  

![Kapsayıcılar penceresindeki ortam sekmesinin ekran görüntüsü](media/view-and-diagnose-containers/container-window.png)

Sol tarafta, yerel makinenizde kapsayıcı listesini görürsünüz. Çözümünüz ile ilişkili kapsayıcılar **çözüm kapsayıcıları**altında gösterilir. Sağ tarafta, **ortam**, **bağlantı noktaları**, **Günlükler**ve **dosyalar**için sekmeler içeren bir bölme görürsünüz.

> [!TIP]
> **Kapsayıcılar** araç penceresinin Visual Studio 'ya yerleştirilmiş olduğu yeri kolayca özelleştirebilirsiniz. Bkz. [Visual Studio 'da pencere düzenlerini özelleştirme](/visualstudio/ide/customizing-window-layouts-in-visual-studio). Varsayılan olarak, **kapsayıcı** penceresi, hata ayıklayıcı çalışırken **izleme** penceresiyle birlikte yerleştirilir.

## <a name="view-environment-variables"></a>Ortam değişkenlerini görüntüle

**Ortam** sekmesi, kapsayıcıdaki ortam değişkenlerini gösterir. Uygulamanızın kapsayıcısı için, bu değişkenleri birçok şekilde ayarlayabilirsiniz. Örneğin, Dockerfile, bir. env dosyası veya bir Docker komutu kullanarak bir kapsayıcı başlattığınızda-e seçeneğini kullanabilirsiniz.

![Kapsayıcılar penceresindeki ortam sekmesinin ekran görüntüsü](media/view-and-diagnose-containers/container-environment-vars.png)

> [!NOTE]
> Ortam değişkenlerinde yapılan değişiklikler gerçek zamanlı olarak yansıtılmaz. Ayrıca, bu sekmedeki ortam değişkenleri, kapsayıcıdaki sistem ortam değişkenleridir ve yerel olarak, uygulamanın kullanıcı ortam değişkenlerini yansıtmaz.

## <a name="view-port-mappings"></a>Bağlantı noktası eşlemelerini görüntüle

**Bağlantı noktaları** sekmesinde, Kapsayıcınız için geçerli olan bağlantı noktası eşlemelerini kontrol edebilirsiniz.

![Kapsayıcılar penceresindeki bağlantı noktaları sekmesinin ekran görüntüsü](media/view-and-diagnose-containers/container-ports.png)

İyi bilinen bağlantı noktaları bağlanır, bu nedenle bir bağlantı noktasında kullanılabilir içerik varsa, tarayıcıyı açmak için bağlantıya tıklayabilirsiniz.

## <a name="view-logs"></a>Günlükleri görüntüleme

**Günlükler** sekmesi, `docker logs` komutun sonuçlarını gösterir. Varsayılan olarak, sekmesi bir kapsayıcıda stdout ve stderr akışlarını gösterir, ancak çıktıyı yapılandırabilirsiniz. Ayrıntılar için bkz. [Docker günlüğü](https://docs.docker.com/config/containers/logging/).  Varsayılan olarak, **Günlükler** sekmesi günlükleri akışlar, ancak sekmedeki **Durdur** düğmesini seçerek bunu devre dışı bırakabilirsiniz.

![Kapsayıcılar penceresindeki Günlükler sekmesinin ekran görüntüsü](media/view-and-diagnose-containers/containers-logs.jpg)

Günlükleri temizlemek için **Günlükler** sekmesindeki **Temizle** düğmesini kullanın.  Tüm günlükleri almak için **Yenile** düğmesini kullanın.

> [!NOTE]
> Visual Studio, STDOUT ve stderr 'i **Çıkış** penceresine otomatik olarak yönlendirir. bu nedenle, kapsayıcılar Visual Studio 'dan (yani, **çözüm kapsayıcıları** bölümünde yer alan kapsayıcılar) Günlükler Bu sekmede görüntülenmez; Bunun yerine **Çıkış** penceresini kullanın.

## <a name="view-the-filesystem"></a>Dosya sistemini görüntüleme

**Dosyalar** sekmesinde, projenizin bulunduğu uygulama klasörü de dahil olmak üzere kapsayıcının dosya sistemini görüntüleyebilirsiniz.

![Kapsayıcılar penceresindeki dosyalar sekmesinin ekran görüntüsü](media/view-and-diagnose-containers/container-filesystem.png)

Visual Studio 'da dosyaları açmak için dosyaya gidin ve çift tıklayın ya da sağ tıklayıp **Aç**' ı seçin. Visual Studio dosyaları salt okuma modunda açar.

![Visual Studio 'da görüntülenmek üzere açık dosyanın ekran görüntüsü](media/view-and-diagnose-containers/container-file-open.png)

**Dosyalar** sekmesini kullanarak, IIS günlükleri, yapılandırma dosyaları ve kapsayıcının dosya sisteminde bulunan diğer içerik dosyaları gibi uygulama günlüklerini görüntüleyebilirsiniz.

## <a name="start-stop-and-remove-containers"></a>Kapsayıcıları başlatma, durdurma ve kaldırma

**Kapsayıcılar** penceresinde, varsayılan olarak Docker 'ın yönettiği makinedeki tüm kapsayıcılar gösterilir. Artık istemediğiniz bir kapsayıcıyı başlatmak, durdurmak veya kaldırmak (silmek) için araç çubuğu düğmelerini kullanabilirsiniz.  Kapsayıcılar oluşturulduğu veya kaldırıldığı için bu liste dinamik olarak güncelleştirilir.

## <a name="next-steps"></a>Sonraki adımlar

[Kapsayıcı araçlarına genel bakış ' ı](overview.md)okuyarak Visual Studio 'Da bulunan kapsayıcı araçları hakkında daha fazla bilgi edinin.

## <a name="see-also"></a>Ayrıca bkz.

[Visual Studio 'da kapsayıcı geliştirme](/visualstudio/containers)

[Visual Studio için Uzantılar marketi](https://marketplace.visualstudio.com/)
