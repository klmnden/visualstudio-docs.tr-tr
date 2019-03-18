---
title: SCRIPTTHREADID sabitleri | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: dfbb39d10d552141a68d40a7be3f1715a80f8f57
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58158058"
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