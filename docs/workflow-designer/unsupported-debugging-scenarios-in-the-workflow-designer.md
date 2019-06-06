---
title: İş Akışı Tasarımcısında desteklenmeyen hata ayıklama senaryoları
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 6adbe379-41d0-4681-9cd0-b91f187c3c2c
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 62d8a2ad847ef1b9aaad02b2739e8154b3148425
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66747263"
---
# <a name="unsupported-debugging-scenarios-in-the-workflow-designer"></a>İş Akışı Tasarımcısında desteklenmeyen hata ayıklama senaryoları

İş Akışı Tasarımcısı aşağıdaki hata ayıklama senaryoları desteklemez:

- Kodu düzenlenmiş sonra yürütülmesine devam ettirilemez.

- Yürütme iş akışının (sonraki ayarlayın) içindeki rastgele bir noktadan devam ettirilemez.

- İmleç (imlece kadar Çalıştır) ulaşılana kadar yürütmeyi devam ettirilemez.

- İş Akışı Tasarımcısı, tasarımcıyı kullanmadan kodda oluşturulan iş akışlarında hata ayıklamak için kullanılamaz.

- .NET Framework 4 veya sonraki bir sürümünde oluşturulan önceki sürümlerinde Windows Workflow Foundation (WF) iş akışı hata ayıklanamıyor.

- Kesme noktaları, etkinlikleri arasındaki bağlantıları tanımlanamıyor veya <xref:System.Activities.Statements.Flowchart> düğümleri.

- Pano hata ayıklama sırasında kullanılamaz.

- Etkinlikleri kopyalandığında veya yapıştırdığınız kesme noktaları korunmaz.

- İş akışı kesme noktaları, çağrı yığını penceresinde olacak şekilde ayarlanamaz.

- Kesme noktaları Tasarımcısı'nda oluştururken **satırı** ve **karakter** ayarlarında **yeni kesme noktası** iletişim kullanılmaz.

- Kesme noktası penceresi ya da kısayol menüsünde aşağıdaki sütunları veya seçenekler iş akışı hata ayıklama için desteklemez:

    - Koşul

    - İsabet sayısı

    - İsabet edildiğinde

    - İşlev

    - Veri

    - İşlem

    - Ayrıştırma için Git