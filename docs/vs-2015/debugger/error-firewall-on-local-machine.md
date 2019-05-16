---
title: 'Hata: Yerel makinede güvenlik duvarı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.firewall.localmachine
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: ab60dda9-7934-4891-aa2f-001380d2ed83
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 35ccc65e7aa19c830603d62254385d289a8477ef
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65697411"
---
# <a name="error-firewall-on-local-machine"></a>Hata: Yerel makinede güvenlik duvarı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Internet Bağlantısı Güvenlik Duvarı, Visual Studio çalıştıran makinenin yerel makinede uzaktan hata ayıklamaya izin verecek şekilde ayarlanır değil. Yönetilen veya yerel uzaktan varsayılan aktarım ile hata ayıklama için TCP 135 bağlantı noktası DCOM trafik için açılmalıdır. Dosya ve yazıcı paylaşımı açılması gerekir ve devenv.exe özel durumlar listesine eklenmesi gerekir. Bazı IPSec bağlantı noktaları açma de gerekebilir.  
  
 Daha fazla bilgi için [ayarlanmış yukarı uzak Araçlar cihazda](https://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c).
