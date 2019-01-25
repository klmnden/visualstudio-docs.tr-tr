---
title: 'Nasıl yapılır: Bir profil oluşturma araçları çağrı izleme raporu oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- performance tools, viewing ETW data
- ETW [Visual Studio ALM], viewing data
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
caps.latest.revision: 24
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3669803bd87cbe04117246afad4d5d61866af896
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54774907"
---
# <a name="how-to-create-a-profiling-tools-call-trace-report"></a>Nasıl yapılır: Bir profil oluşturma araçları çağrı izleme raporu oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

*Çağrı izleme raporu* için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları, uygulamanızın işlevlerine her giriş ve çıkış noktası ve işlevinizden diğer işlevlere her çağrı için zamanlama bilgisi listeler. Çağrı izleme raporları, yalnızca cihaz atama yöntemi ile toplandı ise profil oluşturma verisi için kullanılabilir.  
  
> [!NOTE]
>  Çağrı izleme raporları görüntüleyemez [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Kullanmalısınız **VSPerfReport** virgülle ayrılmış değer (.csv) veya Xml dosyası oluşturmak için komut satırı aracı. Bu araç hakkında daha fazla bilgi için bkz. [VSPerfReport](../profiling/vsperfreport.md).  
  
### <a name="to-create-a-call-trace-report"></a>Çağrı izleme raporu oluşturmak için  
  
1.  Açık bir **komut istemi**penceresi.  
  
2.  Komut satırında, aşağıdaki komutu yazın:  
  
     *ToolsPath* **VSPerfReport** *VSPFile* **/calltrace [/ XML]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|Profil Araçları komut satırı araçları yolu. Daha fazla bilgi için [komut satırı araçları yolunu belirtme](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|  
    |*VSPFile*|Profil oluşturma veri (.vsp veya .vsps) dosyası. Tam ve kısmi yollar kabul edilir.|  
    |Xml|Bir Xml biçimli rapor üretir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: İçin Windows (ETW) verilerini izleme olayını Topla](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)   
 [Profil Araçları API'leri](../profiling/profiling-tools-apis.md)
