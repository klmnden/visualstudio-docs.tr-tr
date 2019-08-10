---
title: "Nasıl yapılır: Visual Studio 'Nun kilidini aç"
titleSuffix: ''
ms.date: 03/30/2019
ms.topic: conceptual
ms.assetid: ffb580a1-8b5d-48f5-b811-87f8036f50ea
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.openlocfilehash: fe0aa86be242e9a7e7ed8d877944c66247718167
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926299"
---
# <a name="how-to-unlock-visual-studio"></a>Nasıl yapılır: Visual Studio 'Nun kilidini aç

Visual Studio Ücretsiz 30 güne kadar değerlendirebilirsiniz. IDE 'de oturum açmak, deneme süresini 90 güne uzatır. Visual Studio 'Yu kullanmaya devam etmek için IDE 'nin kilidini aşağıdakilerden birini yapın:

- Çevrimiçi abonelik kullanma

- ürün anahtarı girme

## <a name="to-unlock-visual-studio-using-an-online-subscription"></a>Çevrimiçi bir abonelik kullanarak Visual Studio 'Nun kilidini açmak için

Visual Studio aboneliği veya bir Microsoft hesabı veya bir iş veya okul hesabıyla ilişkili bir Azure DevOps organizasyonu kullanarak Visual Studio 'Nun kilidini açmak için:

1. IDE 'nin sağ üst köşesindeki **oturum aç** düğmesini seçin (veya **Dosya** > **hesabı ayarları** ' na giderek **Hesap ayarları** iletişim kutusunu açın ve **oturum aç** düğmesini seçin).

1. Bir Microsoft hesabı ya da bir iş veya Okul hesabı için kimlik bilgilerini girin. Visual Studio, bir Visual Studio aboneliği veya hesabınızla ilişkili bir Azure DevOps organizasyonu bulur.

> [!IMPORTANT]
> **Takım Gezgini** araç penceresinden bir Azure DevOps kuruluşuna bağlandığınızda, Visual Studio ilişkili çevrimiçi abonelikleri otomatik olarak arar. Bir Azure DevOps kuruluşuna bağlandığınızda, hem Microsoft hem de iş veya okul hesaplarını kullanarak oturum açabilirsiniz. Bu kullanıcı hesabı için çevrimiçi bir abonelikle varsa Visual Studio IDE sizin için kilidini otomatik.

## <a name="to-unlock-visual-studio-with-a-product-key"></a>Visual Studio ürün anahtarı kullanarak kilidini açmak için

1. **Hesap ayarları** iletişim kutusunu açmak için **Dosya** > **hesabı ayarları** ' nı seçin ve ardından **bir ürün anahtarı bağlantısı olan lisansı** seçin.

1. Ürün anahtarı, sağlanan alana girin.

> [!TIP]
> Visual Studio 'nun yayın öncesi sürümlerinde ürün anahtarları yoktur. Yayın öncesi sürümleri kullanmak için IDE 'de oturum açmanız gerekir.

## <a name="address-license-problem-states"></a>Adres lisansı sorun durumları

### <a name="update-stale-licenses"></a>Eski lisansları Güncelleştir

Lisansınızın Visual Studio 'da eski olduğunu belirten aşağıdaki iletiyi görmüş olabilirsiniz. "Lisansınız eskiyor ve güncellenmesi gerekiyor" şeklinde okur.

![Visual Studio eski lisans iletisi](../ide/media/vs2017_stale-license.png)

Bu ileti, aboneliğiniz hala geçerli olmaya devam ederken, Visual Studio 'Nun aboneliğinizi güncel tutmak için kullandığı lisans belirtecinin yenilenmesi ve aşağıdaki nedenlerden biri nedeniyle eski bir durum olması gerektiğini belirtir:

- Visual Studio 'Yu kullanmışsınız veya uzun bir süre boyunca internet bağlantısı yoktu.
- Visual Studio dışında oturumunuz.

Lisans belirteci eski olmadan önce, Visual Studio önce kimlik bilgilerinizi yeniden girmeniz isteyen bir uyarı iletisi gösterir.

Kimlik bilgilerinizi yeniden girmeyin, belirteç eskgeç çalışmaya başlar ve **Hesap ayarları** iletişim kutusu, belirtecinizin tam olarak sona ermesi için kaç gün kaldığını söyler. Belirtecin süresi dolduktan sonra, Visual Studio 'Yu kullanmaya devam edebilmeniz için önce hesap kimlik bilgilerinizi yeniden girmeniz gerekir.

> [!Important]
> Sınırlı veya internet erişimi olmayan ortamlarda genişletilmiş dönemler için Visual Studio kullanıyorsanız, kesintiye uğramamak için Visual Studio 'Nun kilidini açmak üzere bir ürün anahtarı kullanmanız gerekir.

### <a name="update-expired-licenses"></a>Vadesi geçen lisansları Güncelleştir

Aboneliğiniz tamamen sona erdiğinde ve Visual Studio için artık erişim haklarınız yoksa, aboneliğinizi yenilemeniz veya aboneliği olan başka bir hesap eklemeniz gerekir. Kullanmakta olduğunuz lisans hakkında daha fazla bilgi görmek için, **Dosya** > **hesabı ayarları** ' na gidin ve iletişim kutusunun sağ tarafındaki lisans bilgilerine bakın. Farklı bir hesapla ilişkili başka bir aboneliğiniz varsa, **Hesap Ekle** bağlantısı ' nı seçerek bu hesabı iletişim kutusunun sol tarafındaki **tüm hesaplar** listesine ekleyin.

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio’da oturum açma](../ide/signing-in-to-visual-studio.md)
