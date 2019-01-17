---
title: Iactivescriptsitedebugex arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptSiteDebugEx Interface
ms.assetid: 76869378-1a7b-47bd-8cd0-acc31f91d58d
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c1e462630f7bf52c4ca94aa59df22616e9a335a7
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345883"
---
# <a name="iactivescriptsitedebugex-interface"></a>IActiveScriptSiteDebugEx Arabirimi
İle birlikte bu arabirimi uygulayan `IActiveScriptSiteDebug` bir uygulamada bir çalışma zamanı hatası bir bildirim alın ve hata ayıklama için uygulamayı isteğe bağlı olarak eklemek için gereken bir konak yazıyorsanız arabirim. Hata ayıklama işlemi Yöneticisi üzerinden bildirim sağlayan `IActiveScriptDebug` Just-ın-Time hata ayıklayıcı komut dosyası, bilgisayarda bulunur. Hiçbir Just-ın-Time hata ayıklayıcı komut dosyası ise, bulundu, PDM sağlar üzerinden bildirim `IActiveScriptDebugEx` yerine.  
  
 Bir çalışma zamanı hatası ilişkin bir bildirim almak için ana işlemelidir [ActiveScriptSiteDebug::OnScriptErrorDebug](http://msdn.microsoft.com/en-us/cf7639f9-a699-4571-9f3a-82ef52c0b5f4). Bir kullanıcı eylemine bağlı olarak, ardından return ve iç hata ayıklayıcı iliştirmek için ya da hata ayıklayıcıda OnScriptErrorDebug başlangıç döndürülecek karar verebilir `pfEnterDebugger` parametresi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptSiteDebugEx::OnCanNotJITScriptErrorDebug](../../winscript/reference/iactivescriptsitedebugex-oncannotjitscripterrordebug.md)|Konak işlemde hata ayıklamak, Yöneticisi bir komut dosyası çalışma zamanı hatası hakkında bir dış tam zamanında hata ayıklayıcı bulamazsa bildirir.|