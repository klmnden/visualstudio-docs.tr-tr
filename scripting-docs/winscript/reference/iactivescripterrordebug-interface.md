---
title: Iactivescripterrordebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptErrorDebug interface
ms.assetid: e5d50427-c033-4138-ac6e-3b2dfb3b750a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4d773724d23c61aa72b8cd48917f2cd0bef4a7cb
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345207"
---
# <a name="iactivescripterrordebug-interface"></a>IActiveScriptErrorDebug Arabirimi
Derleme zamanı hataları ve çalışma zamanı özel durumları için belge bağlam bilgilerini sağlar. `IActiveScriptError::QueryInterface` Yöntemi destekler `IActiveScriptErrorDebug` arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IActiveScriptError`, `IActiveScriptErrorDebug` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptErrorDebug::GetDocumentContext](../../winscript/reference/iactivescripterrordebug-getdocumentcontext.md)|Bu hata için belge bağlamı sağlar.|  
|[IActiveScriptErrorDebug::GetStackFrame](../../winscript/reference/iactivescripterrordebug-getstackframe.md)|Çalışma zamanı hataları için geçerli olan yığın çerçevesi sağlar.|