---
title: Iactivescriptwinrterrordebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 52e7728b4143231912227e5e55faa5eef01b7490
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63425780"
---
# <a name="iactivescriptwinrterrordebug-interface"></a>IActiveScriptWinRTErrorDebug Arabirimi
Genişletilmiş Windows çalışma zamanı hata bilgileri sağlamak için JavaScript altyapısı tarafından uygulanan bir [BREAKREASON listelemesi](../../winscript/reference/breakreason-enumeration.md) olay. Bir QueryInterface almak için yapabileceğiniz bir [Iactivescripterror](../../winscript/reference/iactivescripterror.md) nesne.  
  
> [!IMPORTANT]
> Bu arabirim PDM v11.0 ve sonraki sürümler tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IActiveScriptWinRTErrorDebug` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptWinRTErrorDebug::GetCapabilitySid](../../winscript/reference/iactivescriptwinrterrordebug-getcapabilitysid.md)|Varsa Windows çalışma zamanı hatası olanağını SID döndürür.|  
|[IActiveScriptWinRTErrorDebug::GetRestrictedErrorReference](../../winscript/reference/iactivescriptwinrterrordebug-getrestrictederrorreference.md)|Döndürür Windows çalışma zamanı hatası başvuru dizesi varsa kısıtlı.|  
|[IActiveScriptWinRTErrorDebug::GetRestrictedErrorString](../../winscript/reference/iactivescriptwinrterrordebug-getrestrictederrorstring.md)|Varsa, döndürür Windows çalışma zamanı hata dizesi kısıtlı.|