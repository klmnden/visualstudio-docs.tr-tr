---
title: Kapsayıcı günlükleri, ortam değişkenleri ve dosya sistemi erişim
description: Uygulamanızı hata ayıklama ve kapsayıcılarda barındıran neler olup bittiğini görmek için bir araç penceresini kullanarak kapsayıcı tabanlı uygulamalarınızı Visual Studio'da tanılama yeteneğinizi geliştirmek nasıl açıklar.
author: ghogen
ms.author: ghogen
ms.topic: conceptual
ms.date: 05/06/2019
ms.technology: vs-azure
monikerRange: vs-2019
ms.openlocfilehash: b8e8e2db3f8f6e5aa60f3fa593caf017c349dca8
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66261196"
---
# <a name="how-to-view-and-diagnose-containers-in-visual-studio"></a>Görüntüleme ve kapsayıcıları Visual Studio'da tanılama

Kullanarak uygulamanızı barındırmak kapsayıcıların içinde neler olduğunu görüntüleyebilirsiniz **kapsayıcıları** penceresi. Bu pencere, görüntülemek ve kapsayıcılarınızı ile neler olduğunu tanılamak için Docker komutlarını çalıştırmak için komut istemi kullanarak alışıksanız Visual Studio IDE'den çıkmadan kapsayıcılarınızı izleyecek şekilde daha kullanışlı bir yol sağlar.

