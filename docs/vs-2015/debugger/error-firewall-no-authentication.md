---
title: 'Hata: Güvenlik Duvarı kimlik doğrulaması yok | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.firewall.noauth
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: dda1acb8-bed7-4bc8-9991-9cdc49c2ac1e
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: db13165c584399952dc491cf714ac84ee4de7598
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697421"
---
# <a name="error-firewall-no-authentication"></a>Hata: Güvenlik Duvarı kimlik doğrulaması yok
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Internet Bağlantısı Güvenlik Duvarı uzak makinede uzaktan hata ayıklamaya izin verecek şekilde ayarlanır değil. İle uzaktan hata ayıklama `No Authentication`, msvsmon.exe özel durumlar listesine eklenmesi gerekir. Bazı IPSec bağlantı noktaları açma de gerekebilir.  
  
> [!NOTE]
> Uzaktan hata ayıklayıcıyı otomatik olarak Windows Güvenlik Duvarı'nı yapılandırabilirsiniz. Windows Güvenlik Duvarı gibi üçüncü taraf yazılım güvenlik duvarı veya donanım güvenlik duvarı dışında bir güvenlik duvarı kullanırken, uzaktan hata ayıklama izin vermek için güvenlik duvarını el ile yapılandırılması gerekir. Bunu yapmak için msvsmon.exe'nin TCP/IP bağlantı noktalarında trafiğe izin dinlediği. Varsayılan olarak, bu, bağlantı noktası 4018 ve burada 4018 tüm işletim sistemlerinde kullanılır ve 4019 yalnızca Windows üzerinde x64 x86 hata ayıklamaya izin verecek şekilde kullanılan 4019 işlemlerdir.  
  
 Daha fazla bilgi için [ayarlanmış yukarı uzak Araçlar cihazda](https://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c).
