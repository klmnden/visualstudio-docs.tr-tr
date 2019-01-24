---
title: 'Hata: Kerberos kimlik doğrulaması başarısız oldu | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.callback_kerberos_auth_failed
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: c18053f9-9074-4bc3-a8bf-13e4acbea921
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: dba1ec7a21c0340db8b89124892edf78db2e04c8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54803319"
---
# <a name="error-kerberos-authentication-failed"></a>Hata: Kerberos kimlik doğrulaması başarısız oldu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uzaktan hata ayıklama yapmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:  
  
```  
Error: The Visual Studio Remote Debugger on the target computer cannot connect back to this computer. Kerberos auythentication failed.  
```  
  
 Visual Studio uzaktan hata ayıklama İzleyicisi yerel sistem veya ağ hizmeti hesabı altında çalışıyorsa, bu hata oluşur. Bu hesaplardan birini altında uzaktan hata ayıklayıcı geri Visual Studio hata ayıklayıcısı ana bilgisayar iletişim kurmak için Kerberos kimlik doğrulaması bağlantı oluşturmanız gerekir.  
  
 Kerberos kimlik doğrulaması, bu koşullar altında kullanılamıyor:  
  
- Hedef bilgisayar ya da hata ayıklayıcısı ana bilgisayar bir etki alanı yerine bir çalışma grubunda değil  
  
   \- veya -  
  
- Etki alanı denetleyicisinde Kerberos devre dışı bırakıldı.  
  
  Kerberos kimlik doğrulaması kullanılabilir durumda değilse, Visual Studio uzaktan hata ayıklama İzleyicisi'ni çalıştırmak için kullanılan hesabı değiştirin. Yordamı için bkz: [hata: Hedef bilgisayardaki Visual Studio uzaktan hata ayıklayıcı hizmeti geriye bu bilgisayara bağlanamıyor](../debugger/error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer.md).  
  
  Her iki bilgisayar aynı etki alanına bağlı ve bu iletiyi almaya devam ediyorsanız, DNS hedef bilgisayarda hata ayıklayıcısı ana bilgisayar adını doğru çözüyor doğrulayın. Aşağıdaki yordama bakın.  
  
### <a name="to-verify-that-dns-on-the-target-computer-is-correctly-resolving-the-debugger-host-computer-name"></a>Hedef bilgisayarda DNS doğru hata ayıklayıcısı ana bilgisayar adı çözdüğünü doğrulamak için  
  
1.  Hedef bilgisayarda açın **Başlat** menüsünde **Donatılar** ve ardından **komut istemi**.  
  
2.  İçinde **komut istemi** penceresinde, tür:  
  
    ```  
    ping <debugger_host_computer_name>  
    ```  
  
3.  İlk satırı `ping` yanıt tam bilgisayar adını ve belirtilen bilgisayar için DNS tarafından döndürülen IP adresini gösterir.  
  
4.  Hata ayıklayıcı ana bilgisayarda açık bir **komut istemi** penceresi ve çalışma `ipconfig`.  
  
5.  IP adresi değerini karşılaştırır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
