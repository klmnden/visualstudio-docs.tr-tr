---
title: ACR kayıt defterine ASP.NET Docker kapsayıcısı dağıtma
description: ASP.NET Core Web uygulamasını bir kapsayıcı kayıt defterine dağıtmak için Visual Studio kapsayıcı araçlarını kullanmayı öğrenin
author: ghogen
manager: jillfra
ms.assetid: e5e81c5e-dd18-4d5a-a24d-a932036e78b9
ms.devlang: dotnet
ms.topic: conceptual
ms.technology: vs-azure
ms.date: 03/14/2019
ms.author: ghogen
ms.openlocfilehash: b3b012bfe3b9fc359a8c9688c52aa5bfc27fd2c7
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70179874"
---
# <a name="deploy-an-aspnet-container-to-a-container-registry-using-visual-studio"></a>Visual Studio kullanarak kapsayıcı kayıt defterine ASP.NET kapsayıcısı dağıtma

## <a name="overview"></a>Genel Bakış

Docker, uygulamaları ve Hizmetleri barındırmak için kullanabileceğiniz bir sanal makineye bazı yollarla benzer bir basit kapsayıcı altyapısıdır.
Bu öğretici, Kapsayıcılı uygulamanızı bir [Azure Container Registry](https://azure.microsoft.com/services/container-registry)yayımlamak Için Visual Studio 'yu kullanma konusunda size kılavuzluk eder.

Azure aboneliğiniz yoksa başlamadan önce [ücretsiz bir hesap](https://azure.microsoft.com/free/dotnet/?utm_source=acr-publish-doc&utm_medium=docs&utm_campaign=docs) oluşturun.

## <a name="prerequisites"></a>Önkoşullar

Bu öğreticiyi tamamlamak için:

::: moniker range="vs-2017"
* "ASP.NET and Web Development" iş yüküne sahip [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download)' in en son sürümünü yükler
::: moniker-end
::: moniker range=">=vs-2019"
* "ASP.NET and Web Development" iş yüküne sahip [Visual Studio 2019](https://visualstudio.microsoft.com/downloads) ' in en son sürümünü yükler
::: moniker-end
* [Docker for Windows](https://docs.docker.com/docker-for-windows/install/) yüklensin

## <a name="create-an-aspnet-core-web-app"></a>ASP.NET Core Web uygulaması oluşturma
Aşağıdaki adımlar, bu öğreticide kullanılacak temel bir ASP.NET Core uygulaması oluştururken size rehberlik eder.

::: moniker range="vs-2017"
[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]
::: moniker-end
::: moniker range=">=vs-2019"
[!INCLUDE [create-aspnet5-app](../azure/includes/vs-2019/create-aspnet5-app-2019.md)]
::: moniker-end

## <a name="publish-your-container-to-azure-container-registry"></a>Kapsayıcınızı Azure Container Registry yayımlayın
1. **Çözüm Gezgini** ' de projenize sağ tıklayın ve **Yayımla**' yı seçin.
2. Hedefi Yayımla iletişim kutusunda **Container Registry** sekmesini seçin.
3. **Yeni Azure Container Registry** seçip **Yayımla**' ya tıklayın.
4. **Yeni Azure Container Registry oluştur ' a**istediğiniz değerleri girin.

    | Ayar      | Önerilen değer  | Açıklama                                |
    | ------------ |  ------- | -------------------------------------------------- |
    | **DNS ön eki** | Genel olarak benzersiz bir ad | Kapsayıcı kayıt defterinizi benzersiz bir şekilde tanımlayan ad. |
    | **Abonelik** | Aboneliğinizi seçin | Kullanılacak Azure aboneliği. |
    | **[Kaynak grubu](/azure/azure-resource-manager/resource-group-overview)** | myResourceGroup |  Kapsayıcı kayıt defterinizin oluşturulacağı kaynak grubunun adı. Yeni bir kaynak grubu oluşturmak için **Yeni** ' yi seçin.|
    | **[ISTEYIN](https://docs.microsoft.com/azure/container-registry/container-registry-skus)** | Standart | Kapsayıcı kayıt defterinin hizmet katmanı  |
    | **Kayıt defteri konumu** | Size yakın bir konum | Size yakın bir [bölgede](https://azure.microsoft.com/regions/) veya kapsayıcı kayıt defterinizi kullanacak diğer hizmetlerin yakınında bir konum seçin. |

    ![Visual Studio 'nun Azure Container Registry oluştur iletişim kutusu](media/hosting-web-apps-in-docker/vs-acr-provisioning-dialog.png)

5. **Oluştur**'a tıklayın.

Artık kapsayıcıyı, kayıt defterinden Docker görüntülerini çalıştırabilen herhangi bir konağa çekebilirsiniz, örneğin [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).
