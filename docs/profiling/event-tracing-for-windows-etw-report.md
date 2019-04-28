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
ms.openlocfilehash: d13a3db996537005c0d4ec67b85c185ac2841cc0
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63447244"
---
# <a name="event-tracing-for-windows-etw-report"></a>Olay izleme için Windows (ETW) raporu
Bir performans oturumu içinde kaydedilen ETW olayları için olay izleme Windows (ETW) raporu listeler [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları. İkili dosyada toplanan ETW veriler (. *etl*) dosyası.

> [!NOTE]
> ETW raporları görüntüleyemez [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] arabirimi.

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