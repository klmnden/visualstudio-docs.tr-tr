---
title: Yönerge işaretçileri (IP) görünümü - örnekleme verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Instruction Pointers view
ms.assetid: c7f647bb-c5a3-4708-9f9d-33c0fd6e2e96
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 579887c22df16d555c3f309b4326740060aefc1f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63442232"
---
# <a name="instruction-pointers-ips-view---sampling-data"></a>Yönerge işaretçileri (IP) görünümü - örnekleme verileri
Örnekler, profil oluşturma çalışmasında toplanan doğrudan Yürütülüyor derleme yönergeleri için veri listeleri performans verilerini örnekleme IP'ler görünümü.

> [!NOTE]
> Windows 8 ve Windows Server 2012'deki Gelişmiş güvenlik özellikleri Visual Studio profil oluşturucu bu platformlarda veri toplayan bir şekilde önemli değişiklikler gerekmiştir. UWP uygulamaları, ayrıca yeni toplama teknikleri gerektirir. Bkz: [Windows 8 ve Windows Server 2012 uygulamalarında performans araçları](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).

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

## <a name="see-also"></a>Ayrıca bkz.
- [Yönerge işaretçileri (IP) görünümü - örnekleme](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)