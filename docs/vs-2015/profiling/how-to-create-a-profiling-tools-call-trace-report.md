---
title: 'Nasıl yapılır: profil oluşturma araçları çağrı izleme raporu oluşturma | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- performance tools, viewing ETW data
- ETW [Visual Studio ALM], viewing data
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
caps.latest.revision: 24
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6b3d54c0d9c053b8ea35b6f8000135b259f8323a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49251907"
---
# <a name="how-to-create-a-profiling-tools-call-trace-report"></a>Nasıl yapılır: Profil Oluşturma Araçları Çağrı İzleme Raporu Oluşturma
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
 [Nasıl yapılır: olay izleme için Windows (ETW) verilerini toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)   
 [Profil Araçları API'leri](../profiling/profiling-tools-apis.md)



