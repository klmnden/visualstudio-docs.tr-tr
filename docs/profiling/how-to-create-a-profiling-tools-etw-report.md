---
title: 'Nasıl yapılır: Profil oluşturma araçları ETW raporu oluşturma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1208080a13c807b95e1a279606568324cab2b8cd
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63439132"
---
# <a name="how-to-create-a-profiling-tools-etw-report"></a>Nasıl yapılır: Profil oluşturma araçları ETW raporu oluşturma
Bir performans oturumu içinde kaydedilen ETW olayları için olay izleme Windows (ETW) raporu listeler [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları. İkili dosyada toplanan ETW veriler (. *etl*) dosyası. Bu rapor hakkında daha fazla bilgi için bkz. [olay izleme için Windows (ETW) raporu](../profiling/event-tracing-for-windows-etw-report.md).

> [!NOTE]
> Arabirimdeki ETW raporları görüntüleyemez [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].

- Arabirimi kullanarak ETW veri toplama hakkında bilgi için [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], bkz: [nasıl yapılır: Olay izleme için Windows (ETW) verileri toplamak](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md).

- Bir komut istemi'nden ETW veri toplama hakkında daha fazla bilgi için bkz: [VSPerfCmd](../profiling/vsperfcmd.md) ve [olayları](../profiling/events-vsperfcmd.md).

  Kullanarak ETW raporu oluşturma **VSReport / summary: etw** komutu. . *etl* ETW içeren veri, profil oluşturma verilerinin ile aynı dizinde olmalıdır (. *Vsp* veya. *vsps*) dosyası. Varsayılan olarak, bir virgülle ayrılmış değer olarak rapor oluşturulur (. *CSV*) dosyası. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).

### <a name="to-generate-an-etw-report"></a>ETW raporu oluşturmak için

- İçinde bir **komut istemi** penceresinde aşağıdaki komutu yazın:

     *ToolsPath* **VSPerfReport** *VSPFile* **/Summary:ETW [/ XML]**

    |||
    |-|-|
    |*ToolsPath*|Profil oluşturma araçları yardımcı program yolu. Daha fazla bilgi için [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|
    |*VSPFile*|Profil oluşturma verilerinin (. *Vsp* veya. *vsps*) dosyası. Tam ve kısmi yollar kabul edilir.|
    |Xml|XML'de biçimlendirilmiş bir rapor oluşturur.|
