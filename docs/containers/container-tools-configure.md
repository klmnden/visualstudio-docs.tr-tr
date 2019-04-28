---
title: Visual Studio kapsayıcı araçları yapılandırma
description: Visual Studio'da kullanılabilen araçları, Docker kapsayıcıları ile çalışmak için yapılandırın.
author: ghogen
ms.author: ghogen
ms.topic: conceptual
ms.date: 03/20/2019
ms.technology: vs-azure
ms.openlocfilehash: 6fe51e0067ac15eb8e775786047009411c1e3181
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62825112"
---
# <a name="how-to-configure-visual-studio-container-tools"></a>Visual Studio kapsayıcı araçları yapılandırma

Visual Studio ayarları kullanarak Visual Studio ile Docker kapsayıcıları, Docker kapsayıcıları ile çalışırken, performans ve kaynak kullanımını etkileyen ayarları dahil olmak üzere nasıl çalışır bazı yönlerini denetleyebilirsiniz.

## <a name="container-tools-settings"></a>Kapsayıcı Araçları ayarları

Ana menüden **Araçlar > Seçenekler**, genişletin **kapsayıcı araçları > ayarları**. Kapsayıcı Araçları ayarları görüntülenir.

::: moniker range="vs-2017"

![Gösteren visual Studio kapsayıcı araçları seçenekleri: Otomatik olarak proje yükünde gerekli Docker görüntülerini çekme, kapsayıcıları arka planda otomatik olarak Başlat, Kapat çözümdeki kapsayıcıları otomatik olarak sonlandırmak ve SSL sertifikasına güvenme istemi yapma.](./media/overview/visual-studio-docker-tools-options.png)
::: moniker-end

::: moniker range=">=vs-2019"

Kapsayıcı Araçları **genel** ayarları:

![Gösteren visual Studio kapsayıcı araçları seçenekleri: Docker gerekirse Masaüstü ve ASP.NET Core SSL güven sertifikası yükleyin.](./media/configure-container-tools/tools-options-1.png)

Kapsayıcı Araçları **tek proje** ve **Docker Compose** ayarları:

![Gösteren visual Studio kapsayıcı araçları seçenekleri: Projeyi Kapat kapsayıcılarında KILL, projede açık gerekli Docker görüntülerini çekme ve projeyi Çalıştır kapsayıcılarında açın.](./media/configure-container-tools/tools-options-2.png)
::: moniker-end

Aşağıdaki tabloda, bu seçenekleri ayarlamak nasıl karar vermenize yardımcı olabilir.

::: moniker range="vs-2017"
| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Otomatik olarak proje yükünde gerekli Docker görüntülerini çekme | Açık | Docker Compose | Proje yüklenirken performansı artırmak için Visual Studio Docker çekme işlemi arka planda böylece kodunuzu çalıştırmak hazır olduğunuzda, görüntü zaten yüklenene veya yükleme sürecinde başlar. Yalnızca projeler yükleniyor ve kod gözatma ise, ihtiyacınız olmayan kapsayıcı görüntülerini yüklenmesini önlemek için kapatabilirsiniz. |
| Kapsayıcıları arka planda otomatik olarak Başlat | Açık | Docker Compose | Yeniden performansı artırmak için Visual Studio kapsayıcı ile birim başlatmalar, derleme ve kapsayıcı çalıştırma için hazır oluşturur. Kapsayıcı oluşturulduğunda denetlemek istiyorsanız, kapatır. |
| KILL çözümdeki kapsayıcıları otomatik olarak Kapat | Açık | Docker Compose | Kapsayıcıları çözümünüzün çözümün kapatılması veya Visual Studio kapatıldıktan sonra çalışmaya devam etmesini istiyorsanız kapatır. |
| İçin localhost SSL sertifikasına güvenme istemi yapma | Kapalı | ASP.NET Core 2.1 projeleri | Localhost SSL sertifikasına güvenilir değilse, bu onay kutusu işaretli değilse, projenizi her çalıştırdığınızda Visual Studio ister. |
::: moniker-end

::: moniker range=">=vs-2019"

Aşağıdaki tabloda açıklanmıştır **genel** ayarları:

| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Docker Masaüstü gerekirse yükleyin | Bana sor | Tek bir proje, Docker Compose | Docker Masaüstü yüklü değilse sorulması isteyip istemediğinizi seçin. |
| ASP.NET Core SSL sertifikasına güven | Bana sor | ASP.NET Core 2.x projeleri | Ayarlandığında **istemi bana**, projenizi her çalıştırdığınızda localhost SSL sertifikasına Visual Studio ister güvenilir değil. |

Aşağıdaki tabloda açıklanmıştır **tek proje** ve **Docker Compose** ayarları:

| Ad | Varsayılan ayar | Uygulanan Öğe | Açıklama |
| -----|:---------------:|:----------:| ----------- |
| Projede açık gerekli Docker görüntülerini çekme | Doğru | Tek bir proje, Docker Compose | Proje yüklenirken performansı artırmak için Visual Studio Docker çekme işlemi arka planda böylece kodunuzu çalıştırmak hazır olduğunuzda, görüntü zaten yüklenene veya yükleme sürecinde başlar. Yalnızca projeler yükleniyor ve kod gözatma, ayarlayabileceğiniz **False** gerekmez kapsayıcı görüntülerini yüklenmesini önlemek için. |
| Kapsayıcıları projede açık Çalıştır | Doğru | Tek bir proje, Docker Compose | Yeniden performansı artırmak için Visual Studio kapsayıcı ile birim başlatmalar, derleme ve kapsayıcı çalıştırma için hazır oluşturur. Kapsayıcı oluşturulduğunda denetlemek istiyorsanız, kümesine **False**. |
| Proje KILL kapsayıcılarında kapatın | Doğru | Tek proje ve Docker Compose | Kümesine **False** kapsayıcıları çözümünüzün çözümün kapatılması veya Visual Studio kapatıldıktan sonra çalışmaya devam etmesini istiyorsanız. |

::: moniker-end
> [!WARNING]
> Ardından localhost SSL sertifikasına güvenilmiyor ve isteyen bastırmak için kutuyu işaretleyin, HTTPS isteklerine uygulamanızı veya hizmetinizi çalışma zamanında başarısız olabilir. Bu durumda, onay kutusunu temizleyin **sorma** onay kutusunu projenizi çalıştırmak ve güven isteminde gösterir.

## <a name="next-steps"></a>Sonraki adımlar

Bu Visual Studio kapsayıcılarıyla çalışma hakkında daha fazla okuma [genel bakış](visual-studio-tools-for-docker.md).