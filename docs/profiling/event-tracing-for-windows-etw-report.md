---
title: Windows (ETW) raporu için olay izleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Event tracing for Windows profiling report
- ETW profiling report
ms.assetid: 81e88162-b88a-40b6-8b85-a232c8096a47
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bf64c2fae940de74978fb2d6c10ce380ed3958d5
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630190"
---
# <a name="event-tracing-for-windows-etw-report"></a>Olay izleme için Windows (ETW) raporu
Bir performans oturumu içinde kaydedilen ETW olayları için olay izleme Windows (ETW) raporu listeler [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları. İkili dosyada toplanan ETW veriler (. *etl*) dosyası.

> [!NOTE]
>  ETW raporları görüntüleyemez [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] arabirimi.

- ETW profil oluşturma araçları kullanarak toplama hakkında bilgi için [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] arabirim için bkz: [nasıl yapılır: Olay izleme için Windows (ETW) verileri toplamak](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md).

- Kullanarak ETW veri toplama hakkında bilgi için [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı araçları görmek [olayları](../profiling/events-vsperfcmd.md).

- Kullanarak ETW raporu oluşturma **VSReport / Summary: ETW** komutu. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).

|Sütun|Açıklama|
|------------|-----------------|
|**Zaman damgası**|Olay gerçekleştiğinde tanımlar.|
|**İşlem kimliği**|Olayı oluşturan bir işlemi tanımlar.|
|**İş parçacığı kimliği**|Olayı oluşturan iş parçacığını tanımlar.|
|**Açıklama**|Olay sağlayıcısı tanımlar.|
|**Tür**|Olay türü tanımlar.|
|**Özellikler**|Olay Özellikleri. Her olay, parantez içine alınmış bir virgülle ayrılmış, ad-değer çiftidir.|