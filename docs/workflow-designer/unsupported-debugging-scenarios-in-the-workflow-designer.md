---
title: İş Akışı Tasarımcısında desteklenmeyen hata ayıklama senaryoları
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.assetid: 6adbe379-41d0-4681-9cd0-b91f187c3c2c
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 88fa196d5df085249282e595031bbde09ba071a7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53858636"
---
# <a name="unsupported-debugging-scenarios-in-the-workflow-designer"></a>İş Akışı Tasarımcısında desteklenmeyen hata ayıklama senaryoları

İş Akışı Tasarımcısı .NET Framework 4'teki birçok yeni özellikler eklenmiştir, ancak yine de desteklemediği hata ayıklama bazı senaryolar verilmiştir.

Desteklenmeyen iş akışı Tasarımcısı'nin hata ayıklama senaryoları şunlardır:

-   Kodu düzenlenmiş sonra yürütülmesine devam ettirilemez.

-   Yürütme iş akışının (sonraki ayarlayın) içindeki rastgele bir noktadan devam ettirilemez.

-   İmleç (imlece kadar Çalıştır) ulaşılana kadar yürütmeyi devam ettirilemez.

-   İş Akışı Tasarımcısı, tasarımcıyı kullanmadan kodda oluşturulan iş akışlarında hata ayıklamak için kullanılamaz.

-   .NET Framework 4 Tasarımcısı'nda oluşturulan önceki sürümlerinde Windows Workflow Foundation (WF) iş akışı hata ayıklaması yapılamaz.

-   Kesme noktaları, etkinlikleri arasındaki bağlantıları tanımlanamıyor veya <xref:System.Activities.Statements.Flowchart> düğümleri.

-   Pano hata ayıklama sırasında kullanılamaz.

-   Etkinlikleri kopyalandığında veya yapıştırdığınız kesme noktaları korunmaz.

-   İş akışı kesme noktaları, çağrı yığını penceresinde olacak şekilde ayarlanamaz.

-   Kesme noktaları Tasarımcısı'nda oluştururken **satırı** ve **karakter** ayarlarında **yeni kesme noktası** iletişim kullanılmaz.

-   Kesme noktası penceresi ya da kısayol menüsünde aşağıdaki sütunları veya seçenekler iş akışı hata ayıklama için desteklemez:

    -   Koşul

    -   İsabet sayısı

    -   İsabet edildiğinde

    -   İşlev

    -   Veri

    -   İşlem

    -   Ayrıştırma için Git