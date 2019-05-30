---
title: ACR kayıt defterine ASP.NET Docker kapsayıcısı dağıtma
description: ASP.NET Core web uygulaması bir kapsayıcı kayıt defterine dağıtmak için Visual Studio kapsayıcı araçları kullanmayı öğrenin
author: ghogen
manager: jillfra
ms.assetid: e5e81c5e-dd18-4d5a-a24d-a932036e78b9
ms.devlang: dotnet
ms.topic: conceptual
ms.technology: vs-azure
ms.date: 03/14/2019
ms.author: ghogen
ms.openlocfilehash: 812cddf692ab6cc5676a04dabb88a6e1224c7dcb
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66261044"
---
# <a name="deploy-an-aspnet-container-to-a-container-registry-using-visual-studio"></a>Visual Studio kullanarak kapsayıcı kayıt defterine ASP.NET kapsayıcısı dağıtma

## <a name="overview"></a>Genel Bakış

Docker, bazı açılardan konak uygulamalar ve hizmetler için kullanabileceğiniz bir sanal makineye, benzer bir basit bir kapsayıcı alt yapısıdır.
Bu öğreticide, kapsayıcıya alınmış uygulamanızı yayımlamak için Visual Studio kullanarak açıklanmaktadır bir [Azure Container Registry](https://azure.microsoft.com/services/container-registry).

Azure aboneliğiniz yoksa başlamadan önce [ücretsiz bir hesap](https://azure.microsoft.com/free/dotnet/?utm_source=acr-publish-doc&utm_medium=docs&utm_campaign=docs) oluşturun.

## <a name="prerequisites"></a>Önkoşullar

Bu öğreticiyi tamamlamak için:

::: moniker range="vs-2017"
* En son sürümünü yükleyin [Visual Studio 2017](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download)"ASP.NET ve web geliştirme" iş yüküyle birlikte sağlanır
::: moniker-end
::: moniker range=">=vs-2019"
* En son sürümünü yükleyin [Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) "ASP.NET ve web geliştirme" iş yüküyle birlikte sağlanır
::: moniker-end
* Yükleme [Windows için Docker](https://docs.docker.com/docker-for-windows/install/)

## <a name="create-an-aspnet-core-web-app"></a>Bir ASP.NET Core web uygulaması oluşturma
Aşağıdaki adımlar Bu öğreticide kullanılan temel bir ASP.NET Core uygulaması oluşturmada size yol.

::: moniker range="vs-2017"
[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]
::: moniker-end
::: moniker range=">=vs-2019"
[!INCLUDE [create-aspnet5-app](../azure/includes/vs-2019/create-aspnet5-app-2019.md)]
::: moniker-end

## <a name="publish-your-container-to-azure-container-registry"></a>Kapsayıcınızı Azure Container Registry'ye yayımlama
1. Projenize sağ tıklayın **Çözüm Gezgini** ve **Yayımla**.
2. Yayımlama hedefi iletişim kutusunda seçin **kapsayıcı kayıt defteri** sekmesi.
3. Seçin **yeni Azure Container Registry** tıklatıp **Yayımla**.
4. İstenen değerleri doldurun **yeni bir Azure Container Registry oluşturma**.

    | Ayar      | Önerilen değer  | Açıklama                                |
    | ------------ |  ------- | -------------------------------------------------- |
    | **DNS ön eki** | Genel olarak benzersiz bir ad | Kapsayıcı kayıt defterinizde benzersiz olarak tanımlayan ad. |
    | **Abonelik** | Aboneliğinizi seçin | Kullanılacak Azure aboneliği. |
    | **[Kaynak grubu](/azure/azure-resource-manager/resource-group-overview)** | myResourceGroup |  Kapsayıcı kayıt defterinizde oluşturulacağı kaynak grubunun adı. Seçin **yeni** yeni bir kaynak grubu oluşturmak için.|
    | **[SKU](https://docs.microsoft.com/azure/container-registry/container-registry-skus)** | Standart | Hizmet katmanı kapsayıcı kayıt defterinin  |
    | **Kayıt defteri konumu** | Size yakın bir konum | Bir konumdan seçin bir [bölge](https://azure.microsoft.com/regions/) yakınınızdaki veya kapsayıcı kayıt defterinizi kullanacak diğer hizmetlere yakın. |

    ![Visual Studio'nun iletişim Azure Container Registry oluşturma](media/hosting-web-apps-in-docker/vs-acr-provisioning-dialog.png)

5. **Oluştur**'a tıklayın.

Artık kapsayıcı kayıt defterinden herhangi bir konağa Docker görüntüleri, örneğin çalıştırma yeteneğine çekebilirsiniz [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).
