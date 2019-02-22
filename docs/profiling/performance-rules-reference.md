---
title: Performans kuralları başvurusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 59fc9424-76ca-4365-ae47-bb14a736c9c2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ad4cdb96a8d342e191e5c6e92e2916f49fd6406d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56609858"
---
# <a name="performance-rules-reference"></a>Performans Kuralları Başvurusu
Profil Araçları performans kurallarını, ek uyarılar ve uygulamanızın performansı hakkında bilgi sağlar. Performans kuralları profil oluşturma yürütmesine Windows ve işlemci performans sayaçları gibi kaynaklardan toplanan verileri analiz edin. Kural iletileri hata çıkış penceresinde görünür [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] tümleşik geliştirme ortamı. İletiler, aşağıdaki kural düzeylerinden birini listelenmiştir:

|||
|-|-|
|**Hata:**|Çoğu performans sorunlarını yükseltebilir hataları olmadığından bazı kurallar hata iletileri oluşturur. Bir hata iletisi, profil oluşturma verilerini toplamak için bir hata gösterebilir.|
|**Uyarı**|Uyarılar, olası performans sorunlarını kaynağı olabilir veya iyileştirmeler avantajlı olmayabilir, uygulamanızın bir bölümünü gösterir.|
|**Bilgi**|Bilgi iletilerini analizi bir kural koşulu, bir hata iletisi oluşturmak için eşiği ulaşmadı veya bilgi iletisi kullanışlıdır ancak bir performans sorunu yansıtmaz gösterir.|

## <a name="in-this-section"></a>Bu Bölümde

[Kimliğe Göre Performans Kuralları](../profiling/performance-rules-by-id.md)

Profil Araçları performans kuralları dört kategoriler halinde düzenlenmiştir:

|||
|-|-|
|[.NET Framework Kullanımı Performans Kuralları](../profiling/dotnet-framework-usage-performance-rules.md)|Yardımcı kurallar, .NET Framework verimli bir şekilde kullanın.|
|[Bellek ve Disk Belleği Performans Kuralları](../profiling/memory-and-paging-performance-rules.md)|Yönetilen bellek ve disk belleği uygulamanızın davranışını analiz kuralları.|
|[Profil Araçları Kullanım Kuralları](../profiling/profiling-tools-usage-rules.md)|Yardımcı kuralları profil oluşturma araçları verimli bir şekilde kullanın.|
|[Kaynak İzleme Performans Kuralları](../profiling/resource-monitoring-performance-rules.md)|İşlemci ve bellek kullanımı, bir profil oluşturma hakkında bilgi iletileri çalıştırın.|