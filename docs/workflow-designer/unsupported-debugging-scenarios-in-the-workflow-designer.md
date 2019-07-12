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
ms.openlocfilehash: 9cda710a3a2f4945e96e706479996da0a1fa7e12
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67825730"
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
