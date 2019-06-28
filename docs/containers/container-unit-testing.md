---
title: Birim testi kapsayıcılı uygulama
author: ghogen
description: Her derleme için Visual Studio'da Docker projesi ile birim testleri çalıştırma
ms.author: ghogen
ms.date: 06/17/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: ec5aea44362cf82f6745671cc0706f80e01a60ad
ms.sourcegitcommit: 0cd282a7584b9bfd4df7882f8fdf3ad8a270e219
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67467412"
---
# <a name="how-to-run-unit-tests-for-a-containerized-app"></a>Nasıl yapılır: Kapsayıcılı bir uygulama için birim testleri çalıştırma

Dockerfile değiştirerek kapsayıcılı projenizin her derleme ile birim testleri çalıştırabilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

- [Docker Masaüstü](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
- Yükleme [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)
- Birim testleri ayarlama kullanarak çalışacak şekilde [dotnet testi](/dotnet/core/tools/dotnet-test)
- Yükleme [kapsayıcıları penceresini genişletme](https://aka.ms/vscontainerspreview)

## <a name="add-unit-tests-to-the-dockerfile"></a>Birim testleri için bir Dockerfile Ekle

Visual Studio, Dockerfile değiştirmeden önce bazı özel performans iyileştirmeleri desteklemez. Oluşturma sırasında **hata ayıklama** yapılandırma, Visual Studio yerel makinede projeleri derler ve sonuçları kapsayıcıya kopyalar. Bu nedenle, aşamalı Dockerfile yalnızca ilk aşamasında yürütülen Dockerfile içinde belirtildiği gibi. Daha fazla bilgi için [derleme işlemi için Visual Studio kapsayıcı Araçları](container-build.md).

Bir aşamalı Dockerfile için birim testleri eklemek için Ekle bir `unit-test` arasında Dockerfile aşamasına `build` ve `publish` aşamaları.

```
FROM build AS unit-test
RUN dotnet unit-test --logger:trx
```

Visual Studio yalnızca çalışan ilk aşama **hata ayıklama** yapılandırma, bu nedenle `unit-test` aşama çalıştırmak yalnızca **yayın** yapılandırma. Ama bile **yayın** yapılandırma, sonuçları son görüntü oluşturulur çünkü son görüntüde bulunmayacaktır günlük `base` aşama, yerine `unit-test` aşaması. Testleri çalıştırmak ve günlükleri görüntüleyebileceğiniz bir görüntü oluşturmak için aşağıdaki komutu kullanın:

```cmd
docker build --target:unit-test
```

## <a name="next-steps"></a>Sonraki adımlar

Ardından [Zobrazit okno](view-and-diagnose-containers.md) (uzantı yüklü varsa) test görüntülemek üzere günlüğe kaydeder.  

Test günlüklerinizi görüntülemek için kullanın **Ctrl**+**Q** araması **kapsayıcıları** açmak için **kapsayıcıları** penceresi. İçinde **kapsayıcıları** penceresinde kapsayıcınızı, açık Bul **dosyaları** sekmesinde, arama, test sonuçları (.trx) dosyası içinde kapsayıcının dosya sistemi ve Visual Studio'da sonuçlarını görüntülemek için açın.