> [!NOTE]
> Zobrazit okno yapabileceğiniz bir önizleme uzantısı olarak şu anda kullanılabilir [indirme](https://aka.ms/vscontainerspreview) Visual Studio 2019 için.

## <a name="prerequisites"></a>Önkoşullar

- [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
- Yükleme [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)
- Yükleme [kapsayıcıları penceresini genişletme](https://aka.ms/vscontainerspreview)

## <a name="view-information-about-your-containers"></a>Kapsayıcılarınızı hakkındaki bilgileri görüntüleme

**Kapsayıcıları** kapsayıcılı bir .NET projesi başlattığınızda penceresi otomatik olarak açılır. Kapsayıcılarınızı Visual Studio ile dilediğiniz zaman görüntülemek için kullanın **Ctrl**+**Q** Visual Studio aramayı etkinleştirmek için kutusu ve türü `Containers` ve ilk öğeyi seçin. Ayrıca açabilirsiniz **kapsayıcıları** ana menüden penceresi. Menü yolunu kullanın **görünümü** > **diğer Windows** > **kapsayıcıları**.  

![Zobrazit okno sekmede ekran görüntüsü, ortam](media/view-and-diagnose-containers/container-window.png)

Sol tarafta, yerel makinenizde kapsayıcıları listesine bakın. Çözümünüzü ile ilişkili kapsayıcılar altında gösterilen **çözüm kapsayıcıları**. Sağa gördüğünüz için Sekmeler içeren bölme **ortam**, **bağlantı noktaları**, **günlükleri**, ve **dosyaları**.

> [!TIP]
> Where kolayca özelleştirebilirsiniz **kapsayıcıları** araç penceresi, Visual Studio'da yerleştirilmiştir. Bkz: [Visual Studio'da pencere düzenlerini özelleştirme](/visualstudio/ide/customizing-window-layouts-in-visual-studio). Varsayılan olarak, **kapsayıcıları** penceresi ile yerleştirilmiştir **Watch** hata ayıklayıcı çalıştırırken penceresi.

## <a name="view-environment-variables"></a>Ortam değişkenleri görüntüle

**Ortam** sekmesi, kapsayıcıda ortam değişkenlerini gösterir. Uygulamanızın kapsayıcı için bu değişkenler birçok yolla, örneğin, Dockerfile içinde bir .env dosyasında ya da Docker komutu kullanarak kapsayıcı başlattığınızda -e seçeneğini kullanarak ayarlayabilirsiniz.

![Zobrazit okno sekmede ekran görüntüsü, ortam](media/view-and-diagnose-containers/container-environment-vars.png)

> [!NOTE]
> Ortam değişkenlerini herhangi bir değişiklik, gerçek zamanlı olarak yansıtılmıyor. Ayrıca, ortam değişkenleri Bu sekme, ortam değişkenleri kapsayıcı üzerindeki sistem tarafından ve kullanıcı ortam değişkenlerini uygulamada yansıtmaz.

## <a name="view-port-mappings"></a>Bağlantı noktası eşlemelerini görüntüle

Üzerinde **bağlantı noktaları** sekmesi, kapsayıcınız için geçerli olan bağlantı noktası eşlemelerini denetleyebilirsiniz.

![Zobrazit okno sekmede ekran görüntüsü, bağlantı noktaları](media/view-and-diagnose-containers/container-ports.png)

İyi bilinen bağlantı noktalarına bağlı olan, bunu varsa kullanılabilir bir bağlantı noktasında tıklayabilirsiniz tarayıcıda açmak için bağlantıya içerik.

## <a name="view-logs"></a>Günlükleri görüntüleme

**Günlükleri** sekmesi sonuçlarını gösterir `docker logs` komutu. Varsayılan olarak, sekmesi, bir kapsayıcı stdout ve stderr akışları gösterir, ancak çıkış yapılandırabilirsiniz. Ayrıntılar için bkz [Docker günlüğünü](https://docs.docker.com/config/containers/logging/).  Varsayılan olarak, **günlükleri** sekmesini akışı günlükleri, ancak, bu seçerek devre dışı bırakabilirsiniz **Durdur** sekmesindeki düğmesi.

![Zobrazit okno ekran görüntüsü, günlükleri sekmesinde](media/view-and-diagnose-containers/containers-logs.jpg)

Günlükleri temizlemek için kullanın **Temizle** düğmesini **günlükleri** sekmesi.  Tüm kayıtları almak için kullanın **Yenile** düğmesi.

> [!NOTE]
> Visual Studio otomatik olarak yönlendiren stdout ve stderr **çıkış** kapsayıcı Visual Studio'dan başlatıldığında şekilde penceresi (diğer bir deyişle, kapsayıcılarda **çözüm kapsayıcıları** bölümü) görüntülenmez Bu sekmede günlüğe kaydeder; kullanma **çıkış** penceresi yerine.

## <a name="view-the-filesystem"></a>Dosya sistemi görüntüleyin

Üzerinde **dosyaları** sekmesinde, kapsayıcının dosya sistemi, projenizi içeren uygulama klasörü dahil olmak üzere görüntüleyebilirsiniz.

![Zobrazit okno sekmede dosyaların ekran görüntüsü](media/view-and-diagnose-containers/container-filesystem.png)

Dosyaları Visual Studio'da açmak için dosyasına gözatın ve çift tıklayın veya sağ tıklayıp seçin **açın**. Visual Studio dosyaları salt okunur modunda açar.

![Dosya açma Visual Studio'da görüntülemek için ekran görüntüsü](media/view-and-diagnose-containers/container-file-open.png)

Kullanarak **dosyaları** sekmesi, IIS günlükler, yapılandırma dosyalarını ve diğer içerik dosyaları gibi uygulama günlükleri, kapsayıcının dosya sistemine görüntüleyebilirsiniz.

## <a name="start-stop-and-remove-containers"></a>Başlatma, durdurma ve kapsayıcıları kaldırın

Varsayılan olarak, **kapsayıcıları** penceresi tüm kapsayıcıları Docker yönetir makine üzerinde gösterir. Araç çubuğu düğmeleri başlatmak, durdurmak veya artık istemediğiniz kaldırma (silme) bir kapsayıcı kullanabilirsiniz.  Bu liste, kapsayıcıları oluşturulan veya kaldırıldı olarak dinamik olarak güncelleştirilir.

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio kapsayıcı araçları hakkında daha fazla bilgi edinmek [kapsayıcı araçlarına genel bakış](overview.md).

## <a name="see-also"></a>Ayrıca bkz.

[Visual Studio'da kapsayıcı geliştirme](/visualstudio/containers)

[Visual Studio Market uzantıları](https://marketplace.visualstudio.com/)
