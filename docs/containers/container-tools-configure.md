---
title: Visual Studio kapsayıcı araçlarını yapılandırma
description: Visual Studio 'da bulunan araçları Docker kapsayıcılarıyla çalışmak üzere yapılandırın.
author: ghogen
ms.author: ghogen
ms.topic: conceptual
ms.date: 03/20/2019
ms.technology: vs-azure
ms.openlocfilehash: f05eb5d92c0cdaa1242f0d98c3d877eebae27bb1
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253191"
---
# <a name="how-to-configure-visual-studio-container-tools"></a>Visual Studio kapsayıcı araçlarını yapılandırma

Visual Studio ayarlarını kullanarak, Docker kapsayıcılarıyla çalışırken performansı ve kaynak kullanımını etkileyen ayarlar dahil olmak üzere Visual Studio 'nun Docker kapsayıcılarıyla nasıl çalıştığı hakkında bazı yönleri denetleyebilirsiniz.

## <a name="container-tools-settings"></a>Kapsayıcı araçları ayarları

Ana menüden **araçlar > seçenekler**' i seçin ve **kapsayıcı araçları > Ayarlar**' ı genişletin. Kapsayıcı araçları ayarları görüntülenir.

::: moniker range="vs-2017"

![Visual Studio kapsayıcı araçları seçenekleri, şunu gösterir: Gerekli Docker görüntülerini proje yüküne otomatik olarak çekme, kapsayıcıları arka planda otomatik olarak Başlat, çözüm kapatıldığında kapsayıcıları otomatik olarak sonlandır ve SSL sertifikası için sorma.](./media/overview/visual-studio-docker-tools-options.png)
::: moniker-end

::: moniker range=">=vs-2019"

Kapsayıcı araçları **genel** ayarları:

![Visual Studio kapsayıcı araçları seçenekleri, şunu gösterir: Gerekirse Docker Desktop ' ı yükleyip SSL sertifikasına güven ASP.NET Core.](./media/configure-container-tools/tools-options-1.png)

Kapsayıcı araçları **tek proje** ve **Docker Compose** ayarları:

![Visual Studio kapsayıcı araçları seçenekleri, şunu gösterir: Proje kapasitesinde kapsayıcıları sonlandırın, proje açık ' de gerekli Docker görüntülerini çekin ve proje açıkken kapsayıcıları çalıştırın.](./media/configure-container-tools/tools-options-2.png)
::: moniker-end

Aşağıdaki tablo, bu seçeneklerin nasıl ayarlanacağına karar vermenize yardımcı olur.

::: moniker range="vs-2017"
| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Gerekli Docker görüntülerini proje yüküne otomatik olarak çekme | Açık | Docker Compose | Projeleri yüklerken daha yüksek performans için, Visual Studio arka planda bir Docker çekme işlemi başlatır, böylece kodunuzu çalıştırmaya hazırsanız görüntü zaten indirilmeye devam eder ve indirme sürecinde olur. Yalnızca projeler ve tarama kodu yüklüyorsanız, gerek duymadığınız kapsayıcı görüntülerini indirmeyi önlemek için bunu kapatabilirsiniz. |
| Kapsayıcıları arka planda otomatik olarak Başlat | Açık | Docker Compose | Daha yüksek performans için, Visual Studio, kapsayıcınızı oluşturup çalıştırdığınızda, toplu takmaya hazırlama ile bir kapsayıcı oluşturur. Kapsayıcının ne zaman oluşturulduğunu denetlemek isterseniz, bunu kapatın. |
| Çözüm kapatıldığında kapsayıcıları otomatik olarak Sonlandır | Açık | Docker Compose | Çözümünüzü kapattıktan veya Visual Studio 'Yu kapattıktan sonra çözümünüz için kapsayıcıların çalışmaya devam etmesini istiyorsanız bunu kapatın. |
| Localhost SSL sertifikası için güvenme isteme | Kapalı | ASP.NET Core 2,1 projeleri | Localhost SSL sertifikası güvenilir değilse, bu onay kutusu işaretlenmediği takdirde, Visual Studio projenizi her çalıştırdığınızda sorar. |
::: moniker-end

::: moniker range=">=vs-2019"

Aşağıdaki tabloda **genel** ayarları açıklanmaktadır:

| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Gerekirse Docker Desktop 'ı yükler | Bana sor | Tek proje, Docker Compose | Docker Desktop yüklü değilse isteyip istemediğinizi seçin. |
| SSL sertifikası ASP.NET Core güven | Bana sor | ASP.NET Core 2. x projeleri | **Bana sor**olarak ayarlandığında, localhost SSL sertifikası güvenilir değilse, projenizi her çalıştırdığınızda Visual Studio sorar. |

Aşağıdaki tabloda **tek proje** ve **Docker Compose** ayarları açıklanmaktadır:

| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Proje açıkken gerekli Docker görüntülerini çekme | Doğru | Tek proje, Docker Compose | Projeleri yüklerken daha yüksek performans için, Visual Studio arka planda bir Docker çekme işlemi başlatır, böylece kodunuzu çalıştırmaya hazırsanız görüntü zaten indirilmeye devam eder ve indirme sürecinde olur. Yalnızca projeler ve tarama kodu yüklüyorsanız, gerek duymadığınız kapsayıcı görüntülerini indirmemek için **false** olarak ayarlayabilirsiniz. |
| Açık proje üzerinde kapsayıcıları Çalıştır | Doğru | Tek proje, Docker Compose | Daha yüksek performans için, Visual Studio, kapsayıcınızı oluşturup çalıştırdığınızda, daha önce bir kapsayıcı oluşturur. Kapsayıcının ne zaman oluşturulduğunu denetlemek istiyorsanız, **false**olarak ayarlayın. |
| Proje kapatıldığında kapsayıcıları durdur | Doğru | Tek proje ve Docker Compose | Çözümünüzü kapattıktan veya Visual Studio 'Yu kapattıktan sonra çözümünüz için kapsayıcıların çalışmaya devam etmesini istiyorsanız, **false** olarak ayarlayın. |

::: moniker-end
> [!WARNING]
> Localhost SSL sertifikası güvenilir değilse ve sorulmayı önlemek için kutuyu denetederseniz, HTTPS Web istekleri, uygulamanızda veya hizmetinizde çalışma zamanında başarısız olabilir. Bu **durumda, sorma onay kutusunun** işaretini kaldırın, projenizi çalıştırın ve sorulduğunda güveni belirtin.

## <a name="next-steps"></a>Sonraki adımlar

Bu [genel bakışta](visual-studio-tools-for-docker.md)Visual Studio 'da kapsayıcılarla çalışma hakkında daha fazla bilgi edinin.