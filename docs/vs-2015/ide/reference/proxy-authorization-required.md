---
title: Proxy yetkilendirmesi gerekli | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: troubleshooting
ms.assetid: c2d24ae1-9902-460e-b72a-0299eed9ee82
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 520c31f671aee05663a5471aca05cfe06313b168
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65847029"
---
# <a name="proxy-authorization-required"></a>Proxy kimlik doğrulaması gerekli
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

**Proxy Yetkilendirmesi gerekli** hata genellikle oluşur kullanıcılar Visual Studio online kaynakları bir ara sunucu üzerinden bağlanır ve proxy sunucusu çağrıları engeller.

Bu hatayı düzeltmek için bir veya daha fazla aşağıdaki adımları deneyin:

- Visual Studio'yu yeniden başlatın. Bir ara sunucu kimlik doğrulaması iletişim kutusu görünür. İletişim kutusunda kimlik bilgilerinizi girin.

- Yukarıdaki adım sorunu çözmezse, proxy sunucusu için kimlik bilgileri istenmez Bunun nedeni olabilir http://go.microsoft.com yöneliktir ancak bunu yapar *. visualStudio.com adresleri. Bu sunucular için aşağıdaki URL'ler Visual Studio'da tüm oturum açma senaryoları engelini kaldırmak için izin verilenler listesine eklemeniz gerekir:

    - *.windows.net

    - *.microsoftonline.com

    - *.visualstudio.com

    - *.microsoft.com

    - *.live.com

- Kaldırabilirsiniz http://go.microsoft.com için hem de proxy kimlik doğrulaması iletişim kutusu gösterilir böylece adresi izin verilenler listesinden http://go.microsoft.com adresi ve Visual Studio başlatıldığında sunucu uç noktaları.

- Ara sunucunuzda varsayılan kimlik bilgilerinizi kullanmak istiyorsanız, aşağıdakileri yapın:

   1. Devenv.exe.config (devenv.exe yapılandırma dosyası) bulun: **%ProgramFiles%\Microsoft Visual Studio 14.0\Common7\IDE** (veya **% ProgramFiles (x86) %\Microsoft Visual Studio 14.0\Common7\IDE**) .

   2. Yapılandırma dosyasında bulunamıyor `<system.net>` engelleyin ve bu kodu ekleyin:

      ```xml
      <defaultProxy enabled="true" useDefaultCredentials="true">
          <proxy bypassonlocal="True" proxyaddress=" HYPERLINK "http://<yourproxy:port#" http://<yourproxy:port#>"/>
      </defaultProxy>
      ```

      Doğru ara sunucu adresi için ağınızda Ekle `proxyaddress="<http://<yourproxy:port#>`.

- Bölümündeki yönergeleri [bu blog gönderisini](http://blogs.msdn.com/b/rido/archive/2010/05/06/how-to-connect-to-tfs-through-authenticated-web-proxy.aspx) proxy kullanmak izin veren bir kodu eklemek için.
