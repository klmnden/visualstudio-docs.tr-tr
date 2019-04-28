---
title: 'Nasıl yapılır: Performans kuralları yapılandırma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.ruleseditor
ms.assetid: a148b468-b849-4858-880a-808a6b47e596
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7387cc54e96aec4deea6a65875f693d704d51859
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62973974"
---
# <a name="how-to-configure-performance-rules"></a>Nasıl yapılır: Performans kurallarını yapılandırma
Th Visual Studio Profil Araçları Performans uyarılarını, program yürütme yavaşlatabilir profili oluşturulmuş bir uygulamada sorunları gösterir. Uyarı toplama metotlarını daha kullanışlı verileri toplamak için değiştirmeniz gerekebilir de belirtebilir. Performans uyarıları profil oluşturma oturumunu otomatik olarak oluşturulur ve görünür **hata listesi** bir profil oluşturma veri dosyasını açıldığında penceresi [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)]. Belirli uyarıları ilgilendiğiniz ve bazı uyarılar oluştu zamanlayıcılara harekete Geçirilmemesi senaryoları için geçerli olmayabilir. Belirli uyarıları gizlemek veya göstermek için Performans uyarılarını yapılandırabilirsiniz.

### <a name="to-configure-profiler-performance-warnings"></a>Profil Oluşturucu Performans uyarılarını yapılandırmak için

1. Üzerinde **Araçları** menüsünü tıklatın **seçenekleri**.

2. Genişletin **performans araçları**ve ardından **kuralları**.

3. Bir uyarıyı devre dışı bırakmak veya etkinleştirmek için seçin veya uyarı yanındaki onay kutusunu temizleyin **kimliği** ve adı.

4. Bir kural hanedan arasındaki düzeyini belirtmek için **eylem** hücre yanındaki kural ve uyarı düzeyi'ye tıklayın.

    - **Devre dışı bırakılmış** -(Bu, kural kimliği yanındaki onay kutusunu temizleyerek ile aynı) kuralı devre dışı bırakır.

    - **Uyarı** -uyarı kuralı görüntüler.

    - **Hata** - yürütme profil oluşturmayı durdurur ve kuralın hata olarak görüntüler.

    - **Bilgi** -görüntüler kural yalnızca bilgi olarak.