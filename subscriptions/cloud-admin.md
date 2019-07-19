---
title: Bulut abonelikleri için yöneticileri ayarlama | Microsoft Docs
author: evanwindom
ms.author: jaunger
manager: lank
ms.date: 07/17/2019
ms.topic: conceptual
description: Bulut abonelikleri için yöneticileri ayarlama
ms.openlocfilehash: 62a350e6061444e3c75878dfd89739011c4641d5
ms.sourcegitcommit: 57866dd72fd0e15ce61128df70729b427a2d02eb
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2019
ms.locfileid: "68315212"
---
# <a name="set-up-administrators-for-visual-studio-cloud-subscriptions"></a>Visual Studio bulut abonelikleri için yöneticileri ayarlama

Visual Studio bulut abonelikleri yöneticiler tarafından yönetilir. Bu bireyler abonelik atayabilir, atamaları düzenleyebilir, abonelik ekleyebilir veya silebilir ve diğer abonelik yönetim görevlerini gerçekleştirebilir.

## <a name="the-azure-subscription-owner-is-the-first-administrator"></a>Azure abonelik sahibi ilk yöneticiydir

Satın alma işlemleri yapmak için kullanılan Azure aboneliğinin sahibi olarak Visual Studio Cloud abonelikleri satın aldığınızda, bu abonelikler için otomatik olarak bir yönetici olarak ayarlanır.

[Visual Studio Market](https://marketplace.visualstudio.com/subscriptions)aracılığıyla veya bulut çözümü sağlayıcısı ile iletişim kurarak bulut abonelikleri satın alabilirsiniz. Satın alma deneyiminin sonunda Visual Studio Market aracılığıyla satın alırsanız, kullanıcıları yönetmeye yönelik bir fırsat sunulur. Bu seçeneğin belirlenmesi sizi Visual Studio abonelikleri yönetim portalına [https://manage.visualstudio.com](https://manage.visualstudio.com)götürür.

Abonelikleri satın aldıktan sonra istediğiniz zaman [yönetim portalını](https://manage.visualstudio.com) ziyaret edebilirsiniz. Portalda oturum açın ve sol üst ve köşedeki uygun Azure aboneliğini seçin.

Bulut aboneliklerinin satın alınması için kullanılan Azure aboneliğinin sahibi olarak ek yöneticiler de atayabilirsiniz.

## <a name="add-administrators"></a>Yönetici Ekle

Yöneticiler eklemek için:

1. [Portal.Azure.com](https://portal.azure.com)adresinden Azure portalına bağlanın.
2. Visual Studio bulut aboneliklerini satın almak için kullandığınız hesapla oturum açın.
3. Sol gezinti bölmesinde, **maliyet yönetimi + faturalandırma**' e gidin.
4. **Aboneliklerim** listesinde, satın almayı yapmak Için kullandığınız Azure aboneliğini seçin.
5. Sol gezinti bölmesindeki listenin üst kısmına yakın bir konumda bulunan **erişim denetimi**' ne tıklayın.
6. Sayfanın üst kısmındaki **Ekle** sekmesine tıklayın.
7. Tıklayın **rol ataması Ekle**.
8. Sağdaki giriş bölmesinde, bölmenin üst kısmındaki **rol** açılır listesine tıklayın, aşağı kaydırın ve **Kullanıcı erişimi Yöneticisi**' ni seçin.
9. Kullanıcı listesinde, yönetici yapmak istediğiniz kullanıcıya gidin ve bunları seçin. 
10. **Kaydet**'e tıklayın.
11. Seçtiğiniz kullanıcının bir Kullanıcı Erişim Yöneticisi olarak göründüğünü doğrulamak için **rol atamaları** sekmesine tıklayın.

Yeni yönetici artık [yönetim portalında](https://manage.visualstudio.com)oturum açabilir, sayfanın sol üst köşesindeki listeden bulut aboneliklerini satın almak Için kullanılan Azure aboneliğini seçebilir ve bu abonelikleri yönetmeye başlayabilirsiniz.

> [!NOTE]
> Yönetici olarak kurmadığınız bulut aboneliklerinizi düzenlemek için erişimi olan kullanıcılara sahipseniz, bu kullanıcıların, abonelikleri yönetmesine izin veren, temel alınan Azure aboneliğinde rolleri olabilir. Bu roller şunlardır: sahip, katkıda bulunan, hizmet yöneticisi veya ortak yönetici. Daha fazla bilgi için [faturalandırma yöneticileri Ekle](/azure/devops/organizations/billing/add-backup-billing-managers?view=vsts)' ye gidin.

Visual Studio bulut abonelikleri hakkında daha fazla bilgi için, satın alma abonelikleri altındaki [genel bakış](vscloud-overview.md) bölümüne bakın. Visual Studio bulut abonelikleri satın almak için Visual Studio Market [https://marketplace.visualstudio.com/subscriptions](https://marketplace.visualstudio.com/subscription)ziyaret edin.
