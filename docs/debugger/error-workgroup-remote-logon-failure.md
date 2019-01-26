---
title: 'Hata: Çalışma grubu uzak oturum açma hatası | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.workgroup_remote_logon_failure
dev_langs:
- CSharp
- VB
- FSharp
- JScript
- C++
helpviewer_keywords:
- logon failure, remote debugging
- remote debugging, logon failure
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 16ba1c2fd9b1bd562171a69a846fed4e37352f54
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55030450"
---
# <a name="error-workgroup-remote-logon-failure"></a>Hata: Çalışma grubu uzak oturum açma hatası
Bu hata görünür:  
  
 Oturum açma hatası: Bilinmeyen kullanıcı adı veya hatalı parola  
  
 **Nedeni**  
  
 Bir çalışma grubunda bir makineden hata ayıklama ve uzak makinesine bağlanmaya çalışırsanız, bu hata oluşabilir. Olası nedenler şunlardır:  
  
-   Uzak makinede eşleşen adı ve parola ile hesabı yoktur.  
  
-   Çalışma gruplarında, hem Visual Studio bilgisayarı ve uzak makine varsa, bu hata nedeniyle varsayılan oluşabilir **yerel güvenlik ilkesi** uzak makinede ayarlama. Varsayılan ayarı **yerel güvenlik ilkesi** ayardır **yalnızca konuk - yerel kullanıcı konuk olarak kimlik doğrulaması**. Bu kurulum üzerinde hata ayıklamak için uzak makineye ayarları değiştirme **Klasik - yerel kullanıcıların kendileri olarak kimliklerini**.  
  
> [!NOTE]
>  Aşağıdaki görevleri gerçekleştirmek için yönetici olmanız gerekir.  
  
### <a name="to-open-the-local-security-policy-window"></a>Yerel Güvenlik İlkesi penceresini açmak için  
  
1.  Başlangıç **secpol.msc** Microsoft Yönetim Konsolu ek bileşeni. Windows Search'te Windows Çalıştır kutusuna veya bir komut isteminde secpol.msc yazın.  
  
### <a name="to-add-user-rights-assignments"></a>Kullanıcı hakları ataması eklemek için  
  
1.  Açık **yerel güvenlik ilkesi** penceresi.  
  
2.  Genişletin **yerel ilkeler** klasör.  
  
3.  Tıklayın **kullanıcı hakları ataması**.  
  
4.  İçinde **ilke** sütunu, çift tıklatın **programları için hata ayıklama** geçerli yerel Grup İlkesi atamalarını görüntülemek için **Yerel Güvenlik İlkesi ayarının** iletişim kutusu.  
  
     ![Yerel Güvenlik İlkesi kullanıcı hakları](../debugger/media/dbg_err_localsecuritypolicy_userrightsdebugprograms.png "DBG_ERR_LocalSecurityPolicy_UserRightsDebugPrograms")  
  
5.  Yeni kullanıcı eklemek için tıklatın **kullanıcı veya Grup Ekle** düğmesi.  
  
### <a name="to-change-the-sharing-and-security-model"></a>Paylaşım ve güvenlik modeli değiştirmek için  
  
1.  Açık **yerel güvenlik ilkesi** penceresi.  
  
2.  Genişletin **yerel ilkeler** klasör.  
  
3.  Tıklayın **güvenlik seçenekleri**.  
  
4.  İçinde **ilke** sütunu, çift **ağ erişimi: Yerel hesaplar için paylaşım ve güvenlik modeli**.  
  
5.  İçinde **ağ erişimi: Yerel hesaplar için paylaşım ve güvenlik modeli** iletişim kutusunda, bir değerle değiştirmek **Klasik - yerel kullanıcıların kendileri olarak kimliklerini** tıklatıp **Uygula** düğmesi.  
  
     ![Yerel Güvenlik İlkesi güvenlik seçenekleri](../debugger/media/dbg_err_localsecuritypolicy_securityoptions_networkaccess.png "DBG_ERR_LocalSecurityPolicy_SecurityOptions_NetworkAccess")  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)