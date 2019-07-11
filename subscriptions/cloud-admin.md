---
title: Bulut abonelikleri yöneticileri ayarlama | Microsoft Docs
author: evanwindom
ms.author: jaunger
manager: evelynp
ms.date: 03/28/2018
ms.topic: conceptual
description: Yöneticiler bulut abonelikleri için ayarlama
ms.openlocfilehash: 2d16dd72e9b3866f8d8608ecae26a5a215d2610b
ms.sourcegitcommit: 208395bc122f8d3dae3f5e5960c42981cc368310
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/10/2019
ms.locfileid: "67783576"
---
# <a name="set-up-administrators-for-visual-studio-cloud-subscriptions"></a>Visual Studio bulut abonelikleri yöneticileri ayarlama

Visual Studio bulut abonelikleri yöneticileri tarafından yönetilir. Bu kişiler abonelikleri atayabilir, atamalarını düzenlemek, eklemek veya abonelikleri Sil ve diğer abonelik yönetim görevlerini gerçekleştirebilirsiniz.

## <a name="the-azure-subscription-owner-is-the-first-administrator"></a>İlk yönetici Azure aboneliğinin sahibi değil

Visual Studio bulut abonelikleri satın alımları gerçekleştirmek için kullanılan Azure aboneliğinin sahibi olarak satın aldığınızda, otomatik olarak bu abonelikler için yönetici olarak ayarlanır.

Bulut abonelikleri aracılığıyla satın aldığınız [Visual Studio Market](https://marketplace.visualstudio.com/subscriptions), veya bir bulut çözümü sağlayıcısı ile iletişim kurarak. Satın alma deneyimi sonunda Visual Studio Market aracılığıyla satın alırsanız, kullanıcıları yönetmek için bir fırsat ile sağlanması. Seçeneği Visual Studio abonelikleri Yönetim Portalı'na - sürer seçme [ https://manage.visualstudio.com ](https://manage.visualstudio.com).

Abonelikleri satın aldığınız sonra ziyaret edebilirsiniz [Yönetim Portalı](https://manage.visualstudio.com) dilediğiniz zaman. Portalda oturum açın ve sol üst ve köşe uygun Azure aboneliğini seçin.

Bulut abonelikleri satın almak için kullanılan Azure aboneliğinin sahibi, ek Yöneticiler atayabilirsiniz.

## <a name="add-administrators"></a>Yöneticiler Ekle

Yöneticiler eklemek için:

1. Adresinden Azure portalında bağlanma [portal.azure.com](https://portal.azure.com).
2. Visual Studio bulut abonelikleri satın almak için kullandığınız hesapla oturum açın.
3. Sol gezinti bölmesinde aşağı kaydırarak **maliyet Yönetimi + faturalandırma**.
4. İçinde **Aboneliklerim** listesinde, satın alma işlemini gerçekleştirmek için kullanılan Azure aboneliğini seçin.
5. Tıklayın **erişim denetimi**, ekranın üst kısmında listenin sol gezinti bölmesinde bulunur.
6. Tıklayın **Ekle** sayfanın üst kısmındaki sekme.
7. Yönetici yapmak istediğiniz abonelik adına çıkış bölmesinde sağ tıklayın.
8. Tıklayarak **rol** açılan bölmesinin üst kısmında, aşağıya inin ve seçin **kullanıcı erişimi Yöneticisi**.
9. **Kaydet**'e tıklayın.

Belirlediğiniz abone sayfasının ortasında görünür ve rollerine "Kullanıcı Erişim Yöneticisi" gösterilir.

Yeni yönetici artık oturum açarak [Yönetim Portalı](https://manage.visualstudio.com)köşe sayfanın sol üst kısımdaki listesinden bulut abonelikleri satın alınması için kullanılan aynı Azure aboneliği seçin ve bunları yönetmeye başlayabilirsiniz Abonelikler.

> [!NOTE]
> Yönetici olarak'kurmak yaramadı bulut aboneliklerinizi düzenlemek için erişimi olan kullanıcılar görürseniz, temel alınan Azure aboneliğinde Aboneliklerini yönetmek izin rolleri sahip olabilir. Bu roller içerir: sahibi, katkıda bulunan, Hizmet Yöneticisi veya ortak yönetici Daha fazla bilgi için ziyaret [faturalama yöneticileri ekleyin](/azure/devops/organizations/billing/add-backup-billing-managers?view=vsts).

Visual Studio bulut abonelikleri hakkında daha fazla bilgi için bkz: [genel bakış](vscloud-overview.md) bulut abonelikleri satın alma altında. Visual Studio bulut abonelikleri satın almak için Visual Studio Market'ten ziyaret [ https://marketplace.visualstudio.com/subscriptions ](https://marketplace.visualstudio.com/subscription).