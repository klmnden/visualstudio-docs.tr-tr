---
title: Güncelleştirici bilgileri alınırken hata var
description: "' % S'hata 'güncelleştirme bilgisi alınırken hata oluştu' gördüğünüzde, düzeltme hakkında yönergeler. Mac için Visual Studio 2019 içinde"
author: asb3993
ms.author: amburns
ms.date: 04/13/2019
ms.technology: vs-ide-install
ms.assetid: 31AF914A-C66B-4CD3-9429-39695E0E94AE
ms.openlocfilehash: ef0d1f7516c410475f467ecaadecbb0aeaac71a3
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67825724"
---
# <a name="troubleshooting-updater-has-errors-retrieving-information"></a>Sorun Giderme: Güncelleştirici bilgileri alınırken hata var

Nadir durumlarda, hata iletisi "hata bilgilerini güncelleştirmek için denediğinizde görüntülenen alma" görebilirsiniz [Mac için Visual Studio güncelleştirme](update.md). Bu durumda, sorunu gidermek için aşağıdaki adımları deneyin:

- İnternet bağlantınızı kontrol edin. Bir drop bağlantı, bu hatanın en yaygın nedeni ise.
  - İndirmek bir bileşenin başarısız olursa yeniden deneme düğmesi indirmeyi yeniden denemek için bileşen adının yanındaki tıklayabilirsiniz.
- IDE yeniden başlatın.
- Bu hatayı görmeye devam ederseniz, ayrıca Yükleyicisi'ni kullanarak güncelleştirmek deneyebilirsiniz **.dmg** , makine üzerinde hala veya buradan indirebileceğiniz [visualstudio.com](https://visualstudio.microsoft.com/vs/mac/)
  - Yükleyici, makinenizde yüklü bileşenler güncelleştirir.
  - Yükleyici tekrar çalıştırarak, ayrıca daha önce yüklü tüm eksik bileşenleri yüklemek mümkün olacaktır.
- Önbelleğe alınan indirmelerinizi konumundaki dosya silerek temizleme de deneyebilirsiniz `~/Library/Caches/VisualStudio/7.0/TempDownload/index.xml`.
