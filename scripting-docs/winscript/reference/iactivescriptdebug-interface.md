---
title: Iactivescriptdebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptDebug interface
ms.assetid: e3e28cba-ee08-4a52-973a-b74be488c348
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0e21f4c99da886bc4907acf8b0934e1b46d57689
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54344583"
---
# <a name="iactivescriptdebug-interface"></a>IActiveScriptDebug Arabirimi
Destek hata ayıklama komut dosyası motoru tarafından uygulanır. Genellikle, uygulayan bir nesne `IActiveScriptDebug` arabirimini de uygular `IActiveScript` arabirimi. Bu durumda, çağrı `IActiveScript::QueryInterface` elde etmek için yöntemi `IActiveScriptDebug` arabirimi.  
  
 `IActiveScriptDebug` Arabirim için gereken araçları sağlar:  
  
- Belge yönetimini almak için akıllı ana bilgisayar'ı seçin.  
  
- Birden çok komut dosyası motorları, hata ayıklama eşitlemek için işlem hata ayıklama Yöneticisi.  
  
  Devralınan yöntemleri yanı sıra `IUnknown`, `IActiveScriptDebug` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptDebug::GetScriptTextAttributes](../../winscript/reference/iactivescriptdebug-getscripttextattributes.md)|Rastgele bir betik metin bloğu için metin öznitelikleri döndürür.|  
|[IActiveScriptDebug::GetScriptletTextAttributes](../../winscript/reference/iactivescriptdebug-getscriptlettextattributes.md)|Rastgele bir kod oluşturma için metin öznitelikleri döndürür.|  
|[IActiveScriptDebug::EnumCodeContextsOfPosition](../../winscript/reference/iactivescriptdebug-enumcodecontextsofposition.md)|Devreder `IDebugDocumentContext::EnumCodeContexts`.|