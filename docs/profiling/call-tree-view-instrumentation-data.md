---
title: Çağrı ağacı görünümü - izleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Call Tree view
ms.assetid: 306bd176-0ce9-4a10-89ca-20b043d37d4e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a838a511c5f37a00ed2331d2376b395f399e65d2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56638107"
---
# <a name="call-tree-view---instrumentation-data"></a>Çağrı ağacı görünümü - izleme verileri
Bir işlev çağrısı ağacında için değerleri, çağrı ağacında üst işlev tarafından çağrılan işlev örnekleri için zaman gösterir. Yüzde değerleri, toplam geçen kapsamlı süre işlevi örneklerine profil oluşturma çalıştırmasını tüm işlevlerin değerini karşılaştırılmasıyla hesaplanır.

## <a name="general"></a>Genel
 Genel sütunları bir görünüm satır işlevi tanımlar.

|Sütun|Açıklama|
|------------|-----------------|
|**İşlev adı**|İşlevin adı.|
|**İşlev adresi**|İşlevin adresi.|
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|
|**Çağrı sayısı**|Bu işleve yapılan çağrılar toplam sayısı.|
|**Kaynak dosyası**|Bu işlevin tanımını içeren kaynak dosya.|
|**Modül adı**|İşlevi içeren modül adı.|
|**Modül yolu**|İşlevi içeren modül yolu.|
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|
|**İşlem adı**|İşleme atanan ad.|
|**Zaman dışlamalı araştırma ek yükü**|Zaman ek yükü bu işlev, ölçümlü izlemeyle neden oldu. Tüm özel sürelerinden çıkarıldığında araştırma ek yükü.|
|**Zaman kapsamlı araştırma ek yükü**|Zaman ek yükü Bu işlevde ve alt işlevleri, ölçümlü izlemeyle neden oldu. Tüm kapsamlı sürelerinden çıkarıldığında araştırma ek yükü.|
|**Düzey**|İşlev çağrısı ağacında derinliği. Yalnızca [VSPerfReport](../profiling/vsperfreport.md) komut satırı raporlar.|

## <a name="elapsed-inclusive-values"></a>Geçen kapsamlı değerleri
 Geçen kapsamlı değerleri, çağrı ağacında üst işlev tarafından çağrılan işlev örneklerini çağrı yığınını saati gösterir. Saati, harcanan süre işlev tarafından çağrılan alt işlevler ve bağlam anahtarları ve giriş/çıkış işlemleri gibi işletim sistemi çağrıları içerir.

|Sütun|Açıklama|
|------------|-----------------|
|**Geçen kapsamlı süre**|Bu işlevi bu bağlamda yapılan tüm çağrıların toplam kapsamlı süre.|
|**Geçen kapsamlı süre yüzdesi**|Çalıştıran profil oluşturma toplam geçen kapsamlı süre yüzdesi bu işlevi bu bağlamda toplam geçen kapsamlı süre geçen süre.|
|**Geçen ortalama kapsamlı süre**|Ortalama kapsamlı süre bu bağlamda bu işlev çağrısına geçti.|
|**Geçen maksimum kapsamlı süre**|Maksimum kapsamlı süre bu bağlamda bu işlev çağrısına geçti.|
|**Geçen minimum kapsamlı süre**|Minimum kapsamlı süre bu bağlamda bu işlev çağrısına geçti.|

## <a name="elapsed-exclusive-values"></a>Geçen dışlamalı değerleri
 Geçen dışlamalı değerler, çağrı ağacında üst işlev tarafından çağrılan bir işlev örneklerini işlev gövdesinde kod yürütürken zaman gösterir; diğer bir deyişle, işlev çağrı yığınının başında ne zaman. Zaman zaman bağlam anahtarları ve giriş/çıkış işlemleri gibi işletim sistemi çağrıları içerir. Ancak, zaman işlev tarafından çağrılan işlevlerdeki alt harcanan süreyi içermez.

