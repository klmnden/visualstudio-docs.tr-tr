---
title: Iactivescriptprofilercontrol arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1448b394-9743-41b5-8eb9-5026a45773a4
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7caa09f384ce460a3e73b21b10d6d8022182dde7
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349497"
---
# <a name="iactivescriptprofilercontrol-interface"></a>IActiveScriptProfilerControl Arabirimi
Profil oluşturmayı destekler komut dosyası altyapısı tarafından uygulanır. Genellikle, uygulayan bir nesne `IActiveScriptProfilerControl` ayrıca uygulayan [IActiveScript](../../winscript/reference/iactivescript.md) arabirimi. Bu durumda, yönelik bir tanıtıcı elde edebilirsiniz `IActiveScriptProfilerControl` çağırarak arabirim `IUnknown::QueryInterface` nesnesi üzerinde yöntemi. Arabirimi, durdurma ve başlatma komut dosyası altyapısına profil oluşturma için gereken yöntemleri sağlar.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptProfilerControl::StartProfiling](../../winscript/reference/iactivescriptprofilercontrol-startprofiling.md)|Komut dosyası altyapısına'profil oluşturmaya başlar.|  
|[IActiveScriptProfilerControl::SetProfilerEventMask](../../winscript/reference/iactivescriptprofilercontrol-setprofilereventmask.md)|Profil oluşturucu komut dosyası altyapısı içinde olay maskesini ayarlar.|  
|[IActiveScriptProfilerControl::StopProfiling](../../winscript/reference/iactivescriptprofilercontrol-stopprofiling.md)|Komut dosyası altyapısına profil oluşturmayı durdurur.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Profil Oluşturucu Arabirimleri](../../winscript/reference/active-script-profiler-interfaces.md)