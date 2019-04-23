---
title: 'Hata: Kerberos kimlik doğrulaması başarısız oldu | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.callback_kerberos_auth_failed
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 76a62a821a9b110be2ffd8e25cbdf6721f12bc08
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60087572"
---
# <a name="error-kerberos-authentication-failed"></a>Hata: Kerberos kimlik doğrulaması başarısız oldu
Uzaktan hata ayıklama yapmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

```cmd
Error: The Visual Studio Remote Debugger on the target computer cannot connect back to this computer. Kerberos authentication failed.
```

 Visual Studio uzaktan hata ayıklama İzleyicisi yerel sistem veya ağ hizmeti hesabı altında çalışıyorsa, bu hata oluşur. Bu hesaplardan birini altında uzaktan hata ayıklayıcı geri Visual Studio hata ayıklayıcısı ana bilgisayar iletişim kurmak için Kerberos kimlik doğrulaması bağlantı oluşturmanız gerekir.

 Kerberos kimlik doğrulaması, bu koşullar altında kullanılamıyor:

- Hedef bilgisayar ya da hata ayıklayıcısı ana bilgisayar bir etki alanı yerine bir çalışma grubunda değil

   \- veya -

- Etki alanı denetleyicisinde Kerberos devre dışı bırakıldı.

  Kerberos kimlik doğrulaması kullanılabilir durumda değilse, Visual Studio uzaktan hata ayıklama İzleyicisi'ni çalıştırmak için kullanılan hesabı değiştirin. Yordamı için bkz: [hata: Hedef bilgisayardaki Visual Studio uzaktan hata ayıklayıcı hizmeti geriye bu bilgisayara bağlanamıyor](../debugger/error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer.md).

  Her iki bilgisayar aynı etki alanına bağlı ve bu iletiyi almaya devam ediyorsanız, DNS hedef bilgisayarda hata ayıklayıcısı ana bilgisayar adını doğru çözüyor doğrulayın. Aşağıdaki yordama bakın.

### <a name="to-verify-that-dns-on-the-target-computer-is-correctly-resolving-the-debugger-host-computer-name"></a>Hedef bilgisayarda DNS doğru hata ayıklayıcısı ana bilgisayar adı çözdüğünü doğrulamak için

1. Hedef bilgisayarda açın **Başlat** menüsünde **Donatılar** ve ardından **komut istemi**.

2. İçinde **komut istemi** penceresinde, tür:

    ```cmd
    ping <debugger_host_computer_name>
    ```

3. İlk satırı `ping` yanıt tam bilgisayar adını ve belirtilen bilgisayar için DNS tarafından döndürülen IP adresini gösterir.

4. Hata ayıklayıcı ana bilgisayarda açık bir **komut istemi** penceresi ve çalışma `ipconfig`.

5. IP adresi değerini karşılaştırır.

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
