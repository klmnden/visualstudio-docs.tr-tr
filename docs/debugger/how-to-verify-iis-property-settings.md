---
title: 'Nasıl Yapılır: IIS özellik ayarlarını doğrulama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- IIS, property settings
- debugging Web applications, troubleshooting
- IIS administration tool
- Web applications, setting properties
- properties [debugger], setting with IIS administration tool
ms.assetid: 9efc50bf-02fb-4750-9b3e-f03c38f10d8b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b2bfc72fbae9383b54a31f2252ab60b101903a4e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53926891"
---
# <a name="how-to-verify-iis-property-settings"></a>Nasıl Yapılır: IIS özellik ayarlarını doğrulama

IIS Yönetim Aracı'nı kullanarak bir Web uygulaması için özellikleri ayarlayabilirsiniz. Bu ayarlar doğrulanıyor genellikle sorun giderme gerekli bir adım, bu nedenle bu özellikleri çalıştırmak, uygulama için doğru şekilde ayarlamanız gerekir.

> [!NOTE]
> Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [ayarlarına](../ide/environment-settings.md#reset-settings).

## <a name="to-check-iis-settings-for-the-web-application"></a>IIS Web uygulamasının ayarlarını denetlemek için

1. Açık **Yönetimsel Araçlar** penceresi: Üzerinde **Başlat** menüsünde **programlar**ve ardından **Yönetimsel Araçlar**. Varsa **Yönetimsel Araçlar** görünmez **programlar** menüsü, ardından içinde Ara **Denetim Masası**.

   -   Windows 2000'de seçin **Internet Hizmetleri Yöneticisi'ni**.

   -   Windows XP'de seçin **Internet Information Services**.

   -   Windows Server 2003'te çift **sunucunuzu yönetin**.

        **Sunucunuzu yönetin** penceresi açılır. Altında **uygulama sunucusu**, tıklayın **bu uygulama sunucusunu yönetmek**.

        **Uygulama sunucusu** penceresi açılır. Açık **Internet Information Services (IIS) Yöneticisi'ni** sol bölmedeki düğüm.

2. İletişim kutusunda, ağaç denetimi düğümü makineniz için tıklayın. Tıklayın **Web siteleri** düğümünü ve Web uygulamasının düğümünü seçin. Bir Web sitesi düğümü ve bu nedenle bir eşdüzeyi ya da olacak **varsayılan Web sitesi** düğümü veya bir sanal dizin düğümü altında varolan bir Web sitesi düğümü.

3. Web uygulamasına sağ tıklayın ve kısayol menüsünde **özellikleri**.

4. Web uygulaması için güvenlik ayarlarını doğrulayın:

   1.  Web uygulamasındaki **özellikleri** penceresinde tıklayın **dizin güvenliği** sekmesine ve tıklayın **Düzenle**.

   2.  İçinde **kimlik doğrulama yöntemleri** iletişim kutusunda **anonim erişimi etkinleştir** ve **tümleşik Windows kimlik doğrulaması** henüz seçili değilse.

   3.  Tıklayın **Tamam** kapatmak için **kimlik doğrulama yöntemleri** iletişim kutusu.

5. Bir ATL Sunucu uygulaması için DEBUG fiilini, ISAPI uzantısı ile ilişkili olduğunu doğrulayın. Daha fazla bilgi için [nasıl yapılır: DEBUG fiilini uzantısıyla ilişkilendirin](https://msdn.microsoft.com/library/50d261d3-4bd4-41c0-b44e-3591086f121e).

6. İçin bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] uygulama, uygulama kümesinde bir uygulama adı için sanal klasör emin **Internet Information Services (IIS) Yöneticisi'ni**, **Internet Hizmetleri Yöneticisi'ni** veya  **Internet Information Services**.

   1.  Web uygulamasındaki **özellikleri** penceresinde **dizin** sekmesinde, uygulamayı sanal bir dizinde ise veya **giriş dizini** sekmesinde uygulama ise, bir Web sitesi.

   2.  Doğrulayın adlarında **yerel yol** uygulamanın gerçekten dağıtılacağı dizinin adıyla aynıdır.

   3.  Altında **uygulama ayarları**, uygulamayı içeren kök dizinin adını yazın.

   4.  Tıklayın **Tamam** kapatmak için **özellikleri** iletişim kutusu.

7. İçin bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] uygulama tıklayın **ASP.NET** doğrulayın ve sekme doğru sürümünü [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] belirtilir.

8. Tıklayın **Tamam** kapatmak için **özellikleri** iletişim kutusu.

9. Tıklayın **Tamam** kapatmak için **Internet Information Services (IIS) Yöneticisi'ni**, **Internet Hizmetleri Yöneticisi'ni**, veya **Internet Information Services**iletişim kutusu.

## <a name="see-also"></a>Ayrıca bkz.

- [Sorun giderme](../debugger/debugging-web-applications-troubleshooting.md)