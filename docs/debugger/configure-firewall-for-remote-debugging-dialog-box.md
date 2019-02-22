---
title: Uzaktan hata ayıklama iletişim kutusu için güvenlik duvarını | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.firewallconfiguration
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- Configure Firewall for Remote Debugging dialog box
- remote debugging, configuring firewalls
- firewalls, configuring for remote debugging
ms.assetid: 5dff3393-fdeb-4129-a2f6-31f653107a82
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 75342630e347eaabe6854498c43294599afae5a5
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56637522"
---
# <a name="configure-firewall-for-remote-debugging-dialog-box"></a>Uzaktan Hata Ayıklama İçin Güvenlik Duvarını Yapılandır İletişim Kutusu
Windows Güvenlik Duvarı, ağ üzerinden bilgi almasını hata ayıklayıcı engellediğinde bu iletişim kutusu görüntülenir. Uzaktan hata ayıklamaya devam etmek için hata ayıklayıcı bilgi alabilir. böylece delik Güvenlik Duvarı'nda açmanız gerekir.

> [!CAUTION]
> Güvenlik Duvarı'nda delik açma makinenize bir güvenlik duvarı tehditleri engellemek için tasarlanmış güvenlik getirebilir. Uzaktan hata ayıklama delik açma 4020 ve Visual Studio 2015'te 4021 bağlantı noktalarını engellemesini kaldırır. Visual Studio'nun diğer sürümlerinde de diğer bağlantı noktası numaralarını kullanılır. Daha fazla bilgi için [uzaktan hata ayıklayıcı bağlantı noktası atamaları](../debugger/remote-debugger-port-assignments.md). Ayrıca, ek bağlantı noktalarını açmak hata ayıklayıcı sağlar. Daha fazla bilgi için [uzaktan hata ayıklama için Windows Güvenlik Duvarı Yapılandırma](../debugger/configure-the-windows-firewall-for-remote-debugging.md).

## <a name="uielement-list"></a>UIElement Listesi
 **Uzaktan hata ayıklama iptal** uzaktan hata ayıklama denemesi iptal eder. Makinenizin güvenlik ayarlarını değişmeden kalır.

 **Yerel ağa (alt ağ) bilgisayarlarda uzaktan hata ayıklamasını engellemesini** yerel alt ağınız makinelerde uzaktan hata ayıklamasını etkinleştirir. Bu güvenlik açıkları, yerel alt ağdaki makinelere açabilir, ancak bilgi alt ağın dışına geldiğini engellemek güvenlik duvarı devam eder.

 **Herhangi bir bilgisayarda uzaktan hata ayıklama engellemesini** ağ herhangi bir yere makinelerde uzaktan hata ayıklamasını etkinleştirir. Bu ayar, en az güvenli seçenektir.

## <a name="see-also"></a>Ayrıca Bkz.

- [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
- [Kullanıcı arabirim başvurusunda hata ayıklama](../debugger/debugging-user-interface-reference.md)