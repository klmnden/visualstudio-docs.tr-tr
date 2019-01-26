---
title: Yönerge işaretçileri (IP) görünümü - .NET bellek örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Instruction Pointers view
ms.assetid: 7d91cc14-e8e9-4ebb-b14f-b9f0da770508
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 295dd3c490495f481ca9568524ee83eb0b1b59be
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54966835"
---
# <a name="instruction-pointers-ips-view---net-memory-sampling-data"></a>Yönerge işaretçileri (IP) görünümü - .NET bellek örnekleme verileri
Örnekleme metodu kullanılarak tarafından toplanan .NET bellek ayırma profil oluşturma verisini IP'ler görünümünü ayrılan bellek profil oluşturma çalışması süresince derleme yönergeleri listeler. Görünümün sütunlarını ayrıca ayırmaların sayısı ve boyutu listeleyin.  
  
 Yalnızca özel değerleri listelenmektedir.  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|  
|**İşlem adı**|İşlemin adı.|  
|**Modül adı**|Yönergeyi içeren modül adı.|  
|**Modül yolu**|Yönergeyi içeren modül yolu.|  
|**Kaynak dosyası**|Yönergeyi içeren kaynak dosyası.|  
|**İşlev adı**|İşlevin adı.|  
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|  
|**İşlev adresi**|İşlev başlangıç adresi.|  
|**Kaynak satır başlangıcı**|Ayırma oluşan kaynak dosyasındaki başlangıç satırı numarası.|  
|**Kaynak satır sonu**|Ayırma oluşan kaynak dosyasındaki bitiş satır sayısı.|  
|**Kaynak karakter başlangıcı**|Ayırma oluşan kaynak dosya satırında başlangıç karakteri uzaklığı.|  
|**Kaynak karakter sonu**|Öğesindeki taban karakterin bitiş ayırma oluşan kaynak dosya satır uzaklığı.|  
|**Yönerge adresi**|Yönerge adresi.|  
|**Dışlamalı ayırmalar**|Yönerge tarafından oluşturulan nesnelerin toplam sayısı.|  
|**Dışlamalı ayırma yüzdesi**|Yönerge tarafından ayrılan profil oluşturma çalışmasında oluşturulan tüm nesneleri yüzdesi.|  
|**Dışlamalı bayt**|Yönerge tarafından ayrılan bellek, profil oluşturma çalışmasında ayrılan bayt sayısı.|  
|**Dışlamalı bayt yüzdesi**|Yönerge tarafından ayrılan tüm profil oluşturma çalışmasında ayrılan belleği bayt yüzdesi.|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Yönerge İşaretçileri (IP) Görünümü](../profiling/instruction-pointers-ips-view-sampling-data.md)