---
title: Bellek ayırma ve nesne yaşam verisi değerlerini anlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- Profiling Tools, .NET memory method
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9fc9dd62c3d264d3b502845cb4d0f3e9c2a8fa78
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56615149"
---
# <a name="understand-memory-allocation-and-object-lifetime-data-values"></a>Bellek ayırma ve nesne yaşam verisi değerlerini anlama

*.NET bellek ayırma* yöntemi profil oluşturma [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları, boyut ve içinde bir ayırma oluşturulan veya bir çöp toplama yok nesnelerin sayısı ve hakkında ek bilgiler toplar işlevi hakkında bilgi *çağrı yığını* olayın gerçekleştiği. A *çağrı yığını* işlemci üzerinde yürütülen işlevler hakkında bilgi depolayan dinamik bir yapıdır.

Bellek profili Oluşturucu, profili oluşturulmuş bir uygulama .NET Framework nesnesinin her ayırma sırasında bilgisayar işlemci kesintiye uğratır. Nesne yaşam verisi ayrıca toplandığında, profil oluşturucu işlemci her .NET Framework çöp toplamanın ardından kesintiye uğratır. Veriler, her nesne türü ve profili oluşturulan her işlev için toplanır.

## <a name="allocation-data"></a>Veri ayırma

.Memory olay ortaya çıktığında, toplam sayısı ve bellek ayrılmış veya yok edilmiş nesne boyutu artar.

.Memory ayırma olay ortaya çıktığında, profil oluşturucu çağrı yığınında her işlev için örnek sayısını artırır. Verileri toplandığında, yalnızca bir işlev çağrı yığınında kodu kendi işlev gövdesindeki şu anda yürütülüyor. Yığında diğer işlevler işlev çağrılarının döndürülecek olarak adlandırılan işlevler için bekleyen sıradüzeni içindeki içindedir.

- Profil Oluşturucu artışlarla ayırma olayının *özel* örnek sayısı, yönergeler şu anda yürüten işlev. Özel bir örnek de toplamın bir parçası olduğundan (*kapsamlı*) örnekleri işlevinin etkin işlev kapsayıcı örnek sayısı da artar.

- Profil Oluşturucu çağrı yığınında diğer tüm işlevlerin kapsamlı örnek sayısını artırır.

## <a name="lifetime-data"></a>Yaşam süresi verisi

.NET Framework'ün çöp toplayıcı ayrılmasını ve uygulamanız için bellek serbest yönetir. Atık toplayıcının performansını optimize etmek için Yönetilen yığın üç kuşaklar halinde ayrılmıştır: 0, 1 ve 2. Çalışma zamanı 's atık toplayıcı nesil 0 yeni nesneler depolar. Sonra varlığını sürdüren nesneler yükseltilerek ve depolanan nesil 1 ve 2.

Çöp toplayıcı tüm nesneleri nesil serbest bırakarak belleği geri kazanır. Profili oluşturulan uygulama oluşturulan nesneler için nesne ömrü görünümü sayısına ve boyutuna nesnelerin ve ne zaman geri alındığını nesil görüntüler.