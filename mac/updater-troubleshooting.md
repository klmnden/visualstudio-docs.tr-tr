---
title: Güncelleştirici, bilgileri alırken hatalara sahip
description: "' Güncelleştirme bilgilerini alma hatası ' hatasını gördüğünüzde nasıl düzeltileceğini gösteren yönergeler. Mac için Visual Studio 2019"
ms.topic: troubleshooting
author: asb3993
ms.author: amburns
ms.date: 04/13/2019
ms.technology: vs-ide-install
ms.assetid: 31AF914A-C66B-4CD3-9429-39695E0E94AE
ms.openlocfilehash: 5ba295defe19c6f3c6c56d5bccc7cc3fa367bb50
ms.sourcegitcommit: cf8c0fef2b9690595e99ce3802586cdd55fd37c2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70107781"
---
# <a name="troubleshooting-updater-has-errors-retrieving-information"></a>Sorun Giderme: Güncelleştirici, bilgileri alırken hatalara sahip

Nadir bir gün içinde, [Mac için Visual Studio güncelleştirmeyi](update.md)denediğinizde "güncelleştirme bilgileri alınırken hata oluştu" hata iletisini görebilirsiniz. Bu durumda, çözümü onarmak için aşağıdaki adımları deneyin:

- İnternet bağlantınızı kontrol edin. Bu hatanın en yaygın nedeni bağlantıda yer açdır.
  - Bir bileşen indirilemezse, indirmeyi yeniden denemek için bileşen adının yanındaki yeniden dene düğmesine tıklayabilirsiniz.
- IDE 'yi yeniden başlatın.
- Bu hata iletisini görmeye devam ederseniz, **. dmg** hala makinenizde ise yükleyiciyi kullanarak güncelleştirmeyi deneyebilir ya da [VisualStudio.com](https://visualstudio.microsoft.com/vs/mac/) adresinden indirebilirsiniz.
  - Yükleyici, makinenizde yüklü olan tüm bileşenleri güncelleştirecek.
  - Yükleyiciyi yeniden çalıştırarak, daha önce yüklemediyseniz eksik olan bileşenleri de yükleyebilirsiniz.
- Ayrıca, konumunda `~/Library/Caches/VisualStudio/7.0/TempDownload/index.xml`bulunan dosyayı silerek önbelleğe alınmış indirilerinizi temizlemeyi deneyebilirsiniz.
