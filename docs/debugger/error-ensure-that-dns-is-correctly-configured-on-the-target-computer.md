---
title: 'Hata: DNS hedef bilgisayarda düzgün yapılandırılmış olduğundan emin olun | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.callback_dns_failed
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
ms.openlocfilehash: c538a2b4ff4a50cd89bd9571a8746ccb58aaed04
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62850883"
---
# <a name="error-ensure-that-dns-is-correctly-configured-on-the-target-computer"></a>Hata: DNS hedef bilgisayarda düzgün yapılandırılmış olduğundan emin olun
Uzaktan hata ayıklama yapmaya çalışırken, aşağıdaki hata iletisini alabilirsiniz:

```cmd
Error: The Visual Studio Remote Debugger on the target computer cannot connect back to this computer. Ensure that DNS is correctly configured on the target computer.
```

 Bu ileti, hedef bilgisayar, Visual Studio hata ayıklayıcısı ana bilgisayar adını çözümleyemediğinde oluşur. Hedef bilgisayarda DNS ayarlarını denetleyin.

- Windows 8.1, Vista, Windows 7, Windows Server 2012, Windows Server 2008 veya Windows Server 2008 R2'de, DNS ayarınızı görüntüleme hakkında bilgi için bunu: üzerinde **Başlat** menüsünde seçin **Yardım ve Destek** ve ardından arama **TCP/IP ayarlarını değiştir**.

- Daha fazla bilgi için Git [Microsoft Windows web sitesi](http://go.microsoft.com/fwlink/?LinkId=252720) araması **TCP/IP ayarlarını değiştir**.

  DNS sorununu gideremezseniz, farklı bir hesap altında Uzaktan Hata Ayıklayıcı'yı çalıştırmayı deneyebilirsiniz. Bu hata yalnızca Yerel Sistem veya Ağ Hizmeti hesabı altında Uzaktan Hata Ayıklayıcı'yı çalıştırırken oluşur. Uzaktan Haya Ayıklayıcı'yı başka bir hesap altında çalıştırırsanız, DNS gerektirmeyen NTLM kimlik doğrulaması kullanabilir. biçimindeki telefon numarasıdır. Yordamı için bkz: [hata: Hedef bilgisayardaki Visual Studio uzaktan hata ayıklayıcı hizmeti geriye bu bilgisayara bağlanamıyor](../debugger/error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer.md).
