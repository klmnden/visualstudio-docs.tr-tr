---
title: Bellek ayırma ve nesne yaşam verisi değerlerini anlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method
- Profiling Tools, .NET memory method
ms.assetid: a22445b3-39a6-4919-8506-2b5b0ceaf77e
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 816f750148cc30de86fc116f80f64b218b4699d0
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60069751"
---
# <a name="understanding-memory-allocation-and-object-lifetime-data-values"></a>Bellek Ayırma ve Nesne Yaşam Verisi Değerlerini Anlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

*.NET bellek ayırma* yöntemi profil oluşturma [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları, boyut ve içinde bir ayırma oluşturulan veya bir çöp toplama yok nesnelerin sayısı ve hakkında ek bilgiler toplar işlevi hakkında bilgi *çağrı yığını* olayın gerçekleştiği. A *çağrı yığını* işlemci üzerinde yürütülen işlevler hakkında bilgi depolayan dinamik bir yapıdır.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
  Bellek profili Oluşturucu, profili oluşturulmuş bir uygulama .NET Framework nesnesinin her ayırma sırasında bilgisayar işlemci kesintiye uğratır. Nesne yaşam verisi ayrıca toplandığında, profil oluşturucu işlemci her .NET Framework çöp toplamanın ardından kesintiye uğratır. Veriler, her nesne türü ve profili oluşturulan her işlev için toplanır.  
  
## <a name="allocation-data"></a>Veri ayırma  
 .Memory olay ortaya çıktığında, toplam sayısı ve bellek ayrılmış veya yok edilmiş nesne boyutu artar.  
  
 .Memory ayırma olay ortaya çıktığında, profil oluşturucu çağrı yığınında her işlev için örnek sayısını artırır. Verileri toplandığında, yalnızca bir işlev çağrı yığınında kodu kendi işlev gövdesindeki şu anda yürütülüyor. Yığında diğer işlevler işlev çağrılarının döndürülecek olarak adlandırılan işlevler için bekleyen sıradüzeni içindeki içindedir.  
  
- Profil Oluşturucu artışlarla ayırma olayının *özel* örnek sayısı, yönergeler şu anda yürüten işlev. Özel bir örnek de toplamın bir parçası olduğundan (*kapsamlı*) örnekleri işlevinin etkin işlev kapsayıcı örnek sayısı da artar.  
  
- Profil Oluşturucu çağrı yığınında diğer tüm işlevlerin kapsamlı örnek sayısını artırır.  
  
## <a name="lifetime-data"></a>Yaşam süresi verisi  
 .NET Framework'ün çöp toplayıcı ayrılmasını ve uygulamanız için bellek serbest yönetir. Atık toplayıcının performansını optimize etmek için Yönetilen yığın üç kuşaklar halinde ayrılmıştır: 0, 1 ve 2. Çalışma zamanı 's atık toplayıcı nesil 0 yeni nesneler depolar. Sonra varlığını sürdüren nesneler yükseltilerek ve depolanan nesil 1 ve 2.  
  
 Çöp toplayıcı tüm nesneleri nesil serbest bırakarak belleği geri kazanır. Profili oluşturulan uygulama oluşturulan nesneler için nesne ömrü görünümü sayısına ve boyutuna nesnelerin ve ne zaman geri alındığını nesil görüntüler.
