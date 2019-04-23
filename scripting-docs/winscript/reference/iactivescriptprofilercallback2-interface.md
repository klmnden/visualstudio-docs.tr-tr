---
title: Iactivescriptprofilercallback2 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerCallback2 interface
ms.assetid: 8f2e62e4-c232-4dc3-a2c0-54dd06298306
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3e292dad6c6b633d5f30f263f388d8e85bb6c541
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60115282"
---
# <a name="iactivescriptprofilercallback2-interface"></a>IActiveScriptProfilerCallback2 Arabirimi
Belge nesne modeli (DOM) olaylar meydana geldiğinde bir profil oluşturucu nesnesini bildirmek için komut dosyası altyapısı tarafından kullanılan yöntemleri sağlar. Bu arabirim, profil oluşturucu nesne tarafından uygulanır.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptProfilerCallback2::OnFunctionEnterByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionenterbyname.md)|DOM işlev çağrısı çalıştırmak için komut dosyası altyapısı gidip profil oluşturucu nesne bildirir.|  
|[IActiveScriptProfilerCallback2::OnFunctionExitByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionexitbyname.md)|Profil oluşturucu komut dosyası motoru nesne çalıştıran bir DOM işlev çağrısı tamamlandı bildirir.|  
  
## <a name="remarks"></a>Açıklamalar  
 `IActiveScriptProfilerCallback2` İlk Internet Explorer 9 ile yayımlanan arabirimi.  
  
 DOM çağırıyor olmayan işlev çağrılarının bildirimi tarafından sağlanır [Iactivescriptprofilercallback arabirimi](../../winscript/reference/iactivescriptprofilercallback-interface.md).  
  
> [!NOTE]
>  Bir komut dosyası çalıştırılırken profil oluşturmayı durdurmak ve başlatmak özelliği eklemek için aşağıdaki yöntemleri çağırın. Bu yöntemleri kullanarak, tam çağrı yığınını edinebilirsiniz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] başlattığınızda veya profil oluşturmayı durdurmak çalışıyor.  
> 
> - Çağrı [IActiveScriptProfilerControl2::CompleteProfilerStart](../../winscript/reference/iactivescriptprofilercontrol2-completeprofilerstart.md) profil oluşturma başlatıldı profil oluşturucu bildirir.  
>   - Çağrı [IActiveScriptProfilerControl2::PrepareProfilerStop](../../winscript/reference/iactivescriptprofilercontrol2-prepareprofilerstop.md) , kısa süre içinde profil oluşturmayı durdurur, profil oluşturucu bildirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Profil Oluşturucu Arabirimleri](../../winscript/reference/active-script-profiler-interfaces.md)