---
title: 'Nasıl Yapılır: Performans kuralları yapılandırma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.ruleseditor
ms.assetid: a148b468-b849-4858-880a-808a6b47e596
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2e3df3b6573bb82303e0412fe50665c86d082481
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53879617"
---
# <a name="how-to-configure-performance-rules"></a>Nasıl Yapılır: Performans kurallarını yapılandırma
Th Visual Studio Profil Araçları Performans uyarılarını, program yürütme yavaşlatabilir profili oluşturulmuş bir uygulamada sorunları gösterir. Uyarı toplama metotlarını daha kullanışlı verileri toplamak için değiştirmeniz gerekebilir de belirtebilir. Performans uyarıları profil oluşturma oturumunu otomatik olarak oluşturulur ve görünür **hata listesi** bir profil oluşturma veri dosyasını açıldığında penceresi [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)]. Belirli uyarıları ilgilendiğiniz ve bazı uyarılar oluştu zamanlayıcılara harekete Geçirilmemesi senaryoları için geçerli olmayabilir. Belirli uyarıları gizlemek veya göstermek için Performans uyarılarını yapılandırabilirsiniz.  
  
### <a name="to-configure-profiler-performance-warnings"></a>Profil Oluşturucu Performans uyarılarını yapılandırmak için  
  
1.  Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.  
  
2.  Genişletin **performans araçları**ve ardından **kuralları**.  
  
3.  Bir uyarıyı devre dışı bırakmak veya etkinleştirmek için seçin veya uyarı yanındaki onay kutusunu temizleyin **kimliği** ve adı.  
  
4.  Bir kural hanedan arasındaki düzeyini belirtmek için **eylem** hücre yanındaki kural ve uyarı düzeyi'ye tıklayın.  
  
    -   **Devre dışı bırakılmış** -(Bu, kural kimliği yanındaki onay kutusunu temizleyerek ile aynı) kuralı devre dışı bırakır.  
  
    -   **Uyarı** -uyarı kuralı görüntüler.  
  
    -   **Hata** - yürütme profil oluşturmayı durdurur ve kuralın hata olarak görüntüler.  
  
    -   **Bilgi** -görüntüler kural yalnızca bilgi olarak.