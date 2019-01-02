---
title: 'Hata: Güvenlik Duvarı kimlik doğrulaması yok | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.firewall.noauth
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a37fc9c1df938c1cb4817b74d2ebb1d239377823
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53827240"
---
# <a name="error-firewall-no-authentication"></a>Hata: Güvenlik Duvarı kimlik doğrulaması yok
Internet Bağlantısı Güvenlik Duvarı uzak makinede uzaktan hata ayıklamaya izin verecek şekilde ayarlanır değil. İle uzaktan hata ayıklama `No Authentication`, msvsmon.exe özel durumlar listesine eklenmesi gerekir. Bazı IPSec bağlantı noktaları açma de gerekebilir.  
  
> [!NOTE]
>  Uzaktan hata ayıklayıcıyı otomatik olarak Windows Güvenlik Duvarı'nı yapılandırabilirsiniz. Windows Güvenlik Duvarı gibi üçüncü taraf yazılım güvenlik duvarı veya donanım güvenlik duvarı dışında bir güvenlik duvarı kullanırken, uzaktan hata ayıklama izin vermek için güvenlik duvarını el ile yapılandırılması gerekir. Bunu yapmak için msvsmon.exe'nin TCP/IP bağlantı noktalarında trafiğe izin dinlediği. Varsayılan olarak, bu, bağlantı noktası 4018 ve burada 4018 tüm işletim sistemlerinde kullanılır ve 4019 yalnızca Windows üzerinde x64 x86 hata ayıklamaya izin verecek şekilde kullanılan 4019 işlemlerdir.  
  
 Daha fazla bilgi için [uzaktan hata ayıklama](../debugger/remote-debugging.md).