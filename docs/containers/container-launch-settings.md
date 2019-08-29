---
title: Visual Studio kapsayıcı araçları başlatma ayarları
author: ghogen
description: Kapsayıcı araçları derleme işlemine genel bakış
ms.author: ghogen
ms.date: 08/15/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: e039e862040036f3d96729c3bdf48caafe092136
ms.sourcegitcommit: 3cda0d58c5cf1985122b8977b33a171c7359f324
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/29/2019
ms.locfileid: "70158390"
---
# <a name="container-tools-launch-settings"></a>Kapsayıcı araçları başlatma ayarları

ASP.NET Core projesindeki *Özellikler* klasöründe, Web uygulamanızın geliştirme makinenizde nasıl başlatıldığını denetleyen ayarları Içeren launchsettings. json dosyasını bulabilirsiniz. Bu dosyanın ASP.NET geliştirmede nasıl kullanıldığı hakkında ayrıntılı bilgi için bkz. [ASP.NET Core birden çok ortam kullanma](/aspnet/core/fundamentals/environments?view=aspnetcore-2.2). *Launchsettings. JSON*dosyasında **Docker** bölümündeki ayarlar, Visual Studio 'nun Kapsayıcılı uygulamaları nasıl işleyeceği ile ilgilidir.

::: moniker range="vs-2017"
```json
    "Docker": {
      "commandName": "Docker",
      "launchBrowser": true,
      "launchUrl": "{Scheme}://{ServiceHost}:{ServicePort}"
    }
```

::: moniker-end
::: moniker range=">=vs-2019"

```json
    "Docker": {
      "commandName": "Docker",
      "launchBrowser": true,
      "launchUrl": "{Scheme}://{ServiceHost}:{ServicePort}",
      "environmentVariables": {
        "ASPNETCORE_URLS": "https://+:443;http://+:80",
        "ASPNETCORE_HTTPS_PORT": "44360"
      },
      "httpPort": 51803,
      "useSSL": true,
      "sslPort": 44360
    }
```

::: moniker-end

CommandName ayarı, bu bölümün kapsayıcı araçları için geçerli olduğunu tanımlar. Aşağıdaki tabloda, bu bölümde ayarlankullanılabilecek özellikler gösterilmektedir:

::: moniker range="vs-2017"
|Ayar adı|Örnek|Açıklama|
|------------|-------|-------|---------------|
|launchBrowser|Visual Studio 2017|"launchBrowser": true|Projeyi başarıyla başlattıktan sonra tarayıcının başlatılıp başlatılmayacağını belirtir.|
|launchUrl 'Si|Visual Studio 2017|"launchurl": "\<Scheme >://\<ServiceHost >:\<serviceport >"|Bu URL tarayıcı başlatılırken kullanılır.  Bu dize için desteklenen değiştirme belirteçleri şunlardır:<br>   \<Düzen >-SSL 'nin kullanılıp kullanılmadığını bağlı olarak, "http" veya "https" ile değiştirilmiştir.<br>   \<serviceHost >-genellikle "localhost" ile değiştirilmiştir. Windows 10 RS3 veya daha eski sürümlerde Windows kapsayıcıları hedeflenirken, kapsayıcının IP 'si ile değiştirilmiştir.<br>   \<servicePort >-genellikle, SSL 'nin kullanılıp kullanılmadığını bağlı olarak sslPort veya httpPort ile değiştirilmiştir.  Windows 10 RS3 veya daha eski sürümlerde Windows kapsayıcıları hedeflenirken, SSL 'nin kullanılıp kullanıldığına bağlı olarak, "443" veya "80" ile değiştirilmiştir.|
::: moniker-end
::: moniker range=">=vs-2019"
|Ayar adı|Örnek|Açıklama|
|------------|-------|-------|---------------|
|commandLineArgs|"Commanddoğrgs": "--myValue" ayarı|Bu komut satırı bağımsız değişkenleri, projenizi kapsayıcıda başlatırken kullanılır.|
|environmentVariables|"environmentVariables": {<br>    "ASPNETCORE_URLS": "https://+:443; http://+:80",<br>    "ASPNETCORE_HTTPS_PORT": "44381"<br>}|Bu ortam değişkeni değerleri, kapsayıcıda başlatıldığında işleme geçirilir.|
|httpPort|"httpPort": 24051|Bu bağlantı noktası, kapsayıcıyı başlatırken kapsayıcının bağlantı noktası 80 ' e eşlenir.  Belirtilmemişse, değer iisSettings değerinden alınır.|
|launchBrowser|"launchBrowser": true|Projeyi başarıyla başlattıktan sonra tarayıcının başlatılıp başlatılmayacağını belirtir.|
|launchUrl 'Si|"launchurl": "\<Scheme >://\<ServiceHost >:\<serviceport >"|Bu URL tarayıcı başlatılırken kullanılır.  Bu dize için desteklenen değiştirme belirteçleri şunlardır:<br>   \<Düzen >-SSL 'nin kullanılıp kullanılmadığını bağlı olarak, "http" veya "https" ile değiştirilmiştir.<br>   \<serviceHost >-genellikle "localhost" ile değiştirilmiştir. Windows 10 RS3 veya daha eski sürümlerde Windows kapsayıcıları hedeflenirken, kapsayıcının IP 'si ile değiştirilmiştir.<br>   \<servicePort >-genellikle, SSL 'nin kullanılıp kullanılmadığını bağlı olarak sslPort veya httpPort ile değiştirilmiştir.  Windows 10 RS3 veya daha eski sürümlerde Windows kapsayıcıları hedeflenirken, SSL 'nin kullanılıp kullanıldığına bağlı olarak, "443" veya "80" ile değiştirilmiştir.|
|sslPort|"sslPort": 44381|Bu bağlantı noktası, kapsayıcıyı başlatırken kapsayıcının bağlantı noktası 443 ' e eşlenir.  Belirtilmemişse, değer iisSettings değerinden alınır.|
|useSSL|"useSSL": true|Projeyi başlatırken SSL kullanılıp kullanılmayacağını gösterir.  UseSSL belirtilmemişse, sslPort 0 > için SSL kullanılır.
::: moniker-end

## <a name="next-steps"></a>Sonraki adımlar

[Kapsayıcı araçları derleme özelliklerini](container-msbuild-properties.md)ayarlayarak projenizi yapılandırın.

## <a name="see-also"></a>Ayrıca bkz.

[Docker Compose derleme özellikleri](docker-compose-properties.md)
