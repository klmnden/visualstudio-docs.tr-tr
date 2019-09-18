---
title: Ağ ya da proxy hatalarını giderme
description: Yüklediğinizde veya Visual Studio'yu bir güvenlik duvarı veya proxy sunucusu arkasında kullanın karşılaşabileceğiniz ağ veya Ara sunucu ile ilgili hatalar için çözüm bulun.
ms.date: 05/22/2019
ms.topic: troubleshooting
helpviewer_keywords:
- network installation, Visual Studio
- administrator guide, Visual Studio
- installing Visual Studio, administrator guide
- list of domains, locations, URLs, Visual Studio
- proxy errors, Visual Studio
ms.assetid: ''
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 7879efca149c31fbe3114b0ddfcba2f2a347f5e6
ms.sourcegitcommit: 2db01751deeee7b2bdb1db25419ea6706e6fcdf8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/17/2019
ms.locfileid: "71062780"
---
# <a name="troubleshoot-network-related-errors-when-you-install-or-use-visual-studio"></a>Visual Studio 'Yu yüklerken veya kullanırken ağla ilgili hatalarda sorun giderme

Yüklediğinizde veya Visual Studio'yu bir güvenlik duvarı veya proxy sunucusu arkasında kullanın karşılaşabileceğiniz en sık karşılaşılan ağ veya Ara sunucu ile ilgili hatalar için çözümleri sorunumuz.

## <a name="error-proxy-authorization-required"></a>Hata: "Proxy yetkilendirmesi gerekiyor"

Bu hata genellikle kullanıcılar bir ara sunucu üzerinden İnternet'e bağlı ve proxy sunucu Visual Studio bazı ağ kaynaklarına yaptığı çağrılar engeller oluşur.

### <a name="to-fix-this-proxy-error"></a>Bu proxy hatayı düzeltmek için

- Visual Studio'yu yeniden başlatın. Bir ara sunucu kimlik doğrulaması iletişim kutusu görünür. İletişim kutusunda istendiğinde kimlik bilgilerinizi girin.

- Visual Studio 'yu yeniden başlatmak sorunu çözmezse, proxy sunucunuz http:&#47;&#47;go.Microsoft.com adreslerinde kimlik bilgilerini istemez ancak. visualStudio.Microsoft.com adresleri için &#42;bunu yapar. Bu sunucular için, Visual Studio 'daki tüm oturum açma senaryolarına engel olmak için aşağıdaki URL 'Leri izin verilenler listesine eklemeyi göz önünde bulundurun:

  - &#42;. windows.net

  - &#42;.microsoftonline.com

  - &#42;. visualstudio.microsoft.com

  - &#42;. microsoft.com

  - &#42;. live.com

- Aksi takdirde, http:&#47;&#47;go.Microsoft.com adresini izin verilenler listesinden kaldırabilirsiniz. böylece, proxy kimlik doğrulama iletişim kutusu, Visual Studio olduğunda her ikisi de&#47;&#47;http: go.Microsoft.com adresi ve sunucu uç noktaları için görüntülenir başladığında.

  -VEYA-

- Ara sunucunuzda varsayılan kimlik bilgilerinizi kullanmak istiyorsanız, aşağıdaki eylemleri gerçekleştirebilirsiniz:

::: moniker range="vs-2017"

  1. Bulma **devenv.exe.config** (devenv.exe yapılandırma dosyası) içindeki: **%ProgramFiles%\Microsoft Visual Studio\2017\Enterprise\Common7\IDE** veya **% ProgramFiles (x86) %\Microsoft Görsel Studio\2017\Enterprise\Common7\IDE**.

  2. Yapılandırma dosyasında bulunamıyor `<system.net>` engelleme ve sonra bu kodu ekleyin:

      ```xml
      <defaultProxy enabled="true" useDefaultCredentials="true">
          <proxy bypassonlocal="True" proxyaddress="http://<yourproxy:port#>"/>
      </defaultProxy>
      ```

      Doğru ara sunucu adresi için ağınızda eklemelisiniz `proxyaddress="<http://<yourproxy:port#>`.

     > [!NOTE]
     > Daha fazla bilgi için [ &lt;defaultProxy&gt; öğesi (ağ ayarları)](/dotnet/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings/) ve [ &lt;proxy&gt; öğesi (ağ ayarları)](/dotnet/framework/configure-apps/file-schema/network/proxy-element-network-settings) sayfalarına bakın.

