---
title: 'Nasıl yapılır: Profil oluşturma araçları ETW raporu oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0de5d5560c2e840fd2df7fdc5811c5eea0747da8
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60106507"
---
# <a name="how-to-create-a-profiling-tools-etw-report"></a>Nasıl yapılır: Profil oluşturma araçları ETW raporu oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir performans oturumu içinde kaydedilen ETW olayları için olay izleme Windows (ETW) raporu listeler [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları. ETW verilerini bir ikili (.etl) dosyasında toplanır. Bu rapor hakkında daha fazla bilgi için bkz. [olay izleme için Windows (ETW) raporu](../profiling/event-tracing-for-windows-etw-report.md).  
  
> [!NOTE]
>  Arabirimdeki ETW raporları görüntüleyemez [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
- Arabirimi kullanarak ETW veri toplama hakkında bilgi için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], bkz: [nasıl yapılır: Olay izleme için Windows (ETW) verilerini toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md).  
  
- Bir komut istemi'nden ETW veri toplama hakkında daha fazla bilgi için bkz: [VSPerfCmd](../profiling/vsperfcmd.md) ve [olayları](../profiling/events-vsperfcmd.md).  
  
  Kullanarak ETW raporu oluşturma **VSReport / summary: etw** komutu. ETW verilerini içeren .etl, profil oluşturma veri (.vsp veya .vsps) dosyası olarak aynı dizinde olmalıdır. Varsayılan olarak, bir virgülle ayrılmış değer (.csv) dosyası olarak rapor oluşturulur. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).  
  
### <a name="to-generate-an-etw-report"></a>ETW raporu oluşturmak için  
  
- İçinde bir **komut istemi** penceresinde aşağıdaki komutu yazın:  
  
     *ToolsPath* **VSPerfReport** *VSPFile* **/Summary:ETW [/ XML]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|Profil oluşturma araçları yardımcı program yolu. Daha fazla bilgi için [komut satırı araçları yolunu belirtme](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|  
    |*VSPFile*|Profil oluşturma veri (.vsp veya .vsps) dosyası. Tam ve kısmi yollar kabul edilir.|  
    |Xml|XML'de biçimlendirilmiş bir rapor oluşturur.|
