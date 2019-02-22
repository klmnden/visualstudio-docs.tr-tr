---
title: İşlevler görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method,Functions View
- Functions view
ms.assetid: 029d5ebb-e551-46b0-b64e-2c553d9dbb8e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c734c7eb5ad6aed489d1c6d2ffb8cd774be6fdd7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56624327"
---
# <a name="functions-view---sampling-data"></a>İşlevler görünümü - örnekleme verileri
Örnekleme profili yöntemi için işlevleri rapor görünümü, profil oluşturma sırasında örneklenen işlevleri listeler.

> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

|Sütun|Açıklama|
|------------|-----------------|
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|
|**İşlem adı**|İşlemin adı.|
|**Modül adı**|İşlevi içeren modül adı.|
|**Modül yolu**|İşlevi içeren modül yolu.|
|**Kaynak dosyası**|Bu işlevin tanımını içeren kaynak dosya.|
|**İşlev adı**|İşlev tam adı.|
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|
|**İşlev adresi**|İşlevin adresi.|
|**Kapsamlı örnekler**|Bu işlev yürütülürken, toplanan örneklerin toplam sayısı; diğer bir deyişle, bu işlev çağrı yığını üzerinde olduğu zaman, toplanan örnek sayısı. Bu işlev tarafından çağrılan işlevler yürütülürken toplanan örnekler içerir.|
|**Kapsamlı örnek yüzdesi**|Profil çalıştıran tüm örneklerin yüzdesi, bu işlevin kapsamlı örnekler yoktu.|
|**Dışlamalı örnekler**|Bu işlev gövdesinde kod yürütürken, toplanan örneklerin toplam sayısı; diğer bir deyişle, bu işlev çağrı yığınının üzerinde ne zaman. Bu işlev tarafından çağrılan işlevler toplanan örnekler dahil edilmez.|
|**Dışlamalı örnek yüzdesi**|Profil çalıştıran tüm örneklerin yüzdesi, bu işlevin dışlamalı örnekler yoktu.|

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)
- [İşlevler görünümü - izleme](../profiling/functions-view-dotnet-memory-instrumentation-data.md)
- [İşlevler görünümü - örnekleme](../profiling/functions-view-dotnet-memory-sampling-data.md)
- [İşlevler Görünümü](../profiling/functions-view-instrumentation-data.md)