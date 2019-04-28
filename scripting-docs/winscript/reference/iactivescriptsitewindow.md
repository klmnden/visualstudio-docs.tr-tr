---
title: Iactivescriptsitewindow | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptSiteWindow interface
ms.assetid: 96d5c493-2c0b-47e2-848b-4a8dacdcd65c
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3691a874121c00dcccc69958eb5746a2c1d78122
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62992020"
---
# <a name="iactivescriptsitewindow"></a>IActiveScriptSiteWindow
Bu arabirim aynı nesne üzerinde bir kullanıcı arabirimini destekleyen konaklar tarafından uygulanan [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) . Uygulamaz sunucuları gibi bir kullanıcı arabirimi desteklemeyen Konaklar `IActiveScriptSiteWindow` arabirimi. Komut dosyası altyapısı çağırarak bu arabirimi erişen `QueryInterface` gelen `IActiveScriptSite`.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptSiteWindow::GetWindow](../../winscript/reference/iactivescriptsitewindow-getwindow.md)|Komut dosyası altyapısı görüntülemelidir bir açılır pencere sahibi olarak davranıp pencere tanıtıcısı alır.|  
|[IActiveScriptSiteWindow::EnableModeless](../../winscript/reference/iactivescriptsitewindow-enablemodeless.md)|Etkinleştirmek veya kalıcı olmayan iletişim kutuları yanı sıra ana penceresi devre dışı bırakmak için ana neden olur.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Arabirimleri](../../winscript/reference/active-script-interfaces.md)