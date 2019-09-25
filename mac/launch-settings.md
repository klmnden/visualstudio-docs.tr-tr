---
title: launchSettings. JSON desteği
description: Bu belge Mac için Visual Studio 'de launchSettings. JSON desteğini içerir
author: sayedihashimi
ms.author: sayedha
ms.date: 09/18/2019
ms.assetid: a556f9d7-86a8-408e-aa54-392584845889
ms.openlocfilehash: e7de368dd26bf2724a7bc060dade46422817da1e
ms.sourcegitcommit: ea182703e922c74725045afc251bcebac305068a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71213761"
---
# <a name="launchsettingsjson"></a>launchSettings. JSON

ASP.NET Core projeleri geliştirirken, `launchSettings.json` dosyanın içeriğini özelleştirerek projenizin geliştirme senaryolarında nasıl başlatılacağına ilişkin bir yapılandırma yapabilirsiniz. Mac için Visual Studio, bu dosyayı proje seçenekleri Kullanıcı arabirimini kullanarak veya doğrudan `launchSettings.json` dosyayı düzenleyerek güncelleştirebilirsiniz. Bu dosya, Visual Studio 'Yu Windows üzerinde veya kullanarak `dotnet`komut satırından çalıştırırken kullanılabilecek yapılandırma dosyasıdır. Bu dosya projenizde `Properties` klasörü altında depolanır.

Daha ayrıntılı bilgi için [ASP.NET Core ' de birden çok ortam kullanma](https://docs.microsoft.com/aspnet/core/fundamentals/environments)bölümüne gidebilirsiniz. Bu belgede, Mac için Visual Studio ' de bu dosyayı nasıl güncelleştireceğiz.

## <a name="updating-start-configuration-using-visual-studio-for-mac"></a>Mac için Visual Studio kullanarak başlangıç yapılandırması güncelleştiriliyor

`launchSettings.json` İçinde Mac için Visual Studio doğrudan düzenleyebilir veya proje seçeneklerini kullanarak düzenleyebilirsiniz. Proje seçeneklerine ulaşmak için projenize sağ tıklayın ve Seçenekler ' i seçin. Aşağıdaki görüntüye bakın.

![Proje bağlam menüsü seçenekleri seçildi](media/vsmac-ctx-proj-options.png)

Bu iletişim kutusuna ulaştıktan sonra varsayılan > > yapılandırmasını Çalıştır ' a gidin.

![Varsayılan yapılandırma çalıştırma](media/vsmac-run-config-default.png)

Öncelikle burada yapılandıracaksınız iki şey vardır.

 - Başlangıç olarak ayarlanan ortam değişkenleri
 - Projenin başlangıç URL 'SI

## <a name="configure-environment-variables"></a>Ortam değişkenlerini yapılandırma

Ortam değişkenlerinin değerlerini belirtmek için kılavuzunu kullanabilirsiniz. Bu ortam değişkenleri, uygulamanızı Mac için Visual Studio içinde başlattığınızda ayarlanır. ASP.NET Core uygulamalar geliştirirken, özel `ASPNETCORE_ENVIRONMENT` ortam değişkenini bilmelisiniz. Daha fazla bilgi için bkz. [ASP.NET Core birden çok ortam kullanma](https://docs.microsoft.com/aspnet/core/fundamentals/environments).


## <a name="configure-start-url"></a>Başlangıç URL 'sini Yapılandır

Uygulamanın başlatılacağı URL 'YI yapılandırmak için ASP.NET Core sekmesine gidin.

![PROJ seçenekleri başlangıç URL 'si](media/vsmac-run-config-default-aspnetcore.png)

Burada, uygulamanın başlatıldığında dinleyeceği URL 'leri belirtebilirsiniz.