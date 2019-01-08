---
title: SCRIPTTHREADID sabitleri | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- SCRIPTTHREADID
apilocation:
- scrobj.dll
helpviewer_keywords:
- SCRIPTTHREADID
ms.assetid: 1df9940c-ad0c-42d8-96b9-6a6abe2382e6
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 27852f97cf0a78919b10043c64b1c5a7cc7d3ec5
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097818"
---
# <a name="scriptthreadid-constants"></a>SCRIPTTHREADID Sabitleri
İş parçacığı türünü belirtmek için kullanılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef DWORD SCRIPTTHREADID;  
```  
  
## <a name="constants"></a>Sabitler  
  
|Sabit|Değer|Açıklama|  
|--------------|-----------|-------------|  
|SCRIPTTHREADID_CURRENT|0xFFFFFFFD|Şu anda yürütülen iş parçacığı.|  
|SCRIPTTHREADID_BASE|0xFFFFFFFE|Temel; iş parçacığı diğer bir deyişle, iş parçacığı, komut dosyası altyapısı örneği.|  
|SCRIPTTHREADID_ALL|0xFFFFFFFF|Tüm iş parçacıkları.|  
  
## <a name="remarks"></a>Açıklamalar  
 `SCRIPTTHREADID` Türü tarafından kullanılan `IActiveScript::GetCurrentScriptThreadID`, `IActiveScript::GetScriptThreadID`, `IActiveScript::GetScriptThreadState`, ve `IActiveScript::InterruptScriptThread`, ancak sabitler tarafından yalnızca kullanılabilir `IActiveScript::GetScriptThreadState` ve `IActiveScript::InterruptScriptThread`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript::GetCurrentScriptThreadID](../../winscript/reference/iactivescript-getcurrentscriptthreadid.md)   
 [IActiveScript::GetScriptThreadID](../../winscript/reference/iactivescript-getscriptthreadid.md)   
 [IActiveScript::GetScriptThreadState](../../winscript/reference/iactivescript-getscriptthreadstate.md)   
 [IActiveScript::InterruptScriptThread](../../winscript/reference/iactivescript-interruptscriptthread.md)