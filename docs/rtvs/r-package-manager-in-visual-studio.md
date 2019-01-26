---
title: R için Paket Yöneticisi
description: R paketi Yöneticisi'nde yüklemek için Visual Studio ve manager R paketleri kullanma
ms.date: 01/24/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 966a05e0b339409a5dc4df247b4ea2101a8a768d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54922853"
---
# <a name="package-manager"></a>Paket yöneticisi

Visual Studio (RTVS) Paket Yöneticisi için R araçları, R paketlerini yönetmek için bir kullanıcı Arabirimi kullanılır. Açmak için seçin **R Araçları** > **Windows** > **paketleri** ya basarak **Ctrl** + **7**.

Paket Yöneticisi üç sekme bulunur. Her sekme, sol taraftaki ilgili paketlerin listesini görüntüler ve diğer ilgili bilgileri için belirli ayrıntıları sağda, paketin sürümü, açıklama, lisansın da dahil olmak üzere seçilen paket için konum ve bağlantı yükleyin. Sağ üst köşedeki arama kutusuna, listeyi filtrelemek sağlar.

> [!Tip]
> Sekmeler arasında geçiş yaptığınızda, arama kutusuna bir terim yürürlükte kalır.

- **Kullanılabilir** paketleri yüklemek için Gözat sağlar. Paket zaten yüklü değilse, **yükleme** sağ taraftaki düğmeyi değişiklikleri **kaldırma**.

    ![R araçları Visual Studio Paket Yöneticisi için sekmesinde kullanılabilir paketler](media/package-manager-available.png)

- **Yüklü** tüm yüklü ve yüklenen paketler gösterilmektedir. Bir paket yanında yeşil bir noktayı R oturuma yüklendiğini gösterir. Kırmızı X simgesini sol taraftaki listenin veya **kaldırma** sağ düğmesi, paketi kaldırmak için kullanılabilir. Yüklü bir paketin daha yeni bir sürümü varsa, mavi yukarı ok sağa paketin bir güncelleştirme gerçekleştirir.

    ![Paketleri sekmesinde Visual Studio Paket Yöneticisi için R araçları yüklü](media/package-manager-installed.png)

- **Yüklenen** R oturuma her biri ile yeşil bir noktayı görünür yüklenen paketleri görüntüler. Ayrıca, kaldırma ve güncelleştirme paketleri burada.

    ![Yüklü paketleri sekmesinde Visual Studio Paket Yöneticisi için R araçları](media/package-manager-loaded.png)

## <a name="package-locations"></a>Paket konumları

Paketler aşağıdaki konumlara yüklenir:

- RTVS ile birlikte gelen temel paketler yüklenir *C:\Program Files\Microsoft\R Client\R_SERVER\library*
- Ek paketler yüklenir *%userprofile%\Documents\R\win-library\3.3*
