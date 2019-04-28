---
title: 'Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [ClickOnce], prerequisites
- prerequisites, ClickOnce
- components, bootstrapping
ms.assetid: e964fca5-fdfd-47cf-a1c9-7fb96b1c88b5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 047ac897931cbb93d8a06406e300d39cd83a9fe4
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63406770"
---
# <a name="how-to-install-prerequisites-with-a-clickonce-application"></a>Nasıl yapılır: ClickOnce uygulamasıyla Önkoşulları Yükleme
Tüm [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulamaları gerektirir çalıştırılabilmesi için önce .NET Framework sürümünü doğru bir bilgisayara yüklenir; pek çok uygulama diğer Önkoşullar da sahip. Yayımlama sırasında bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama, bir dizi önkoşul bileşenlerinin yanı sıra müşterilerinizin uygulamanıza paketlenmiş seçebilirsiniz. Yükleme sırasında her önkoşulu zaten mevcut olup olmadığını belirlemek bir denetim gerçekleştirilir. Bu yüklemeden önce değil yüklenecekse [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama.

 Paketleme ve önkoşulları yerine bileşenler için indirme konumu belirtebilirsiniz. Örneğin, yayımladığınız her uygulamasına Önkoşullar dahil olmak üzere yerine, bir merkezi dosya paylaşımı veya tüm önkoşulların için yükleyicileri içeren Web konumu kullanabilirsiniz — yükleme zamanında bileşenler indirilir ve Bu konumdan yüklü.

> [!IMPORTANT]
> İlk yayımlamadan önce önkoşul yükleyicisi paketleri geliştirme bilgisayarınıza eklemelisiniz [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama. Daha fazla bilgi için [nasıl yapılır: ClickOnce uygulamasına Önkoşullar dahil etme](../deployment/how-to-include-prerequisites-with-a-clickonce-application.md).

 Önkoşullar yönetilen **önkoşulları** iletişim kutusu, erişilebilir **Yayımla** bölmesinde **Proje Tasarımcısı**.

> [!NOTE]
> Önceden belirlenmiş Önkoşullar listesine ek olarak kendi bileşenleri listesine ekleyebilirsiniz. Daha fazla bilgi için [önyükleyici paketleri oluşturma](../deployment/creating-bootstrapper-packages.md).

### <a name="to-specify-prerequisites-to-install-with-a-clickonce-application"></a>Yükleme ClickOnce uygulamasıyla önkoşulları belirlemek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünü tıklatın **özellikleri**.

2. Seçin **Yayımla** bölmesi.

3. Tıklayın **önkoşulları** açmak için düğmeyi **önkoşulları** iletişim kutusu.

4. İçinde **önkoşulları** iletişim kutusunda, emin olun **Önkoşul bileşenlerini yüklemek için Kurulum programını Oluştur** onay kutusu seçilidir.

5. İçinde **önkoşulları** listesinde, yükleyin ve ardından istediğiniz bileşenleri seçin **Tamam**.

     Seçili bileşenler paketlenmeli ve yanı sıra müşterilerinizin uygulamanıza yayımlandı.

### <a name="to-specify-a-different-download-location-for-prerequisites"></a>Önkoşullar için farklı indirme konumunu belirtmek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünü tıklatın **özellikleri**.

2. Seçin **Yayımla** bölmesi.

3. Tıklayın **önkoşulları** açmak için düğmeyi **önkoşulları** iletişim kutusu.

4. İçinde **önkoşulları** iletişim kutusunda, emin olun **Önkoşul bileşenlerini yüklemek için Kurulum programını Oluştur** onay kutusu seçilidir.

5. İçinde **Önkoşullar için yükleme konumunu belirtin** bölümünden **aşağıdaki konumdan önkoşulları karşıdan**.

6. Aşağı açılan listeden bir konum seçin veya bir URL, dosya yolunu veya FTP konumu girin ve ardından **Tamam.**

    > [!NOTE]
    > Belirtilen bileşenler için yükleyicileri belirtilen konumda bulunduğundan emin olmanız gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)
- [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)