::: moniker-end

::: moniker range="vs-2019"

  1. : **%ProgramFiles%\Microsoft Visual Studio\2019\Enterprise\Common7\IDE** veya **% ProgramFiles (x86)% \ Microsoft Visual Studio\2019\Enterprise\Common7\IDE**içindeki **devenv. exe. config** (devenv. exe yapılandırma dosyası) bulun.

  2. Yapılandırma dosyasında bulunamıyor `<system.net>` engelleme ve sonra bu kodu ekleyin:

      ```xml
      <defaultProxy enabled="true" useDefaultCredentials="true">
          <proxy bypassonlocal="True" proxyaddress="http://<yourproxy:port#>"/>
      </defaultProxy>
      ```

      Doğru ara sunucu adresi için ağınızda eklemelisiniz `proxyaddress="<http://<yourproxy:port#>`.

     > [!NOTE]
     > Daha fazla bilgi için [ &lt;defaultProxy&gt; öğesi (ağ ayarları)](/dotnet/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings/) ve [ &lt;proxy&gt; öğesi (ağ ayarları)](/dotnet/framework/configure-apps/file-schema/network/proxy-element-network-settings) sayfalarına bakın.

::: moniker-end

## <a name="error-the-underlying-connection-was-closed"></a>Hata: "Temel alınan bağlantı kapatıldı"

Visual Studio, bir güvenlik duvarı özel bir ağda Visual Studio kullanıyorsanız, bazı ağ kaynaklarına bağlanmak mümkün olmayabilir. Azure DevOps Services oturum açma ve lisans, NuGet ve Azure Hizmetleri için bu kaynakları içerebilir. Bu kaynaklar birine bağlanmak Visual Studio başarısız olursa, aşağıdaki hata iletisini görebilirsiniz:

  **Temel alınan bağlantı kapatıldı: Gönderme sırasında beklenmeyen bir hata oluştu**

Visual Studio, ağ kaynaklarına bağlanmak için Aktarım Katmanı Güvenliği (TLS) 1.2 protokolünü kullanır. Visual Studio TLS 1.2 kullandığı durumlarda, bazı özel ağlar üzerindeki güvenlik gereçlerinin bazı sunucu bağlantılarını engelleyin.

### <a name="to-fix-this-connection-error"></a>Bu bağlantı hatayı düzeltmek için

Aşağıdaki URL'ler için bağlantılar sağlar:

- https:&#47;&#47;management.core.windows.net

- https:&#47;&#47;app.vssps.visualstudio.com

- https:&#47;&#47;login.microsoftonline.com

- https:&#47;&#47;login.live.com

- https:&#47;&#47;go.microsoft.com

- https:&#47;&#47;graph.windows.net

- https:&#47;&#47;app.vsspsext.visualstudio.com

- &#42;. azurewebsites.net (Azure bağlantıları için)

- &#42;. visualstudio.microsoft.com

- CDN.vsassets.io (ana içerik teslim ağı veya CDN, içerik)

- &#42;. gallerycdn.vsassets.io (ana Azure DevOps Hizmetleri uzantıları)

- static2.sharepointonline.com (Office UI Fabric Seti'nde yazı tipleri gibi Visual Studio kullanan ana bilgisayar kaynakları)

- &#42;. nuget.org (NuGet bağlantıları için)

  > [!NOTE]
  > Özel NuGet sunucu URL'leri bu listede bulunmayabilir ait. % APPData%\Nuget\NuGet.Config kullanmakta olduğunuz NuGet sunucularını denetleyebilirsiniz.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio’yu bir güvenlik duvarı veya ara sunucusunun arkasına yükleme ve burada kullanma](install-and-use-visual-studio-behind-a-firewall-or-proxy-server.md)
* [Visual Studio Yönetici Kılavuzu](visual-studio-administrator-guide.md)
* [Visual Studio'yu yükleyin](install-visual-studio.md)
