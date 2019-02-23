---
title: 'Hata: Web sunucusu doğru yapılandırılmamış | Microsoft Docs'
ms.date: 09/20/2017
ms.topic: troubleshooting
f1_keywords:
- vs.debug.remote.projnotconfigured
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fc0c61b766b6f93fd1321b15861000d7c628f124
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56711611"
---
# <a name="error-the-web-server-is-not-configured-correctly"></a>Hata: Web sunucusu doğru yapılandırılmamış

Bu sorunu çözmek için burada ayrıntıları verilen adımlar aldıktan sonra ve hata ayıklamak yeniden denemeden önce IIS'yi sıfırlayın gerekebilir. Bir yönetici komut istemi'ni açıp yazarak bunu yapabilirsiniz `iisreset`.

Bu sorunu çözmek için aşağıdaki adımları gerçekleştirin:

1. Sunucu üzerinde barındırılan web uygulaması olarak yapılandırılmışsa, bir yayın yapısı hata ayıklama derlemesi yeniden yayımlamanız ve web.config dosyasını içerdiğini doğrulayın `debug=true` derleme öğesinde. IIS ve yeniden deneme sıfırlayın.

    Örneğin, bir yayın yapısı için bir yayımlama profili kullanıyorsanız, hata ayıklama değiştirin ve yeniden yayımlayın. Aksi takdirde, hata ayıklama özniteliği olarak ayarlanır `false` yayımladığınızda.

2. (IIS) Fiziksel yolun doğru olduğundan emin olun. IIS, bu ayarda bulduğunuz **temel ayarları > fiziksel yolu** (veya **Gelişmiş ayarlar** IIS eski sürümlerinde).

    Web uygulamasını farklı bir makineye kopyaladığınız, el ile yeniden adlandırıldı veya taşındı fiziksel yolu yanlış olabilir. IIS ve yeniden deneme sıfırlayın.

3. Visual Studio'da yerel olarak hata ayıklaması yapıyorsanız doğru sunucu özelliklerinde seçili olduğunu doğrulayın. (Açık **özellikleri > Web > sunucuları** veya **özellikleri > hata ayıklama** proje türüne bağlı olarak. Bir Web formları projesi için açık **özellik sayfaları > Başlat Seçenekleri > sunucu**).

    IIS gibi harici bir (özel) sunucusu kullanıyorsanız, URL'nin doğru olması gerekir. Aksi takdirde, IIS Express ve Yeniden Dene'yi seçin.

4. (IIS) ASP.NET doğru sürümü sunucuda yüklü olduğundan emin olun.

    ASP.NET IIS ve Visual Studio projenize eşleşmeyen sürümleri, bu soruna neden olabilir. Framework sürümü web.config dosyasında ayarlamanız gerekebilir. IIS üzerinde ASP.NET yüklemek için kullanın [Web Platformu Yükleyicisi (Webpı)](https://www.microsoft.com/web/downloads/platform.aspx). Ayrıca bkz [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45) veya ASP.NET Core [IIS ile Windows Konağında](https://docs.asp.net/en/latest/publishing/iis.html).

4. Varsa `maxConnection` IIS sınırı çok düşük ve bağlantı sayısı çok fazla olması, gerekebilir [bağlantı sınırını artırmak](/iis/configuration/system.applicationhost/sites/sitedefaults/limits).

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzak IIS Bilgisayarında Uzaktan ASP.NET ile Hata Ayıklama](../debugger/remote-debugging-aspnet-on-a-remote-iis-7-5-computer.md)
- [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)