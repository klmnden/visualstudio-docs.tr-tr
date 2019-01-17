---
title: Idebugstackframe arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugStackFrame interface
ms.assetid: e95c1b4f-17c1-490c-a56b-c25fa45d4822
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0834abbedf88b911dd952c1f3928c5da3414abec
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348548"
---
# <a name="idebugstackframe-interface"></a>IDebugStackFrame Arabirimi
İş parçacığı yığınında bir mantıksal yığın çerçevesini temsil eder. Çağrı `IDebugStackFrame::QueryInterface` elde etmek için yöntemi `IDebugExpressionContext` ifade değerlendirme ve İzle pencereleri sağlayan arabirim.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugStackFrame` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugStackFrame::GetCodeContext](../../winscript/reference/idebugstackframe-getcodecontext.md)|Yığın çerçevesiyle ilgili geçerli kod bağlamı döndürür.|  
|[IDebugStackFrame::GetDescriptionString](../../winscript/reference/idebugstackframe-getdescriptionstring.md)|Yığın çerçevesinin kısa veya uzun metin açıklamasını döndürür.|  
|[IDebugStackFrame::GetLanguageString](../../winscript/reference/idebugstackframe-getlanguagestring.md)|Bu dil kısa veya uzun metin açıklamasını döndürür.|  
|[IDebugStackFrame::GetThread](../../winscript/reference/idebugstackframe-getthread.md)|Bu yığın çerçevesiyle ilgili iş parçacığı döndürür.|  
|[IDebugStackFrame::GetDebugProperty](../../winscript/reference/idebugstackframe-getdebugproperty.md)|Geçerli çerçeve için bir özellik tarayıcısı döndürür.|