---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: İş Akışı Tasarımcısı ile XAML Hatalarını Ayıklama'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d9305dbc-af62-4bdd-b03f-c54e3fe9ecc7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: cdbf5fa21c8fcf9069db9a7348d4ed576fc342c5
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60065889"
---
# <a name="how-to-debug-xaml-with-the-workflow-designer"></a>Nasıl yapılır: İş Akışı Tasarımcısı ile XAML Hatalarını Ayıklama

İş akışı XAML açısından tanımlanır. İş akışı UI gösterimini iş akışını tanımlayan XAML ağaç üzerinde oluşturulmuştur. Hata ayıklama deneyimini, iş akışı Tasarımcısı iş akışlarında hata ayıklama için benzerdir. İş Akışı Tasarımcısı hata ayıklama yaparken, XAML hata ayıklarken yerel öğeler, izleme ve iş parçacıkları windows aynı şekilde çalışır. Ayrıca, XAML hata ayıklama sırasında çağrı yığınını görüntüle satırı tabanlı hiyerarşik bir görünümü yürütme akış iş akışı için ' dir.

> [!NOTE]
> XAML iş akışı için etkinlikler aynı bütünleştirilmiş kod bulunuyorsa, sınıf adları derleme kısmı dahil değildir. Sınıf (etkinlik) adları bu kısmı XAML çalışma zamanında yüklenemez. Ana proje ile aynı ad alanında etkinlikleri tanımlamak için önerilmez; Aksi takdirde, XAML Tasarımcısı'nda düzenlenebilir sonra elle düzenlenerek olması gerekir.

## <a name="to-debug-workflow-xaml"></a>İş akışı XAML hatalarını ayıklamak için

1. Bir iş akışı veya etkinlik projesini Visual Studio'da açın.

2. Bölümünde anlatıldığı gibi ayıklamak istediğiniz etkinlikleri ve etkinlik üzerinde bir kesme noktası ayarlamak [nasıl yapılır: İş akışlarında kesme noktası ayarlama](../workflow-designer/how-to-set-breakpoints-in-workflows.md).

3. Seçin ve iş akışı tanımını içeren .xaml dosyasını sağ tıklatın **kodu görüntüle**. Tasarım görünümünde kesme noktasına kümesi etkinliğin XAML öğe bildirimi ile aynı satırda görüntülenen bir kesme noktası görürsünüz.

4. Hata ayıklayıcısı içinde açıklanan şekilde çağırır [iş akışı hata ayıklama](debugging-workflows-with-the-workflow-designer.md).

5. Kod yürütmeyi kesme noktalarınız ulaştığında, o kesme noktası ile ilişkili XAML öğe vurgulanır. Sonraki kesme noktasına gidin, **F10** veya **F11** anahtarı.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: İş Akışlarında Kesme Noktası Ayarlama](../workflow-designer/how-to-set-breakpoints-in-workflows.md)
- [İş akışı hata ayıklama](debugging-workflows-with-the-workflow-designer.md)