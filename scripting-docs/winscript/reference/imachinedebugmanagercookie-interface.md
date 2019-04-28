---
title: Imachinedebugmanagercookie arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IMachineDebugManagerCookie interface
ms.assetid: 04770935-3ccf-41e9-b0c1-c78376ab1e3c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fdc02498360f2e3900012166474c5d1e35abd6ee
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977695"
---
# <a name="imachinedebugmanagercookie-interface"></a>IMachineDebugManagerCookie Arabirimi
Benzer şekilde `IMachineDebugManager` arabirimi `IMachineDebugManagerCookie` arabirimi hata ayıklama tanımlama bilgilerini destekler.  
  
 Bu arabirim (ile birlikte `IDebugCookie` arabirimi) hata ayıklayıcı bu komut dosyalarını izlemek, gerek kalmadan bir komut dosyası hata ayıklayıcı işlemi çalıştırmaya betiklere izin vermek.  
  
 Bir komut dosyası hata ayıklayıcı çağırır `IDebugCookie::SetDebugCookie` yöntemi üzerinde işlem hata ayıklama Yöneticisi (PDM). Ardından, PDM yöntemlerini kullanarak bu tanımlama bilgisi eklemek veya kaldırmak için veya gelen Makine Hata Ayıklama Yöneticisi'ni (MDM), bir betik uygulaması için herhangi bir istekle birlikte gönderir `IMachineDebugManagerCookie` arabirimi. MDM sonra her hata ayıklayıcı konusu tanımlama bilgisine sahip dışındaki bir değişikliği bildirir.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IMachineDebugManagerCookie` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IMachineDebugManagerCookie::AddApplication](../../winscript/reference/imachinedebugmanagercookie-addapplication.md)|Çalışan bir uygulama ekler uygulama listesi.|  
|[IMachineDebugManagerCookie::EnumApplications](../../winscript/reference/imachinedebugmanagercookie-enumapplications.md)|Çalışan uygulamalar geçerli listenin bir numaralandırıcı döndürür.|  
|[IMachineDebugManagerCookie::RemoveApplication](../../winscript/reference/imachinedebugmanagercookie-removeapplication.md)|Bir uygulamanın çalışmasını kaldırır uygulama listesi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Imachinedebugmanager arabirimi](../../winscript/reference/imachinedebugmanager-interface.md)   
 [IDebugCookie Arabirimi](../../winscript/reference/idebugcookie-interface.md)