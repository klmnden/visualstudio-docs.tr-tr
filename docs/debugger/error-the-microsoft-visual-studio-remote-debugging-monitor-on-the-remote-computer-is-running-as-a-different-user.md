---
title: 'Hata: Uzak bilgisayardaki Microsoft Visual Studio Uzaktan Hata Ayıklama İzleyicisi farklı kullanıcı olarak çalışıyor'
titleSuffix: ''
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- -anyuser option
- anyuser option
- Remote Debugging Monitor
- remote debugging, Remote Debugging Monitor
- msvsmon.exe
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 513d05149ca52e1d2ec1ca057cca722cef097bd1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55034853"
---
# <a name="error-the-microsoft-visual-studio-remote-debugging-monitor-on-the-remote-computer-is-running-as-a-different-user"></a>Hata: Uzak bilgisayardaki Microsoft Visual Studio Uzaktan Hata Ayıklama İzleyicisi farklı kullanıcı olarak çalışıyor
Uzaktan hata ayıklama yapmaya çalışırken, aşağıdaki hata iletisini alabilirsiniz:  
  
 Microsoft Visual Studio uzaktan hata ayıklama İzleyicisi uzak bilgisayardaki farklı bir kullanıcı olarak çalışıyor.  
  
## <a name="cause"></a>Sebep  
 Bu ileti, kimlik doğrulaması yok modunda hata ayıklama ve msvsmon başlatan kullanıcının Visual Studio çalıştıran kullanıcının olmadığında oluşur.  
  
## <a name="solution"></a>Çözüm  
 Güvenli ve en iyi çözümü uzak bir hata ayıklama İzleyicisi (msvsmon.exe) Visual Studio aynı kullanıcı hesabı altında çalıştırmaktır. Bu işlemi yapamazsınız ile başka bir hesap altında uzaktan hata ayıklama İzleyicisi çalıştırabilirsiniz **tüm kullanıcıların hata ayıklamasına izin** seçeneği uzak hata ayıklama İzleyicisi'nde seçili **seçenekleri** iletişim kutusu.  
  
> [!CAUTION]
>  Diğer kullanıcıların bağlanma izni verme yanlışlıkla yanlış uzaktan hata ayıklama oturumu için bağlanma olanağı sağlar. Hata ayıklama **kimlik doğrulaması yok** modu hiçbir zaman güvendedir ve dikkatli kullanılmalıdır.
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan hata ayıklama ve sorun giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)