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
ms.openlocfilehash: e390b610d6912de0078b817c9dfb503e5924a374
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54797436"
---
# <a name="iactivescriptsitedebugex-interface"></a>IActiveScriptSiteDebugEx Arabirimi

İle birlikte bu arabirimi uygulayan `IActiveScriptSiteDebug` bir uygulamada bir çalışma zamanı hatası bir bildirim alın ve hata ayıklama için uygulamayı isteğe bağlı olarak eklemek için gereken bir konak yazıyorsanız arabirim. Hata ayıklama işlemi Yöneticisi üzerinden bildirim sağlayan `IActiveScriptDebug` Just-ın-Time hata ayıklayıcı komut dosyası, bilgisayarda bulunur. Hiçbir Just-ın-Time hata ayıklayıcı komut dosyası ise, bulundu, PDM sağlar üzerinden bildirim `IActiveScriptDebugEx` yerine.

Bir çalışma zamanı hatası ilişkin bir bildirim almak için ana işlemelidir `ActiveScriptSiteDebug::OnScriptErrorDebug`. Bir kullanıcı eylemine bağlı olarak, ardından return ve iç hata ayıklayıcı iliştirmek için ya da hata ayıklayıcıda OnScriptErrorDebug başlangıç döndürülecek karar verebilir `pfEnterDebugger` parametresi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri

|Yöntem|Açıklama|
|------------|-----------------|
|[IActiveScriptSiteDebugEx::OnCanNotJITScriptErrorDebug](../../winscript/reference/iactivescriptsitedebugex-oncannotjitscripterrordebug.md)|Konak işlemde hata ayıklamak, Yöneticisi bir komut dosyası çalışma zamanı hatası hakkında bir dış tam zamanında hata ayıklayıcı bulamazsa bildirir.|