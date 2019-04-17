---
title: Komut satırından ölçü CPU kullanımı
description: Komut satırından uygulamanızdaki CPU performansına ölçen.
ms.custom: ''
ms.date: 02/19/2019
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools, command-line
- Diagnostics Tools, command-line
- CPU Usage, command-line
author: mikejo5000
ms.author: mikejo
manager: jillfra
monikerRange: '>= vs-2019'
ms.workload:
- multiple
ms.openlocfilehash: 87bf0c236f34e753866ea114dfc7f45e8f16a979
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59670491"
---
# <a name="measure-application-performance-from-the-command-line"></a>Komut satırından ölçü uygulama performansı

Komut satırı araçlarını kullanarak bir uygulama performans bilgilerini toplayabilirsiniz.

Örnekte, bu makalede açıklanan Microsoft Notepad performans bilgilerini toplama, ancak aynı yöntemin herhangi bir işlem profili için kullanılabilir.

## <a name="prerequisites"></a>Önkoşullar

* Visual Studio 2019 Preview 3 veya sonraki sürümler

* Komut satırı araçları konusunda

## <a name="collect-performance-data"></a>Performans verilerini topla

Visual Studio tanılama CLI araçları ile profil oluşturma, bir işlem için profil oluşturma aracı, Toplayıcı aracılarının biriyle birlikte ekleyerek çalışır. Profil oluşturma aracı ekleme, yakalayan bir tanılama oturumu başlatmak ve aracı durduruluncaya kadar profil oluşturma verilerini depoladığı noktada, bu verileri içine aktarılır bir *.diagsession* dosya. Ardından sonuçları analiz etmek için Visual Studio'daki bu dosyayı açabilirsiniz.

1. Not Defteri'ni başlatın ve ardından, işlem Kimliğine (PID) almak için Görev Yöneticisi'ni açın. Görev Yöneticisi'nde PID içinde Bul **ayrıntıları** sekmesi.

1. Bir komut istemi açın ve dizini ile yürütülebilir, toplama aracısı için genellikle burada değiştirin.

   ```<Visual Studio installation folder>\2019\Preview\Team Tools\DiagnosticsHub\Collector\```

1. Başlangıç *VSDiagnostics.exe* aşağıdaki komutu yazarak.

   ```cmd
   VSDiagnostics.exe start <id> /attach:<pid> /loadConfig:<configFile>
   ```

   Dahil edilmesi gereken bağımsız değişkenleri şunlardır:

   * \<*Kimliği*> koleksiyon oturumu tanımlar. Kimliği, 1-255 arasında bir sayı olmalıdır.
   * \<*PID*> işlemin, istediğiniz profili, bu durumda PID 1. adımda bulduğunuz
   * \<*configFile*>, başlatmak istediğiniz koleksiyonu aracısı için yapılandırma dosyası. Daha fazla bilgi için [aracılar için yapılandırma dosyalarını](#config_file).

1. Not Defteri'ni yeniden boyutlandırma veya bazı ilginç profil bilgilerini toplandığı emin olmak için bir şeyler içinde yazın.

1. Koleksiyon oturumu durdurun ve aşağıdaki komutu yazarak çıkışı bir dosyaya göndermek.

   ```cmd
   VSDiagnostics.exe stop <id> /output:<path to file>
   ```

1. Önceki komutta dosya çıkışı gidin ve toplanan bilgileri incelemek için Visual Studio'da açın.

## <a name="config_file"></a> Aracı yapılandırma dosyaları

Toplama aracıları, farklı türde ölçmek çalıştığınız bağlı olarak verileri toplamak birbirinin yerine bileşenlerdir.

Kolaylık olması için bu bilgileri bir aracı yapılandırma dosyasında depolayabilirsiniz. Yapılandırma dosyası bir *.json* en azından adını içeren dosya *.dll* ve onun COM CLSID. Aşağıdaki klasörde bulabilirsiniz örnek yapılandırma dosyaları şunlardır:

```<Visual Studio installation folder>\2019\Preview\Team Tools\DiagnosticsHub\Collector\AgentConfigs\```

* İçin toplanan verilere karşılık gelen CpuUsage yapılandırmaları (temel/yüksek/düşük) [CPU kullanımı](../profiling/cpu-usage.md) aracı profil oluşturma.
* İçin toplanan verilere karşılık gelen DotNetObjectAlloc yapılandırmaları (temel/düşük) [.NET nesne ayırma aracı](https://devblogs.microsoft.com/visualstudio/visual-studio-2017-version-15-8-preview-3/#tooling).

Taban/düşük/yüksek yapılandırmaları için örnekleme oranını bakın. Örneğin, düşük 100 örnek/saniye ve yüksek 4000 örnek/saniye.

İçin *VSDiagnostics.exe* koleksiyon Aracısı ile çalışmak için aracı, uygun aracıyı bir DLL hem bir COM CLSID gerektiriyor ve ek yapılandırma seçeneklerini aracı olabilir. Bir yapılandırma dosyası bir aracı kullanıyorsanız, biçimi aşağıdaki komutu kullanın.

```cmd
VSDiagnostics.exe start <id> /attach:<pid> /loadAgent:<agentCLSID>;<agentName>[;<config>]
```

## <a name="permissions"></a>İzinler

Yükseltilmiş izinler gerektiren bir uygulama profili oluşturmak için yükseltilmiş bir komut isteminden bunu gerekir.
