---
title: 'Nasıl yapılır: ClickOnce uygulaması için özel izinleri ayarlama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce applications, permissions
- permissions, ClickOnce applications
ms.assetid: 660459ca-ef73-44a8-b323-610001f63b93
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2c8a6fd6625726f749afcf20b80f83178a47ab92
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63407000"
---
# <a name="how-to-set-custom-permissions-for-a-clickonce-application"></a>Nasıl yapılır: ClickOnce uygulaması için özel izinleri ayarlama
Dağıtabileceğiniz bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] Internet veya yerel Intranet bölgeleri için varsayılan izinler kullanan bir uygulama. Alternatif olarak, uygulamanız için gereken belirli izinleri için özel bir bölge oluşturabilirsiniz. Bunu şirket güvenlik izinlerini özelleştirerek yapmak **güvenlik** sayfasının **Proje Tasarımcısı**.

### <a name="to-customize-a-permission"></a>Bir izni özelleştirmek için

1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.

2. Tıklayın **güvenlik** sekmesi.

3. Seçin **ClickOnce güvenlik ayarlarını etkinleştirme** onay kutusu.

4. Seçin **kısmi güven uygulamasıdır** seçenek düğmesini.

     Denetimlerde **ClickOnce güvenlik izinleri** bölüm etkinleştirilir.

5. Gelen **uygulamanızı yükleneceği kaynak bölge** aşağı açılan listesinde, tıklayın **(özel)**.

6. Tıklayın **düzenleme izinleri XML**.

     *App.manifest* dosyasını XML düzenleyicisinde açar.

7. Önce `</applicationRequestMinimum>` öğesi, uygulamanızın gerektirdiği izinler için XML kodunu ekleyin.

    > [!NOTE]
    > Kullanabileceğiniz `ToXml` yöntemi bir izin kümesi XML kodunu uygulama bildirimini oluşturmak için. Örneğin, için XML oluşturmak için <xref:System.Security.Permissions.EnvironmentPermission> izin kümesi, çağrı <xref:System.Security.Permissions.EnvironmentPermission.ToXml%2A> yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce uygulamalarının güvenliğini sağlama](../deployment/securing-clickonce-applications.md)
- [ClickOnce uygulamaları için kod erişimi güvenliği](../deployment/code-access-security-for-clickonce-applications.md)
