---
title: Iactivescriptprofilercallback arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 76f9164b-b086-4b29-ac79-76f9c76f1d11
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a0eb8ef209e1fc55fabf37c0c4469fd390f5a478
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146337"
---
# <a name="iactivescriptprofilercallback-interface"></a>IActiveScriptProfilerCallback Arabirimi
Komut dosyası altyapısı tarafından olaylar meydana geldiğinde bir profil oluşturucu nesnesini bildirmek için kullanılan yöntemleri sağlar. Bu arabirim, profil oluşturucu nesne tarafından uygulanır.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptProfilerCallback::Initialize](../../winscript/reference/iactivescriptprofilercallback-initialize.md)|Bir komut dosyası altyapısına profil oluşturma başlatıldığında, profil oluşturucu nesnesini başlatmak üzere çağrılır.|  
|[IActiveScriptProfilerCallback::Shutdown](../../winscript/reference/iactivescriptprofilercallback-shutdown.md)|Ücretsiz ve profil oluşturma, bir komut dosyası altyapısına durdurulur zaman profil oluşturucu nesnesini serbest bırakmak için çağrılır.|  
|[IActiveScriptProfilerCallback::ScriptCompiled](../../winscript/reference/iactivescriptprofilercallback-scriptcompiled.md)|Komut dosyası motoru nesne derlenmiş komut dosyası profil oluşturucu bildirir.|  
|[IActiveScriptProfilerCallback::FunctionCompiled](../../winscript/reference/iactivescriptprofilercallback-functioncompiled.md)|Profil oluşturucu komut dosyası motoru nesne bir komut dosyası derlenirken bir işlevle karşılaştığında bildirir.|  
|[IActiveScriptProfilerCallback::OnFunctionEnter](../../winscript/reference/iactivescriptprofilercallback-onfunctionenter.md)|Komut dosyası altyapısı hakkında belge nesne modeli (DOM) içine çağrı değil bir işlev çağrısı yürütmek için profil oluşturucu nesnesini bildirir.|  
|[IActiveScriptProfilerCallback::OnFunctionExit](../../winscript/reference/iactivescriptprofilercallback-onfunctionexit.md)|Profil Oluşturucu bir işlev yürütülürken tamamlanmış komut dosyası altyapısı çağrı, nesne yerli çağrısını değil bildirir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Belge nesne modeli (DOM) içine işlev çağrılarının bildirimi tarafından sağlanır [Iactivescriptprofilercallback2 arabirimi](../../winscript/reference/iactivescriptprofilercallback2-interface.md).  
  
> [!NOTE]
>  Bir komut dosyası çalıştırılırken profil oluşturmayı durdurmak ve başlatmak özelliği eklemek için aşağıdaki yöntemleri çağırın. Bu yöntemleri kullanarak, tam çağrı yığınını edinebilirsiniz [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] başlattığınızda veya profil oluşturmayı durdurmak çalışıyor.  
> 
> - Çağrı [IActiveScriptProfilerControl2::CompleteProfilerStart](../../winscript/reference/iactivescriptprofilercontrol2-completeprofilerstart.md) profil oluşturma başlatıldı profil oluşturucu bildirir.  
>   -   Çağrı [IActiveScriptProfilerControl2::PrepareProfilerStop](../../winscript/reference/iactivescriptprofilercontrol2-prepareprofilerstop.md) , kısa süre içinde profil oluşturmayı durdurur, profil oluşturucu bildirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Profil Oluşturucu Arabirimleri](../../winscript/reference/active-script-profiler-interfaces.md)