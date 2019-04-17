---
title: Yayımlama WebApplicationWebSite (Windows PowerShell Betiği) | Microsoft Docs
description: Bir Azure Web sitesine bir web projesi yayımlamayı öğrenin. Bu betik, mevcut olmaması durumunda Azure aboneliğinizde gerekli kaynakları oluşturur.
author: ghogen
manager: jillfra
assetId: 63cfaa2d-f04d-40dc-8677-345385c278d5
ms.custom: vs-azure
ms.workload: azure-vs
ms.topic: conceptual
ms.date: 11/11/2016
ms.author: ghogen
ms.openlocfilehash: 2e5bd615e83c56a257e093c42fca2a98c5a3efd8
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59649205"
---
# <a name="publish-webapplicationwebsite-windows-powershell-script"></a>Publish-WebApplicationWebSite (Windows PowerShell betiği)
## <a name="syntax"></a>Sözdizimi
Bir Azure Web sitesine bir web projesi yayımlar. Mevcut olmaması durumunda betik, Azure aboneliğinizde gerekli kaynakları oluşturur.

    Publish-WebApplicationWebSite
    –Configuration <configuration>
    -SubscriptionName <subscriptionName>
    -WebDeployPackage <packageName>
    -DatabaseServerPassword @{Name = "name"; Password = "password"}
    -SendHostMessagesToOutput
    -Verbose

## <a name="configuration"></a>Yapılandırma
Dağıtım ayrıntılarını açıklayan JSON yapılandırma dosyası yolu.

| Parametre | Varsayılan değer |
| --- | --- |
| Diğer adlar |yok |
| Gerekli mi? |true |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| Ardışık giriş yapılabilir mi? |false |
| Joker karakterler kabul edilsin mi? |false |

## <a name="subscriptionname"></a>subscriptionName
Web sitesi oluşturmak istediğiniz Azure aboneliğini adı.

| Parametre | Varsayılan değer |
| --- | --- |
| Diğer adlar |yok |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| Ardışık giriş yapılabilir mi? |false |
| Joker karakterler kabul edilsin mi? |false |

## <a name="webdeploypackage"></a>WebDeployPackage
Web sitesine yayımlamak için web dağıtım paketi yolu. Bu paket, Visual Studio'da Web'i Yayımla Sihirbazı'nı kullanarak oluşturabilirsiniz. Daha fazla bilgi için [Azure Cloud Services ve ASP.NET kullanmaya başlama](http://go.microsoft.com/fwlink/p/?LinkID=623089).

| Parametre | Varsayılan değer |
| --- | --- |
| Diğer adlar |yok |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| Ardışık giriş yapılabilir mi? |false |
| Joker karakterler kabul edilsin mi? |false |

## <a name="databaseserverpassword"></a>DatabaseServerPassword
Kullanıcı adı ve Azure SQL veritabanı için parola.

| Parametre | Varsayılan değer |
| --- | --- |
| Diğer adlar |yok |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| Ardışık giriş yapılabilir mi? |false |
| Joker karakterler kabul edilsin mi? |false |

## <a name="sendhostmessagestooutput"></a>SendHostMessagesToOutput
TRUE ise, yazdırma komut dosyasından çıkış akışına iletileri.

| Parametre | Varsayılan değer |
| --- | --- |
| Diğer adlar |yok |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |false |
| Ardışık giriş yapılabilir mi? |false |
| Joker karakterler kabul edilsin mi? |false |

## <a name="remarks"></a>Açıklamalar
Geliştirme ve Test ortamları oluşturmak için komut dosyası kullanmayı tam bir açıklaması için bkz [yayımlamak için geliştirme ve Test ortamları için Windows PowerShell betiklerini kullanarak](vs-azure-tools-publishing-using-powershell-scripts.md).

JSON yapılandırma dosyası, dağıtılacak nedir ayrıntılarını belirtir. Bu Web sitesi için kullanıcı adı ve adı gibi bir proje oluştururken belirttiğiniz bilgileri içerir. Ayrıca veritabanını sağlama, varsa içerir. Aşağıdaki kod, örnek bir JSON yapılandırma dosyası gösterir:

    {
        "environmentSettings": {
            "webSite": {
                "name": "WebApplication10554",
                "location": "West US"
            },
            "databases": [
                {
                    "connectionStringName": "DefaultConnection",
                    "databaseName": "WebApplication10554_db",
                    "serverName": "iss00brc88",
                    "user": "sqluser2",
                    "password": "",
                    "edition": "",
                    "size": "",
                    "collation": "",
                    "location": "West US"
                }
            ]
        }
    }

Ne dağıtılır değiştirmek için JSON yapılandırma dosyasını düzenleyebilirsiniz. Bir Web Bölümü gereklidir, ancak veritabanı bölümü isteğe bağlıdır.

## <a name="next-steps"></a>Sonraki adımlar
Daha fazla bilgi için [Yayımla-WebApplicationVM (Windows PowerShell komut dosyası)](vs-azure-tools-publish-webapplicationvm.md)
