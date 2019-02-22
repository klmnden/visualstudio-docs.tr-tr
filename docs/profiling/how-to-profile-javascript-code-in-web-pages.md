---
title: 'Nasıl yapılır: Web sayfalarında JavaScript kod profil | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- JavaScript performance profiling
- Profiling Tools,JavaScript
- web site performance profiling
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3d8e4c2b8b5f557f9f7eff26972593c4f40146be
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56646141"
---
# <a name="how-to-profile-javascript-code-in-web-pages"></a>Nasıl yapılır: Web sayfalarında JavaScript kodu profili

Visual Studio profil oluşturma araçları, yürütülen JavaScript kodu için performans verilerini toplayabilir bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] web uygulaması, bir rastgele web sayfası veya yöntemi profil oluşturma Araçları'nı kullanarak JavaScript uygulaması. Internet Explorer 8 veya sonraki sürümünü gerektirir.

> [!WARNING]
> UWP uygulamalarında JavaScript profili oluşturmak için bkz: [JavaScript belleği](../profiling/javascript-memory.md)

Performans oturumu oluşturmak için profil oluşturma Sihirbazı'nı kullanabilirsiniz. Araçlar yöntemini belirtin ve ardından JavaScript profil oluşturma performans oturumu Özellikleri iletişim kutusunun izleme sayfasındaki seçeneğini belirtin.

JavaScript profil oluşturma belirttiğinizde, her iki JavaScript kodu, yürütür tarayıcıda ve [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] sunucu üzerinde yürütülen kodu profili.

- İçin bir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] web uygulaması, tarayıcıda yürüten iki JavaScript kodunu ve [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] sunucu üzerinde yürütülen kodu profili.

- Rastgele bir web sayfası için tarayıcı içinde yürütülen JavaScript kod profil oluşturulan.

## <a name="to-profile-javascript-in-an-aspnet-web-application-project"></a>Bir ASP.NET web uygulaması projesinde JavaScript profili oluşturmak için

1. Açık [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] Visual Studio'da web projesi.

2. Üzerinde **Çözümle** menüsünü tıklatın **performans Sihirbazını Başlat**.

3. Performans Sihirbazı'nın ilk sayfasında belirttiğiniz **izleme** yöntemi profil oluşturma ve ardından **sonraki**.

4. Sihirbazın ikinci sayfasında, geçerli projenin hedefleri listesinde seçili olduğundan emin olun ve ardından **sonraki.**

5. Sihirbazın üçüncü sayfasında **JavaScript profili** onay kutusunu işaretleyin ve ardından **sonraki**.

6. Sihirbazının dördüncü sayfasında tıklayın **son** tarayıcıda web uygulamasını başlatmak için.

7. Profil oluşturmak istediğiniz işlevi çalıştırın.

8. Profil oluşturma oturumunu sona erdirmek için tarayıcıyı kapatın.

### <a name="to-profile-javascript-in-individual-web-pages-or-a-javascript-applications"></a>Tek tek web sayfalarında JavaScript veya JavaScript uygulamaları profilini çıkarmak için

1. Visual Studio'yu açın.

2. Üzerinde **Çözümle** menüsünü tıklatın **performans Sihirbazını Başlat**.

3. Performans Sihirbazı'nın ilk sayfasında belirttiğiniz **izleme** yöntemi profil oluşturma ve ardından **sonraki**.

4. Bir ASP.NET veya JavaScript uygulama sihirbazının ikinci sayfasında tıklayın ve ardından **sonraki.**

5. Sihirbazın üçüncü sayfasında:

    1. Sayfanın URL'sini yazın **uygulamanız hangi URL'de çalışacak** kutusu.

    2. Seçin **JavaScript profili** onay kutusunu işaretleyin ve ardından **sonraki**.

6. Sihirbazının dördüncü sayfasında tıklayın **son** tarayıcıda web sayfasını başlatmak için.

7. Profil oluşturmak istediğiniz işlevi çalıştırın.

8. Profil oluşturma oturumunu sona erdirmek için tarayıcıyı kapatın.