---
title: Olay açıklamaları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], events
ms.assetid: 09f61652-7e16-4bb0-8055-f61a84bf384e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d5a1567cc7f5d3f6072b47fda1aacd32f69cb672
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695290"
---
# <a name="event-descriptions"></a>Olay açıklamaları
Her olay türüne belirli bir amacı vardır.

## <a name="events-and-the-reasons-for-their-use"></a>Olayları ve bunların kullanılması için nedenler

|Olay|Açıklama|
|-----------|-----------------|
|Belge olayları etkinleştirme|Hata ayıklama altyapısı (DE) veya belge öne getirmek IDE istediğinde gerçekleşir.|
|Bağlı kesme noktası veya kesme noktası hata olayları|Gönderilen bir kesme noktası bağlı olduğunu veya ne zaman bir kesme noktası bağlanamıyor ve bir hata döndürdü.|
|İlişkisiz bir kesme noktası olayları|İlişkili bir kesme noktası koddan keser ortaya çıkar.|
|Olayları durdurabilirsiniz|Kullanıcı kodunda belirtilen bir noktada durdurmak isteyip istemediğinizi belirlemek için IDE gönderdi.|
|Kesme noktası olayları|Bir kod veya veri kesme noktası isabet edildiğinde gerçekleşir.|
|Belge metin olayları|Bir belgenin metni değiştiğinde oluşur. Bu olayları aracılığıyla gönderilmez `IDebugEventCallBack2::Event` yöntemi.|
|Altyapı olayları oluşturma|Altyapının oluşturulduğunda gönderilir.|
|Giriş noktası olayları|Hata ayıklanan programa başlatma kodunu çalıştırın ya da kendi ilk kullanıcı giriş noktası sınırına gönderilir.|
|Özel durum olayları|Çalışan bir program ulaştığında bir özel durum gönderilir.|
|İfade değerlendirme tam olayları|Zaman uyumsuz bir ifade değerlendirme işlemi tamamlandıktan sonra gönderilir.|
|Sembol etkinlik bulun|Bir modül için sembolleri Bul kullanıcıdan DE gerektiğinde gönderilir.|
|Tam olay yükle|Yalnızca ilk program yükleme tamamlandıktan ve programı çalıştırmak üzere ilk kodudur gönderilir.|
|İleti olayları|Kullanıcılara gönderilen iletileri gönderilir.|
|Modül yükleme olayları|Yeni bir modül yüklendiğinde veya kaldırılmış gönderilir.|
|Çıkış dizesi olayları|Programın hata ayıklama çıkışını yazdığında gönderilir.|
|Oluşturma ve yok etme olayları|Visual Studio IDE hataları ayıklanmakta olan program durumunu izlemek için oluşturma veya yok etme işlemleri, programlar, özellikleri, oturumları ve iş parçacıkları duyurmaktan gönderdi.|
|Adım Tamamlandı olayları|Bir adım tamamlandıktan sonra gönderilir.|
|İş parçacığı adı değişikliği olayları|Kullanıcı bir iş parçacığı adı değiştiğinde gönderilir.|
|Program adı değişikliği olayları|Kullanıcı bir program adı değiştiğinde gönderilir.|

## <a name="see-also"></a>Ayrıca bkz.
- [Olayları gönderme](../../extensibility/debugger/sending-events.md)