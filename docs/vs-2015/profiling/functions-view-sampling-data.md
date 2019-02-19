---
title: İşlevler görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method,Functions View
- Functions view
ms.assetid: 029d5ebb-e551-46b0-b64e-2c553d9dbb8e
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 68280c4da20ce063b93b7347cc2857d4a83b9a18
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54769168"
---
# <a name="functions-view---sampling-data"></a>İşlevler Görünümü - Örnekleme Verileri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Örnekleme profili yöntemi için işlevleri rapor görünümü, profil oluşturma sırasında örneklenen işlevleri listeler.  
  
> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)   
 [İşlevler görünümü - izleme](../profiling/functions-view-dotnet-memory-instrumentation-data.md)   
 [İşlevler görünümü - örnekleme](../profiling/functions-view-dotnet-memory-sampling-data.md)   
 [İşlevler Görünümü](../profiling/functions-view-instrumentation-data.md)
