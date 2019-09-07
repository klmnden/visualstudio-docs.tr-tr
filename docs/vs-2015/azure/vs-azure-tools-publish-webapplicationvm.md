---
title: Publish-WebApplicationVM | Microsoft Docs
description: Bir Web uygulamasını bir sanal makineye dağıtmayı öğrenin. Bu betik, mevcut değilse, Azure aboneliğinizde gerekli kaynakları oluşturur.
author: ghogen
manager: jillfra
assetId: de4cec95-f73f-44d9-babd-9f47f2633cdb
ms.prod: visual-studio-dev14
ms.technology: vs-azure
ms.custom: vs-azure
ms.workload: azure-vs
ms.topic: conceptual
ms.date: 11/11/2016
ms.author: ghogen
ms.openlocfilehash: e35f5decee2a908a9d1075ff3f6365a1d358c7b2
ms.sourcegitcommit: dae5dfd626277b58ebd7b21a75757f683f1eacc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "70739318"
---
# <a name="publish-webapplicationvm-windows-powershell-script"></a>Publish-WebApplicationVM (Windows PowerShell betiği)
Bir sanal makineye bir Web uygulaması dağıtır. Komut dosyası, mevcut değilse, Azure aboneliğinizde gerekli kaynakları oluşturur.

```
Publish-WebApplicationVM
–Configuration <configuration>
-SubscriptionName <subscriptionName>
-WebDeployPackage <packageName>
-VMPassword @{Name = "name"; Password = "password")
-DatabaseServerPassword @{Name = "name"; Password = "password"}
-SendHostMessagesToOutput
-Verbose
```

### <a name="configuration"></a>Yapılandırma
Dağıtımın ayrıntılarını açıklayan JSON yapılandırma dosyasının yolu.

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |true |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

### <a name="subscriptionname"></a>SubscriptionName
Sanal makineyi oluşturmak istediğiniz Azure aboneliğinin adı.

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |Abonelik dosyasındaki ilk aboneliği kullanır |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

### <a name="webdeploypackage"></a>WebDeployPackage
Sanal makinede yayımlanacak Web dağıtım paketinin yolu. Bu paketi Visual Studio 'daki Web 'i Yayımla Sihirbazı 'nı kullanarak oluşturabilirsiniz. Bkz [. nasıl yapılır: Visual Studio](https://msdn.microsoft.com/library/dd465323.aspx)'Da bir Web dağıtım paketi oluşturun.

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

### <a name="allowuntrusted"></a>Allowgüvenilmeyen
Doğru ise, güvenilen kök yetkili tarafından imzalanmamış sertifikaların kullanılmasına izin verin.

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |false |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

### <a name="vmpassword"></a>VMPassword
Sanal makine hesabının kimlik bilgileri. Örnek:-VMPassword @ {Name = "admin"; Password = "parola"}

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

### <a name="databaseserverpassword"></a>DatabaseServerPassword
Azure 'da SQL veritabanı için kimlik bilgileri. Örnek:-DatabaseServerPassword @ {Name = "admin"; Password = "parola"}

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |yok |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

### <a name="sendhostmessagestooutput"></a>Sendhostiletitooutput
Doğru ise, komut dosyasından çıkış akışına iletileri yazdırın.

| Diğer adlar | yok |
| --- | --- |
| Gerekli mi? |false |
| Konum |adlandırılmış |
| Varsayılan değer |false |
| İşlem hattı girişi kabul edilsin mi? |false |
| Joker karakterler kabul edilsin mi? |false |

## <a name="remarks"></a>Açıklamalar
Geliştirme ve test ortamları oluşturmak için betiğin nasıl kullanılacağına ilişkin ayrıntılı bir açıklama için, bkz. [geliştirme ve test ortamlarında yayımlamak Için Windows PowerShell betiklerini kullanma](vs-azure-tools-publishing-using-powershell-scripts.md).

JSON yapılandırma dosyası, dağıtılması gereken ayrıntıları belirtir. Projeyi oluştururken belirttiğiniz bilgileri içerir (örneğin ad, benzeşim grubu, VHD görüntüsü ve sanal makinenin boyutu). Ayrıca sanal makinedeki uç noktaları, sağlama yapılacak veritabanlarını ve Web Dağıtım parametrelerini de içerir. Aşağıdaki kod örnek bir JSON yapılandırma dosyasını göstermektedir:

```
{
    "environmentSettings": {
        "cloudService": {
            "name": "myvmname",
            "affinityGroup": "",
            "location": "West US",
            "virtualNetwork": "",
            "subnet": "",
            "availabilitySet": "",
            "virtualMachine": {
                "name": "myvmname",
                "vhdImage": "a699494373c04fc0bc8f2bb1389d6106__Windows-Server-2012-R2-201404.01-en.us-127GB.vhd",
                "size": "Small",
                "user": "vmuser1",
                "password": "",
                "enableWebDeployExtension": true,
                "endpoints": [
                    {
                        "name": "Http",
                        "protocol": "TCP",
                        "publicPort": "80",
                        "privatePort": "80"
                    },
                    {
                        "name": "Https",
                        "protocol": "TCP",
                        "publicPort": "443",
                        "privatePort": "443"
                    },
                    {
                        "name": "WebDeploy",
                        "protocol": "TCP",
                        "publicPort": "8172",
                        "privatePort": "8172"
                    },
                    {
                        "name": "Remote Desktop",
                        "protocol": "TCP",
                        "publicPort": "3389",
                        "privatePort": "3389"
                    },
                    {
                        "name": "Powershell",
                        "protocol": "TCP",
                        "publicPort": "5986",
                        "privatePort": "5986"
                    }
                ]
            }
        },
        "databases": [
            {
                "connectionStringName": "",
                "databaseName": "",
                "serverName": "",
                "user": "",
                "password": ""
            }
        ],
        "webDeployParameters": {
            "iisWebApplicationName": "Default Web Site"
        }
    }
}
```

Sağlanan öğeleri değiştirmek için JSON yapılandırma dosyasını düzenleyebilirsiniz. Bir sanal makine ve bulut hizmeti gereklidir, ancak veritabanı bölümü isteğe bağlıdır.
