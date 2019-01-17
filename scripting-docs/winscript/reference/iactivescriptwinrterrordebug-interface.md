---
title: Iactivescriptwinrterrordebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptWinRTErrorDebug Interface
ms.assetid: 58b45096-633f-479f-95c4-8eae7376d3a1
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2355b9aa38abbed2ca66964a07bb47082eb76c32
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346507"
---
# <a name="iactivescriptwinrterrordebug-interface"></a>IActiveScriptWinRTErrorDebug Arabirimi
Genişletilmiş Windows çalışma zamanı hata bilgileri sağlamak için JavaScript altyapısı tarafından uygulanan bir [BREAKREASON listelemesi](../../winscript/reference/breakreason-enumeration.md) olay. Bir QueryInterface almak için yapabileceğiniz bir [Iactivescripterror](../../winscript/reference/iactivescripterror.md) nesne.  
  
> [!IMPORTANT]
>  Bu arabirim PDM v11.0 ve sonraki sürümler tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IActiveScriptWinRTErrorDebug` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptWinRTErrorDebug::GetCapabilitySid](../../winscript/reference/iactivescriptwinrterrordebug-getcapabilitysid.md)|Varsa Windows çalışma zamanı hatası olanağını SID döndürür.|  
|[IActiveScriptWinRTErrorDebug::GetRestrictedErrorReference](../../winscript/reference/iactivescriptwinrterrordebug-getrestrictederrorreference.md)|Döndürür Windows çalışma zamanı hatası başvuru dizesi varsa kısıtlı.|  
|[IActiveScriptWinRTErrorDebug::GetRestrictedErrorString](../../winscript/reference/iactivescriptwinrterrordebug-getrestrictederrorstring.md)|Varsa, döndürür Windows çalışma zamanı hata dizesi kısıtlı.|