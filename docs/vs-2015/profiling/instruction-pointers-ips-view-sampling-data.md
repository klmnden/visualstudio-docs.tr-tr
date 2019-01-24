---
title: Yönerge işaretçileri (IP) görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Instruction Pointers view
ms.assetid: c7f647bb-c5a3-4708-9f9d-33c0fd6e2e96
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b2d4ce3c3a6ba7e49d70b335a85a17a847739962
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758504"
---
# <a name="instruction-pointers-ips-view---sampling-data"></a>Yönerge İşaretçileri (IP) Görünümü- Örnekleme Verileri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Örnekler, profil oluşturma çalışmasında toplanan doğrudan Yürütülüyor derleme yönergeleri için veri listeleri performans verilerini örnekleme IP'ler görünümü.  
  
> [!NOTE]
>  Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. Windows Store apps ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**İşlem kimliği**|İşlem, profil oluşturma çalışması Kimliğine (PID).|  
|**İşlem adı**|İşlemin adı.|  
|**Modül adı**|Yönergeyi içeren modül adı.|  
|**Modül yolu**|Yönergeyi içeren modül yolu.|  
|**Kaynak dosyası**|Yönergeyi içeren kaynak dosyası.|  
|**İşlev adı**|Yönergeyi içeren işlev adı.|  
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|  
|**İşlev adresi**|Yüklenen ikili işlevinde başlangıç bellek adresi.|  
|**Kaynak satır başlangıcı**|Bu örnek, toplanan kaynak dosyadaki başlangıç satır numarası.|  
|**Kaynak satır sonu**|Bitiş satır numarası kaynak dosyada, bu örnek toplanmadı.|  
|**Kaynak karakter başlangıcı**|Bu örnek, toplanan kaynak dosya satırında başlangıç karakteri uzaklığı.|  
|**Kaynak karakter sonu**|Bu örnek, toplanan kaynak dosya satırdaki bitiş karakter uzaklığı.|  
|**Yönerge adresi**|Yüklenen ikili yönerge adresi.|  
|**Dışlamalı örnekler**|Yönerge yürütülürken, toplanan örneklerin toplam sayısı.|  
|**Dışlamalı örnek yüzdesi**|Yönerge yürütülürken, toplanmış olan profil oluşturma, tüm örneklerin yüzdesi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yönerge İşaretçileri (IP) Görünümü- Örnekleme](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)
