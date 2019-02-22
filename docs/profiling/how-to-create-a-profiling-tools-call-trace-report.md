---
title: 'Nasıl yapılır: Bir profil oluşturma araçları çağrı izleme raporu oluşturma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, viewing ETW data
- ETW [Visual Studio ALM], viewing data
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cdfe600192e61e8e7721c0e5486afafbedcaa6eb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56624223"
---
# <a name="how-to-create-a-profiling-tools-call-trace-report"></a>Nasıl yapılır: Profil oluşturma araçları çağrı izleme raporu oluşturma
*Çağrı izleme raporu* için [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları, uygulamanızın işlevlerine her giriş ve çıkış noktası ve işlevinizden diğer işlevlere her çağrı için zamanlama bilgisi listeler. Çağrı izleme raporları, yalnızca cihaz atama yöntemi ile toplandı ise profil oluşturma verisi için kullanılabilir.

> [!NOTE]
>  Çağrı izleme raporları görüntüleyemez [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Kullanmalısınız **VSPerfReport** virgülle ayrılmış bir değer oluşturmak için komut satırı aracını (. *CSV*) veya. *xml* dosya. Bu araç hakkında daha fazla bilgi için bkz. [VSPerfReport](../profiling/vsperfreport.md).

### <a name="to-create-a-call-trace-report"></a>Çağrı izleme raporu oluşturmak için

1.  Açık bir **komut istemi** penceresi.

2.  Komut satırında, aşağıdaki komutu yazın:

     *ToolsPath* **VSPerfReport** *VSPFile* **/calltrace [/ XML]**

    |||
    |-|-|
    |*ToolsPath*|Profil Araçları komut satırı araçları yolu. Daha fazla bilgi için [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|
    |*VSPFile*|Profil oluşturma verilerinin (. *Vsp* veya. *vsps*) dosyası. Tam ve kısmi yollar kabul edilir.|
    |Xml|Bir XML biçimli rapor üretir.|


## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Olay izleme için Windows (ETW) verileri toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)
- [Profil Araçları API'leri](../profiling/profiling-tools-apis.md)
