---
title: Hata ayıklama senaryoları iş akışı tasarımcısında desteklenmeyen | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
ms.assetid: 6adbe379-41d0-4681-9cd0-b91f187c3c2c
caps.latest.revision: 4
author: steved0x
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2f9799aa821c2281c8d7889009871e28a72dd5f6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788083"
---
# <a name="unsupported-debugging-scenarios-in-the-workflow-designer"></a>İş Akışı Tasarımcısında desteklenmeyen hata ayıklama senaryoları
İş Akışı Tasarımcısı'nda [!INCLUDE[netfx40_short](../includes/netfx40-short-md.md)] birçok yeni özellikler eklenmiştir, ancak yine de desteklemediği hata ayıklama bazı senaryolar verilmiştir. Bu belge, iş akışı Tasarımcısı ile hata ayıklama senaryoları desteklenmeyen ayrıntıları.  
  
-   Kodu düzenlenmiş sonra yürütülmesine devam ettirilemez.  
  
-   Yürütme iş akışının (sonraki ayarlayın) içindeki rastgele bir noktadan devam ettirilemez.  
  
-   İmleç (imlece kadar Çalıştır) ulaşılana kadar yürütmeyi devam ettirilemez.  
  
-   İş Akışı Tasarımcısı, tasarımcıyı kullanmadan kodda oluşturulan iş akışlarında hata ayıklamak için kullanılamaz.  
  
-   ' In önceki sürümlerinde oluşturulan iş akışları [!INCLUDE[wf](../includes/wf-md.md)] içinde ayıklanamıyor [!INCLUDE[netfx40_short](../includes/netfx40-short-md.md)] Tasarımcısı.  
  
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