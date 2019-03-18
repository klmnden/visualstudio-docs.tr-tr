---
title: Iactivescriptsitedebugex arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 605505d101611dfe39835671b042852eab5ca9cb
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146948"
---
# <a name="iactivescriptsitedebugex-interface"></a>IActiveScriptSiteDebugEx Arabirimi

İle birlikte bu arabirimi uygulayan `IActiveScriptSiteDebug` bir uygulamada bir çalışma zamanı hatası bir bildirim alın ve hata ayıklama için uygulamayı isteğe bağlı olarak eklemek için gereken bir konak yazıyorsanız arabirim. Hata ayıklama işlemi Yöneticisi üzerinden bildirim sağlayan `IActiveScriptDebug` Just-ın-Time hata ayıklayıcı komut dosyası, bilgisayarda bulunur. Hiçbir Just-ın-Time hata ayıklayıcı komut dosyası ise, bulundu, PDM sağlar üzerinden bildirim `IActiveScriptDebugEx` yerine.

Bir çalışma zamanı hatası ilişkin bir bildirim almak için ana işlemelidir `ActiveScriptSiteDebug::OnScriptErrorDebug`. Bir kullanıcı eylemine bağlı olarak, ardından return ve iç hata ayıklayıcı iliştirmek için ya da hata ayıklayıcıda OnScriptErrorDebug başlangıç döndürülecek karar verebilir `pfEnterDebugger` parametresi.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri

|Yöntem|Açıklama|
|------------|-----------------|
|[IActiveScriptSiteDebugEx::OnCanNotJITScriptErrorDebug](../../winscript/reference/iactivescriptsitedebugex-oncannotjitscripterrordebug.md)|Konak işlemde hata ayıklamak, Yöneticisi bir komut dosyası çalışma zamanı hatası hakkında bir dış tam zamanında hata ayıklayıcı bulamazsa bildirir.|