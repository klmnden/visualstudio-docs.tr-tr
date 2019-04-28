---
title: 'Nasıl yapılır: ClickOnce güvenlik ayarlarını etkinleştirme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- security [Visual Studio], ClickOnce applications
- ClickOnce deployment, security settings
- security settings, ClickOnce deployment
ms.assetid: 73cd3e9d-cd72-4ad2-8cae-94d6bb6b01e0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e52acc18aa18873076df3d02071616c0399b1f33
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63407126"
---
# <a name="how-to-enable-clickonce-security-settings"></a>Nasıl yapılır: ClickOnce güvenlik ayarlarını etkinleştirme
ClickOnce uygulamaları için kod erişimi güvenliği, uygulama yayımlamak için etkinleştirilmesi gerekir. Yayımlama Sihirbazı'nı kullanarak bir uygulama yayımladığınızda, bu otomatik olarak gerçekleştirilir.

 Bazı durumlarda, kod erişim güvenliği etkinleştirme oluşturma veya uygulamanızı hata ayıklama performansı etkileyebilir; Bu durumlarda, güvenlik ayarlarını geçici olarak devre dışı bırakmak isteyebilir.

 ClickOnce güvenlik ayarlarını etkinleştirilebilir veya devre dışı **güvenlik** sayfasının **Proje Tasarımcısı**.

### <a name="to-enable-clickonce-security-settings"></a>ClickOnce güvenlik ayarlarını etkinleştirme

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **güvenlik** sekmesi.

3. Seçin **ClickOnce güvenlik ayarlarını etkinleştirme** onay kutusu.

     Ayrıca, uygulamanızın Güvenlik sayfasında artık güvenlik ayarlarını özelleştirebilirsiniz.

    > [!NOTE]
    > Bu onay kutusu ile uygulamanın yayımlandığı her zaman otomatik olarak seçilen **Yayımla** Sihirbazı.

### <a name="to-disable-clickonce-security-settings"></a>ClickOnce güvenlik ayarlarını devre dışı bırakmak için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **güvenlik** sekmesi.

3. NET **ClickOnce güvenlik ayarlarını etkinleştirme** onay kutusu.

     Uygulama tam güven güvenlik ayarlarıyla çalışır; herhangi bir ayarı **güvenlik** sayfa yok sayılacak.

    > [!NOTE]
    > Uygulama Yayımlama Sihirbazı kullanarak, her yayımlandığında, bu onay kutusu işaretli; yeniden başarılı her yayımlamadan sonra temizlemelisiniz.

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce uygulamalarının güvenliğini sağlama](../deployment/securing-clickonce-applications.md)
- [ClickOnce uygulamaları için kod erişimi güvenliği](../deployment/code-access-security-for-clickonce-applications.md)
