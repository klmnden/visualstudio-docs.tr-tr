---
title: Bir çalışan işlemi bir kullanıcı hesabı altında Çalıştır | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- user accounts, aspnet_wp.exe
- ASP.NET, debugging Web applications
- tools, aspnet_wp.exe
- ASP.NET, tools
- aspnet_wp.exe
ms.assetid: b58e97b1-e62a-4318-aea4-52276ea20735
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aebe1faf31d53fb44cf5efddbee154018e42a365
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62847777"
---
# <a name="how-to-run-the-worker-process-under-a-user-account"></a>Nasıl yapılır: Bir kullanıcı hesabı altında çalışan işlemini çalıştırma
Bilgisayarınızı çalıştırabileceğiniz şekilde ayarlamak için [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] bir kullanıcı hesabı altında çalışan işlemi (aspnet_wp.exe veya w3wp.exe) aşağıdaki adımları izleyin.

 > [!IMPORTANT]
 > Windows Server 2008 R2 ile başlayarak, kullanılmasını öneririz [ApplicationPoolIdentity](/iis/manage/configuring-security/application-pool-identities) her uygulama havuzunun kimliği olarak.

## <a name="procedure"></a>Yordam

#### <a name="to-run-aspnetwpexe-under-a-user-account"></a>Bir kullanıcı hesabı altında Aspnet_wp.exe çalıştırmak için

1. Çalışma zamanı yüklü olduğu yolu altında CONFIG klasöründeki bilgisayarınızda bulunan machine.config dosyasını açın.

2. Bulma &lt;processModel&gt; bölümünde ve adına ve parola kullanıcı hesabının altında çalıştırılacak aspnet_wp.exe istediğiniz kullanıcı adı ve parola özniteliklerini değiştirebilirsiniz.

3. Machine.config dosyasına kaydedin.

4. Üzerinde [!INCLUDE[winxpsvr](../debugger/includes/winxpsvr_md.md)], IIS 6.0, varsayılan olarak yüklenir. Çalışan işlemi olarak aspnet_wp.exe ile IIS 6.0 modunda çalıştırılması w3wp.exe.To ilgili çalışan işlemi, şu adımları uygulamanız gerekir:

   1. Tıklayın **Başlat**, tıklayın **Yönetimsel Araçlar** seçip **Internet Information Services**.

   2. İçinde **Internet Information Services** iletişim kutusu, sağ **Web siteleri** klasörü seçin **özellikleri**.

   3. İçinde **Web siteleri özellikleri** iletişim kutusunda **hizmet**.

   4. Seçin **IIS6.0 yalıtım modunda çalıştır WWW hizmetini**.

   5. Kapat **özellikleri** iletişim kutusu ve **Internet Hizmetleri Yöneticisi'ni**.

5. Bir Windows komut istemi açın ve sunucu çalıştırarak sıfırlayın:

   ```cmd
   iisreset
   ```

   — veya —

   ```cmd
   net stop iisadmin /y
   net start w3svc
   ```

6. Geçici bulun [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] CONFIG klasörü aynı yol olması gereken dosyalar klasörü. Geçici sağ [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] seçin ve dosyalar klasörü **özellikleri** kısayol menüsünde.

7. İçinde **geçici ASP.NET dosyaları özellikleri** iletişim kutusu, tıklayın **güvenlik** sekmesi.

8. **Gelişmiş**'e tıklayın.

9. İçinde **ASP.Net dosyaları için Gelişmiş güvenlik ayarları** iletişim kutusu, tıklayın **Ekle**.

    **Kullanıcı seç, bilgisayar veya Grup iletişim kutusunda** görünür.

10. Kullanıcı adını yazın **Seçilecek nesne adını girin** kutusuna ve ardından **Tamam**. Kullanıcı adı şu biçimde olmalıdır: DomainName\UserName.

11. İçinde **ASP.NET dosyaları için izin girdisi** iletişim kutusunda, kullanıcıya vermek **tam denetim**ve ardından **Tamam** kapatmak için **geçici ASP için giriş .NET dosyaları** iletişim kutusu.

12. A **güvenlik** iletişim kutusu görünür ve sizin gerçekten bir sistem klasörü izinleri değiştirmek isteyip istemediğinizi sorar. **Evet**'i tıklayın.

13. Tıklayın **Tamam** kapatmak için **geçici ASP.NET dosyaları özellikleri** iletişim kutusu.

## <a name="see-also"></a>Ayrıca Bkz.
- [ASP.NET uygulamalarında hata ayıklama](../debugger/how-to-enable-debugging-for-aspnet-applications.md)
- [ASP.NET hata ayıklaması: Sistem gereksinimleri](../debugger/aspnet-debugging-system-requirements.md)
