---
title: İşlevler görünümü - .NET bellek örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Functions view
ms.assetid: 5d9c6302-2ffd-430e-9535-13ce795f9f7c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: b2e25e1106741e3ebb81bbff52fd5bc75368e806
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54941122"
---
# <a name="functions-view---net-memory-sampling-data"></a>İşlevler görünümü - .NET bellek örnekleme verileri
.NET bellek ayırma profil oluşturma örnekleme yöntemiyle toplanan veriyi işlevler görünümünü ayırmaların sayısı ve boyutu raporlar ve profil oluşturma çalışması süresince bellek ayrılan işlevler listelenir.  
  
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
|**Kapsamlı ayırmalar**|Bu işlevde ve alt işlevleri ayrılmış nesneleri toplam sayısı.|  
|**Kapsamlı ayırma yüzdesi**|Yüzdesi, profil oluşturma çalışmasında ayrılan tüm nesneler, bu işlevin kapsamlı ayırmalar yoktu.|  
|**Dışlamalı ayırmalar**|İşlev çağrı yığınının başında doğrudan yürütülürken, oluşturulan nesne sayısı. Bu sayı, alt işlevlerde oluşturulan nesneleri içermez.|  
|**Dışlamalı ayırma yüzdesi**|Yüzdesi, profil oluşturma çalışmasında ayrılan tüm nesneler, bu işlevin dışlamalı ayırmalar yoktu.|  
|**Kapsamlı bayt**|Bu işlevde ve alt işlevleri tarafından ayrılan bellek bayt sayısı.|  
|**Kapsamlı bayt yüzdesi**|Bu işlevin kapsamlı bayt olan, profil oluşturma çalışmasında ayrılan tüm bellek bayt yüzdesi.|  
|**Dışlamalı bayt**|Bu işlev tarafından ancak alt işlevleri tarafından ayrılan bellek bayt sayısı.|  
|**Dışlamalı bayt yüzdesi**|Bu işlevin dışlamalı bayt olan, profil oluşturma çalışmasında ayrılan tüm bellek bayt yüzdesi.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [İşlevler görünümü - izleme](../profiling/functions-view-dotnet-memory-instrumentation-data.md)   
 [İşlevler görünümü](../profiling/functions-view-sampling-data.md)   
 [İşlevler Görünümü](../profiling/functions-view-instrumentation-data.md)