---
title: Kanallar (iş parçacıkları görünümü) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.channelnames
helpviewer_keywords:
- Concurrency Visualizer, Channels (Threads View)
ms.assetid: 2f798c17-2363-42a4-be94-a5751d208eac
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 94ac6e9e85a2d7dd504b2d2bd83bd1bbdb265ea0
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56642852"
---
# <a name="channels-threads-view"></a>Kanallar (iş parçacıkları görünümü)
Eşzamanlılık görselleştiricisi kanalları dört tür gösterir: iş parçacığı kanalları, disk kanalları, işaret Kanallar ve GPU kanalları.

## <a name="thread-channels"></a>İş parçacığı kanallar
 Bir iş parçacığı kanalı, renk, yalnızca bir iş parçacığı tarafından iş parçacığı durumu gösterir. Verilen iş parçacığı için Başlat işlevi, kanal adına duraklattığımda görüntülenir. Eşzamanlılık görselleştiricisi çeşitli türden iş parçacıklarıyla algılar. En yaygın türü aşağıdaki tabloda gösterilmektedir.

|||
|-|-|
|Ana iş parçacığı|Uygulama başlangıç iş parçacığı.|
|Çalışan iş parçacığı|Uygulamanın ana iş parçacığı tarafından oluşturulmuş bir iş parçacığı.|
|CLR çalışan iş parçacığı|Ortak dil çalışma (CLR) tarafından oluşturulan çalışan iş parçacığı.|
|Hata ayıklayıcı Yardımcısı|Visual Studio hata ayıklayıcı tarafından oluşturulan çalışan iş parçacığı.|
|ConcRT iş parçacığı|Microsoft eşzamanlılık çalışma zamanı tarafından oluşturulan bir iş parçacığı.|
|GDI iş parçacığı|Varsayılmaktadır tarafından oluşturulmuş bir iş parçacığı.|
|OLE/RPC iş parçacığı|Bir RPC iş parçacığı oluşturulmuş bir iş parçacığı.|
|RPC iş parçacığı|Bir RPC iş parçacığı oluşturulmuş bir iş parçacığı.|
|Winsock iş parçacığı|Winsock iş parçacığı oluşturulmuş bir iş parçacığı.|
|İş parçacığı havuzu|CLR iş parçacığı havuzu tarafından oluşturulmuş bir iş parçacığı.|

## <a name="disk-channels"></a>Disk kanallar
 Disk kanalları, fiziksel bilgisayardaki sürücüleri karşılık gelir. Okuma ve yazma işlemleri için farklı bir kanal sistem üzerindeki her fiziksel sürücü olduğundan, her sürücü iki kanal içerir. Disk numaralarını çekirdek cihaz adlara karşılık gelir. Bir disk kanal yalnızca diskte etkinliği olup olmadığını gösterilir.

## <a name="marker-channels"></a>İşaret kanallar
 İşaret kanalları, uygulama ve kullandığı kitaplıkları tarafından oluşturulan olayları karşılık gelir. Örneğin, görev paralel kitaplığı, paralel desenler kitaplığı ve C++ AMP işaretçileri olarak görüntülenen olayları oluşturur. Kanal açıklaması yanında görüntülenen bir iş parçacığı kimliği ile ilişkili her işaret kanalıdır. Olayı oluşturan iş parçacığı kimliği tanımlar. Kanal açıklaması, olaylar için olay izleme Windows (ETW) sağlayıcısı adını içerir. Kanal, olaylarından görüntülerse [eşzamanlılık görselleştiricisi SDK'si](../profiling/concurrency-visualizer-sdk.md), seri adı da görüntülenir.

## <a name="gpu-channels"></a>GPU kanallar
 GPU kanalları sistemde DirectX 11 etkinliği hakkındaki bilgileri görüntüler.  Grafik kartı ile ilişkili her DirectX altyapısı, ayrı bir kanalı vardır.  Tek tek parçaları DMA paket işlenmesi için harcanan zamanı temsil eder.

## <a name="see-also"></a>Ayrıca bkz.
- [İş Parçacıkları görünümü](../profiling/threads-view-parallel-performance.md)