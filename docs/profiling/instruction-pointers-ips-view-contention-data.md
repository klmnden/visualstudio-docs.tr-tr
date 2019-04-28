---
title: Yönerge işaretçileri (IP) görünümü - çakışma verileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Instruction Pointers view
ms.assetid: f5e49c24-d4cf-4f87-977d-37e3223d1196
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d41f48594e50e9d5ae0c6f67aabab673a9f112a3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62995396"
---
# <a name="instruction-pointers-ips-view---contention-data"></a>Yönerge işaretçileri (IP) görünümü - çakışma verileri
Çekişme verisi IP'ler görünümünü veriler için profil oluşturma çalışmasında çalıştırılması engellenen derleme yönergeleri listeler.

 Yönerge işaretçileri görünümü sütun değerleri aşağıdaki tabloda açıklanmaktadır.

|Sütun|Açıklama|
|------------|-----------------|
|**Dışlamalı engellenme süresi**|Bu işlevdeki engellenme süresi.|
|**Dışlamalı engellenme süresi yüzdesi**|Yönerge yürütülmesi sırasında engellenme süresi yüzdesi.|
|**Dışlamalı Çekişmeler**|Yönerge yürütülmesi sırasında oluşan çekişmelerin sayısı.|
|**Dışlamalı Çekişme yüzdesi**|Yönerge yürütülmesi sırasında oluşan profil oluşturma çalışması içindeki tüm çekişmelerin yüzdesi.|
|**İşlev adresi**|Yüklenen ikili işlevinde başlangıç bellek adresi.|
|**İşlev adı**|Yönergeyi içeren işlev adı.|
|**Yönerge adresi**|Yüklenen ikili yönergesinde bellek adresi.|
|**İşlevin satır numarası**|Satır numarası kaynak dosyada bu işlevin başlangıcı.|
|**Modül adı**|Yönergeyi içeren modül adı.|
|**Modül yolu**|Yönergeyi içeren modül yolu.|
|**İşlem kimliği**|İşlem kimliği (PID) profilli işlemin.|
|**İşlem adı**|İşlemin adı.|
|**Kaynak karakter başlangıcı**|Bu yönerge başladığı kaynak dosya satır öğesindeki taban karakterin uzaklığı.|
|**Kaynak karakter sonu**|Bu yönerge erdiği kaynak dosya satır öğesindeki taban karakterin uzaklığı.|
|**Kaynak dosyası**|Yönergeyi içeren kaynak dosyası.|
|**Kaynak satır başlangıcı**|Bu yönerge başladığı kaynak dosyadaki satır numarası.|
|**Kaynak satır sonu**|Bu yönerge erdiği kaynak dosyadaki satır numarası.|

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Rapor görünümü sütunlarını özelleştirme](../profiling/how-to-customize-report-view-columns.md)
- [Yönerge İşaretçileri (IP) Görünümü](../profiling/instruction-pointers-ips-view.md)
- [Yönerge işaretçileri (IP) görünümü - örnekleme](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)
- [Yönerge İşaretçileri (IP) Görünümü](../profiling/instruction-pointers-ips-view-sampling-data.md)