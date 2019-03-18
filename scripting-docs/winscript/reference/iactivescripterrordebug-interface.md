---
title: Iactivescripterrordebug arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 936770859d3bdfe81c84245d32ae63346b142a01
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58153753"
---
# <a name="iactivescripterrordebug-interface"></a>IActiveScriptErrorDebug Arabirimi
Derleme zamanı hataları ve çalışma zamanı özel durumları için belge bağlam bilgilerini sağlar. `IActiveScriptError::QueryInterface` Yöntemi destekler `IActiveScriptErrorDebug` arabirimi.  
  
 Devralınan yöntemleri yanı sıra `IActiveScriptError`, `IActiveScriptErrorDebug` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptErrorDebug::GetDocumentContext](../../winscript/reference/iactivescripterrordebug-getdocumentcontext.md)|Bu hata için belge bağlamı sağlar.|  
|[IActiveScriptErrorDebug::GetStackFrame](../../winscript/reference/iactivescripterrordebug-getstackframe.md)|Çalışma zamanı hataları için geçerli olan yığın çerçevesi sağlar.|