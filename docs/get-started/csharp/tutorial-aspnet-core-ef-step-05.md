---
title: "5. Adım: ASP.NET Core uygulamanızı Azure'a dağıtma"
description: Bu videosu ve adım adım yönergeleri, ASP.NET Core Web uygulamanızı Azure'a dağıtın.
ms.custom: get-started
ms.date: 03/31/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
monikerRange: vs-2019
ms.topic: tutorial
ms.devlang: CSharp
author: ardalis
ms.author: tglee
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- aspnet
- dotnetcore
ms.openlocfilehash: 2d995818ec5b8ac01c9776bbf2290da39d2cc40b
ms.sourcegitcommit: b6177ce198c7c5a00030604c9d4faa735405d5df
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59018109"
---
# <a name="step-5-deploy-your-aspnet-core-app-to-azure"></a>5. Adım: ASP.NET Core uygulamanızı Azure'a dağıtma

ASP.NET Core uygulamanızı ve veritabanını Azure'a dağıtmak için aşağıdaki adımları izleyin.

_Bu videoyu izleyin ve ilk ASP.NET Core uygulamanızı Azure'a dağıtmak için ilerleyebilmek._

> [!VIDEO https://www.youtube.com/embed/n8wz_f5_4wI]

## <a name="open-your-project"></a>Projenizi açın

ASP.NET Core uygulamanızı Visual Studio 2019 ' açın. Uygulama zaten kümesi EF Core ile çalışmaya web API'si, yapılandırılan kullanılmalı [Bu öğretici serisinin 4. adım](tutorial-aspnet-core-ef-step-04.md).

## <a name="publish-to-azure-app-service"></a>Azure App Service’e yayımlama

Çözüm Gezgini'nde projeye sağ tıklayın ve seçin **Yayımla**. Varsayılan ayarlarını bırakın **App Service** ve **Yeni Oluştur** tıklatıp **Yayımla** düğmesi. Azure hesabınız yoksa tıklayın **ücretsiz Azure hesabınızı oluşturun** ve kısa kayıt işlemini tamamlayın.

SQL Server ekleyin. Bir yönetici kullanıcı adı ve parola belirtin.

![Visual Studio 2019 Azure SQL sunucusu oluşturma](media/vs-2019/vs2019-azure-sql-server.png)

Application Insights ekleyin.

Tıklayın **Oluştur** devam etmek için düğme.

![Visual Studio 2019 yeni Azure App Service oluşturma](media/vs-2019/vs2019-azure-create-new-app-service.png)

## <a name="exploring-the-azure-portal-and-your-hosted-app"></a>Azure portalı ve barındırılan uygulamanızı keşfetme

App service oluşturulduktan sonra sitenizi bir tarayıcıda başlatılır. Yüklenirken, App Service Azure portalında bulabilirsiniz. Kullanılabilir seçenekler bulabilirsiniz, app service için keşfetmek bir **genel bakış** bölümü, başlatın ve uygulamayı durdurun.

![Azure uygulama hizmeti seçenekleri](media/vs-2019/vs2019-azure-app-service-menu-options.png)

### <a name="scalability"></a>Ölçeklenebilirlik

Uygulama kapatma de olarak ölçeklendirilebilecek şekilde seçenekleri inceleyebilirsiniz. Büyütme, uygulamanızı barındıran her örneği için verilen kaynakların artırılmasını için ifade eder. Ölçek genişletme, uygulamanızı barındıran örneği sayısını artırmak için ifade eder. Otomatik olarak yüklemek için yanıt uygulamanızı barındırmak için kullanılan örnek sayısını artırın ve yük azaldı sonra bunları azaltmak uygulamanız için otomatik ölçeklendirme yapılandırabilirsiniz.

### <a name="security-and-compliance"></a>Güvenlik ve uyumluluk

Uygulamamızı kullanarak Azure barındırma başka bir avantajı, güvenlik ve uyumluluk içindir. Azure App Service, ISO, SOC ve PCI uyumluluğu sağlar. Azure Active Directory veya Twitter, Facebook, Google veya Microsoft gibi sosyal oturum açma ile kullanıcıların kimliğini doğrulamak seçebilirsiniz. Biz IP kısıtlamaları oluşturma, hizmet kimliklerini yönetin, özel etki alanlarını ekleyin ve uygulama için SSL desteği, yapabilir ile geri yüklenebilen arşiv kopyalarını uygulamanın içeriği, yapılandırma ve veritabanı yedeklerini yapılandırın. Bu özellikler, kimlik doğrulamasını erişilen / yetkilendirme, kimlik, yedeklemeleri ve SSL ayarları menü seçenekleri.

### <a name="deployment-slots"></a>Dağıtım yuvaları

Bir uygulamayı dağıttığınızda sık var. küçük bir kapalı kalma süresine uygulamayı yeniden başlatılırken Dağıtım yuvaları, ayrı hazırlama örneği veya örnekleri kümesi dağıtın ve bunlar üretime almadan önce Isınma izin vererek bu sorunu kaçının. Hızlı ve sorunsuz trafiği yeniden yönlendirme yalnızca bir değiştirme var. Takas sonra üretimde herhangi bir sorun varsa, her zaman son, bilinen iyi üretim durumuna geri takas edebilirsiniz.

## <a name="update-connection-string"></a>Bağlantı dizesini güncelleştirme

Varsayılan olarak, yeni bir uygulamanın bağlantısını adlı bir bağlantı dizesini kullanmak için yeni SQL Server veritabanını Azure bekliyor `DefaultConnection`. Daha önce Bu öğretici serisinde oluşturduğumuz uygulama adlı bir bağlantı dizesi şu anda kullandığı `AppDbContext`. Bunu değiştirmek ihtiyacımız *appsettings.json* ve *Startup.cs* ve ardından uygulamayı dağıtın.

## <a name="test-the-app-running-in-azure"></a>Azure'da çalışan uygulamayı test etme

Gidin */oyunları* ve yolu olmalıdır yeni bir oyun ekleyin ve onu listelenen bakın. Ardından, gitmek */swagger* ve yolu olmalıdır uygulamanın API de çalıştığını onaylamak için buradan web API uç noktalarını kullanabilirsiniz.

Tebrikler! Bu video öğretici serisini tamamladınız!

## <a name="next-steps"></a>Sonraki adımlar

Bu ücretsiz kaynaklar ile ASP.NET Core uygulamaları tasarlama hakkında daha fazla bilgi edinin.

[ASP.NET Core uygulaması mimarisi](https://dotnet.microsoft.com/learn/web/aspnet-architecture)

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio ile Azure'a bir ASP.NET Core uygulaması yayımlama](/aspnet/core/tutorials/publish-to-azure-webapp-using-vs?view=aspnetcore-2.2)