|Sütun|Açıklama|
|------------|-----------------|
|**Geçen dışlamalı süre**|Toplam bu işlevi bu bağlamda yapılan tüm çağrıların dışlamalı süre geçti.|
|**Geçen dışlamalı süre yüzdesi**|Çalıştıran profil oluşturma toplam geçen dışlamalı süre yüzdesi bu işlevi bu bağlamda toplam geçen dışlamalı süre geçen süre.|
|**Geçen ortalama dışlamalı süre**|Ortalama dışlamalı süre bu bağlamda bu işlev çağrısına geçti.|
|**Geçen maksimum dışlamalı süre**|Maksimum dışlamalı süre bu bağlamda bu işlev çağrısına geçti.|
|**Geçen minimum dışlamalı süre**|Minimum dışlamalı süre bu bağlamda bu işlev çağrısına geçti.|

## <a name="application-inclusive-values"></a>Uygulama kapsamlı değerlerini
 Çağrı yığınındaki bir işlev çağrısı ağacında üst işlev tarafından çağrılan örnekleri olan zaman kapsamlı uygulama değerlerini belirtin. Süresi, bağlam anahtarları ve giriş/çıkış işlemleri gibi işletim sistemi çağrılarında harcanan süreyi içermez, ancak zaman harcanan süre işlev tarafından çağrılan alt işlevler dahil.

|Sütun|Açıklama|
|------------|-----------------|
|**Kapsamlı uygulama süresi**|Bu işlevi bu bağlamda yapılan tüm çağrıların toplam uygulama kapsamlı süre.|
|**Kapsamlı uygulama süresi yüzdesi**|Çalıştıran profil oluşturma toplam geçen kapsamlı süre yüzdesi bu işlevi bu bağlamda kapsamlı toplam uygulama süresi geçen süre.|
|**Ortalama kapsamlı uygulama süresi**|Bu işlevi bu bağlamda bir çağrı, ortalama uygulama kapsamlı süre.|
|**Maksimum kapsamlı uygulama süresi**|Bu bağlamda bu işlev çağrısı en fazla uygulama kapsamlı zamanı.|
|**Minimum kapsamlı uygulama süresi**|En düşük uygulama kapsamlı süre bu işlevi bu bağlamda bir çağırma.|

## <a name="application-exclusive-values"></a>Uygulama özel değerler
 Çağrı ağacında üst işlev tarafından çağrılan bir işlev örneklerini doğrudan işlev gövdesinde kod yürütürken, zaman uygulama özel değerler belirtmek; diğer bir deyişle, işlev çağrı yığınının başında ne zaman. Zaman bağlam anahtarları ve giriş/çıkış işlemleri gibi işletim sistemi çağrılarında harcanan süreyi içermez. Bu ayrıca harcanan süre işlev tarafından çağrılan işlevlerdeki alt içermez.

|Sütun|Açıklama|
|------------|-----------------|
|**Dışlamalı uygulama süresi**|Bu işlevi bu bağlamda yapılan tüm çağrıların toplam uygulama dışlamalı süre.|
|**Dışlamalı uygulama süresi yüzdesi**|Çalıştıran profil oluşturma toplam geçen dışlamalı süre yüzdesi bu bağlamda bu işlevin toplam uygulama dışlamalı süre geçen süre.|
|**Ortalama dışlamalı uygulama süresi**|Bu işlevi bu bağlamda bir çağrı, ortalama uygulama dışlamalı süre.|
|**Maksimum dışlamalı uygulama süresi**|Bu bağlamda bu işlev çağrısı en fazla uygulama özel zamanı.|
|**Minimum dışlamalı uygulama süresi**|En düşük uygulama dışlamalı süre, bu bağlamda bu işlev çağrısı.|

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)
- [Çağrı ağacı görünümü](../profiling/call-tree-view-sampling-data.md)
- [Çağrı ağacı görünümü - izleme](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)
- [Çağrı ağacı görünümü - örnekleme](../profiling/call-tree-view-dotnet-memory-sampling-data.md)